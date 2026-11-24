# router

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/route/router)

<a id="类型"></a>

## 类型

```tsx
router
```

<a id="参数"></a>

## 参数

<a id="customroutebuilder"></a>

### CustomRouteBuilder

```tsx
(routeContext: CustomRouteContext,routeOptions: Record<string, any>) => CustomRouteConfig
```

| 参数 | 类型 |
| --- | --- |
| routeContext | `CustomRouteContext` |
| routeOptions | `Record<string, any>` |

<a id="sharedvalue"></a>

### SharedValue

| 参数 | 类型 |
| --- | --- |
| value | `T` |

<a id="customroutecontext"></a>

### CustomRouteContext

| 参数 | 类型 |
| --- | --- |
| primaryAnimation | `SharedValue<number>` |
| primaryAnimationStatus | `SharedValue<number>` |
| secondaryAnimation | `SharedValue<number>` |
| secondaryAnimationStatus | `SharedValue<number>` |
| userGestureInProgress | `SharedValue<number>` |
| startUserGesture | `() => void` |
| stopUserGesture | `() => void` |
| didPop | `() => void` |

<a id="customrouteconfig"></a>

### CustomRouteConfig

| 参数 | 类型 | 必填 |
| --- | --- | --- |
| opaque | `boolean` | 否 |
| maintainState | `boolean` | 否 |
| transitionDuration | `number` | 否 |
| reverseTransitionDuration | `number` | 否 |
| barrierColor | `string` | 否 |
| barrierDismissible | `boolean` | 否 |
| barrierLabel | `string` | 否 |
| canTransitionTo | `boolean` | 否 |
| canTransitionFrom | `boolean` | 否 |
| handlePrimaryAnimation | `RouteAnimationHandler` | 否 |
| handleSecondaryAnimation | `RouteAnimationHandler` | 否 |
| handlePreviousPageAnimation | `RouteAnimationHandler` | 否 |
| allowEnterRouteSnapshotting | `boolean` | 否 |
| allowExitRouteSnapshotting | `boolean` | 否 |
| fullscreenDrag | `boolean` | 否 |
| popGestureDirection | "horizontal" or "vertical" or "multi" | 否 |

<a id="routeanimationhandler"></a>

### RouteAnimationHandler

```tsx
() => { [key: string]: any; }
```

<a id="router"></a>

### router

自定义路由

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/route/router/wx.router.html)

<a id="addroutebuilder"></a>

#### addRouteBuilder

添加自定义路由配置

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/route/router/base/router.addRouteBuilder.html)

```tsx
(routeType: string, routeBuilder: CustomRouteBuilder) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| routeType | `string` | 路由类型 |
| routeBuilder | `CustomRouteBuilder` | 路由动画定义函数 |

<a id="getroutecontext"></a>

#### getRouteContext

获取页面对应的自定义路由上下文对象

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/route/router/base/router.getRouteContext.html)

```tsx
(instance: TaroGeneral.IAnyObject) => CustomRouteContext
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| instance | `TaroGeneral.IAnyObject` | 页面/自定义组件实例 |

<a id="removeroutebuilder"></a>

#### removeRouteBuilder

移除自定义路由配置

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/route/router/base/router.removeRouteBuilder.html)

```tsx
(routeType: string) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| routeType | `string` | 路由类型 |
