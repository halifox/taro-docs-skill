# FollowSwan

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/open/follow-swan)

关注小程序

支持情况：微信小程序 百度小程序 H5 React Native Harmony

> [参考文档](https://smartprogram.baidu.com/docs/develop/extended/component-content/follow-swan/)

<a id="类型"></a>

## 类型

```tsx
ComponentType<FollowSwanProps>
```

<a id="followswanprops"></a>

## FollowSwanProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| size | `string` | `"default"` | 否 | 组件大小 |
| type | `string` | `"primary"` | 否 | 组件样式 |
| onFavorStatusChange | `CommonEventFunction` |  | 否 | 关注和取消关注成功的回调，返回关注状态 {isFavor: trueorfalse} |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- | --- |
| FollowSwanProps.size |  | ✔️ |  |  |  |
| FollowSwanProps.type |  | ✔️ |  |  |  |
| FollowSwanProps.onFavorStatusChange |  | ✔️ |  |  |  |
