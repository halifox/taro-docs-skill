# ChannelVideo

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/media/channel-video)

小程序内嵌视频号视频组件，支持在小程序中播放视频号视频，并无弹窗跳转至视频号。注意：使用该组件打开的视频号视频需要与小程序相同主体或关联主体。

支持情况：微信小程序 H5 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/channel-video.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<ChannelVideoProps>
```

<a id="channelvideoprops"></a>

## ChannelVideoProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| feedId | `string` |  | 是 | 仅视频号视频与小程序同主体时生效。若内嵌非同主体视频，请使用 feed-token。 |
| finderUserName | `string` |  | 是 | 视频号 id，以“sph”开头的id，可在视频号助手获取。视频号必须与当前小程序相同主体。 |
| loop | `boolean` | `false` | 否 | 是否循环播放 |
| muted | `boolean` | `false` | 否 | 是否静音播放 |
| objectFit | "fill" or "contain" or "cover" | `"contain"` | 否 | 当视频大小与 video 容器大小不一致时，视频的表现形式 |
| autoplay | `boolean` | `false` | 否 | 是否自动播放 |
| feedToken | `string` |  | 否 | 仅内嵌小程序非同主体视频号视频时使用，获取方式参考[本指引](https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/channels-activity.html#feed-token)。 |
| onError | `CommonEventFunction` |  | 否 | 视频播放出错时触发 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- |
| ChannelVideoProps.feedId | ✔️ |  |  |  |
| ChannelVideoProps.finderUserName | ✔️ |  |  |  |
| ChannelVideoProps.loop | ✔️ |  |  |  |
| ChannelVideoProps.muted | ✔️ |  |  |  |
| ChannelVideoProps.objectFit | ✔️ |  |  |  |
| ChannelVideoProps.autoplay | ✔️ |  |  |  |
| ChannelVideoProps.feedToken | ✔️ |  |  |  |
| ChannelVideoProps.onError | ✔️ |  |  |  |
