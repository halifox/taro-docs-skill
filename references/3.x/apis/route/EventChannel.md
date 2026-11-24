# EventChannel

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/route/EventChannel)

页面间事件通信通道

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/route/EventChannel.html)

<a id="方法"></a>

## 方法

<a id="emit"></a>

### emit

触发一个事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/route/EventChannel.emit.html)

```tsx
(eventName: string, ...args: any) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| eventName | `string` | 事件名称 |
| args | `any` | 事件参数 |

<a id="on"></a>

### on

持续监听一个事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/route/EventChannel.on.html)

```tsx
(eventName: string, fn: TaroGeneral.EventCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| eventName | `string` | 事件名称 |
| fn | `TaroGeneral.EventCallback` | 事件监听函数 |

<a id="once"></a>

### once

监听一个事件一次，触发后失效

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/route/EventChannel.once.html)

```tsx
(eventName: string, fn: TaroGeneral.EventCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| eventName | `string` | 事件名称 |
| fn | `TaroGeneral.EventCallback` | 事件监听函数 |

<a id="off"></a>

### off

取消监听一个事件。给出第二个参数时，只取消给出的监听函数，否则取消所有监听函数

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/route/EventChannel.off.html)

```tsx
(eventName: string, fn: TaroGeneral.EventCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| eventName | `string` | 事件名称 |
| fn | `TaroGeneral.EventCallback` | 事件监听函数 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| EventChannel | ✔️ |  |  |  |  |
| EventChannel.emit | ✔️ |  |  |  |  |
| EventChannel.on | ✔️ |  |  |  |  |
| EventChannel.once | ✔️ |  |  |  |  |
| EventChannel.off | ✔️ |  |  |  |  |
