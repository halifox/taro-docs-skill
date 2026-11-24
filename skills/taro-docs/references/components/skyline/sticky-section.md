# StickySection

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/skyline/sticky-section)

吸顶布局容器，仅支持作为 scroll-view 自定义模式下的直接子节点。仅 Skyline 支持。

支持情况：微信小程序 H5 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/sticky-section.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<StickySectionProps>
```

<a id="stickysectionprops"></a>

## StickySectionProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| pushPinnedHeader | `boolean` | `true` | 否 | 吸顶元素重叠时是否继续上推 |
| padding | `[number, number, number, number]` | `[0, 0, 0, 0]` | 否 | 长度为 4 的数组，按 top、right、bottom、left 顺序指定内边距 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- |
| StickySectionProps.pushPinnedHeader | ✔️ |  |  |  |
| StickySectionProps.padding | ✔️ |  |  |  |
