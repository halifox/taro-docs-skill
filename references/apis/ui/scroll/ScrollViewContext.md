# ScrollViewContext

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/ui/scroll/ScrollViewContext)

增强 ScrollView 实例，可通过 [Taro.createSelectorQuery](../../wxml/createSelectorQuery.md) 的 [NodesRef.node](../../wxml/NodesRef.md#node) 方法获取。 仅在 `scroll-view` 组件开启 `enhanced` 属性后生效。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/scroll/ScrollViewContext.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| scrollEnabled | `boolean` | 滚动开关 |
| bounces | `boolean` | 设置滚动边界弹性 (仅在 iOS 下生效) |
| showScrollbar | `boolean` | 设置是否显示滚动条 |
| pagingEnabled | `boolean` | 分页滑动开关 |
| fastDeceleration | `boolean` | 设置滚动减速速率 |
| decelerationDisabled | `boolean` | 取消滚动惯性 (仅在 iOS 下生效) |

<a id="scrollto"></a>

### scrollTo

滚动至指定位置

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> H5: 不支持 velocity 参数

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/scroll/ScrollViewContext.scrollTo.html)

```tsx
(object: Option) => void
```

| 参数 | 类型 |
| --- | --- |
| object | `Option` |

<a id="scrollintoview"></a>

### scrollIntoView

滚动至指定位置

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/scroll/ScrollViewContext.scrollIntoView.html)

```tsx
(selector: string) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| selector | `string` | 元素选择器 |

<a id="参数"></a>

## 参数

<a id="scrollto-1"></a>

### scrollTo

<a id="option"></a>

#### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| top | `number` | 否 | 顶部距离 |
| left | `number` | 否 | 左边界距离 |
| velocity | `number` | 否 | 初始速度 |
| duration | `number` | 否 | 滚动动画时长 |
| animated | `boolean` | 否 | 是否启用滚动动画 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.createSelectorQuery()
  .select('#scrollview')
  .node()
  .exec((res) => {
    const scrollView = res[0].node;
    scrollView.scrollEnabled = false;
  })
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | 抖音小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| ScrollViewContext | ✔️ |  |  |  |  |  |
| ScrollViewContext.scrollTo | ✔️ |  | ✔️(不支持 velocity 参数) |  |  |  |
| ScrollViewContext.scrollIntoView | ✔️ | ✔️ | ✔️ |  |  |  |
