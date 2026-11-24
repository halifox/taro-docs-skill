# AwemeData

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/open/aweme-data)

直播间状态组件

支持情况：微信小程序 抖音小程序 H5 React Native Harmony

> [参考文档](https://developer.open-douyin.com/docs/resource/zh-CN/mini-app/develop/component/open-capacity/aweme-data/)

<a id="类型"></a>

## 类型

```tsx
ComponentType<AwemeDataProps>
```

<a id="awemedataprops"></a>

## AwemeDataProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| awemeId | `string` |  | 否 | 用户的抖音号，可以进入抖音 App 用户个人主页查看 |
| type | `string` | `"avatar"` | 否 | 类型，可以选择头像或昵称 |
| disableDefault | `boolean` | `false` | 否 | 禁用默认行为。点击头像时，如果用户处于直播状态下默认会跳转到直播间，非直播状态下跳转到个人主页。如果为 true，点击头像时不会有默认行为。 |
| defaultAvatar | `string` |  | 否 | 获取信息失败时显示的默认头像 url |
| defaultText | `string` |  | 否 | 获取信息失败时显示的默认昵称文本 |
| onError | `CommonEventFunction` |  | 否 | 当错误发生时触发 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 抖音小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- | --- |
| AwemeDataProps.awemeId |  | ✔️ |  |  |  |
| AwemeDataProps.type |  | ✔️ |  |  |  |
| AwemeDataProps.disableDefault |  | ✔️ |  |  |  |
| AwemeDataProps.defaultAvatar |  | ✔️ |  |  |  |
| AwemeDataProps.defaultText |  | ✔️ |  |  |  |
| AwemeDataProps.onError |  | ✔️ |  |  |  |
