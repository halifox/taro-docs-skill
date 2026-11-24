# ChannelLive

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/media/channel-live)

小程序内嵌视频号直播组件，展示视频号直播状态和封面，并无弹窗跳转至视频号。注意：使用该组件打开的视频号视频需要与小程序的主体一致。

支持情况：微信小程序 H5 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/channel-live.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<ChannelLiveProps>
```

<a id="channelliveprops"></a>

## ChannelLiveProps

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| feedId | `string` | 视频 feedId |
| finderUserName | `string` | 视频号 id，以“sph”开头的id，可在视频号助手获取。视频号必须与当前小程序相同主体。 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- |
| ChannelLiveProps.feedId | ✔️ |  |  |  |
| ChannelLiveProps.finderUserName | ✔️ |  |  |  |
