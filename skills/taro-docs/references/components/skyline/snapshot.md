# Snapshot

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/skyline/snapshot)

截图组件
支持将其子节点的渲染结果导出成图片，该组件需配合 snapshot 接口使用。 目前仅在 Skyline 渲染引擎 下支持。

支持情况：微信小程序 H5 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/snapshot.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<SnapshotProps>
```

<a id="snapshotprops"></a>

## SnapshotProps

| 参数 | 类型 | 默认值 | 说明 |
| --- | --- | --- | --- |
| mode | "view" or "picture" | `'view'<br /><br />可选值:<br />- view: 以真实节点渲染<br />- picture: 对子节点生成的内容截图渲染` | 渲染模式 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- |
| SnapshotProps.mode | ✔️ |  |  |  |
