# DraggableSheetContext

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/skyline/DraggableSheetContext)

DraggableSheet 实例，可通过 Taro.createSelectorQuery 的 NodesRef.node 方法获取。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/skyline/DraggableSheetContext.html)

<a id="方法"></a>

## 方法

<a id="scrollto"></a>

### scrollTo

滚动到指定位置。size 取值 [0, 1]，size = 1 时表示撑满 draggable-sheet 组件。size 和 pixels 同时传入时，仅 size 生效。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/skyline/DraggableSheetContext.scrollTo.html)

```tsx
(option: Option) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="参数"></a>

## 参数

<a id="scrollto-1"></a>

### scrollTo

<a id="option"></a>

#### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| size | `number` |  | 否 | 相对目标位置 |
| pixels | `number` |  | 否 | 绝对目标位置 |
| animated | `boolean` | `true` | 否 | 是否启用滚动动画 |
| duration | `number` | `300` | 否 | 滚动动画时长（ms) |
| easingFunction | `string` | `ease` | 否 | 缓动函数 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| DraggableSheetContext | ✔️ |  |  |  |  |
