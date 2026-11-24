# MediaAudioPlayer

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/media/audio/MediaAudioPlayer)

MediaAudioPlayer 实例，可通过 [Taro.createMediaAudioPlayer](createMediaAudioPlayer.md) 接口获取实例。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/MediaAudioPlayer.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 默认值 | 说明 |
| --- | --- | --- | --- |
| volume | `number` | `1` | 音量。范围 0~1 |

<a id="start"></a>

### start

启动播放器

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/MediaAudioPlayer.start.html)

```tsx
() => Promise<void>
```

<a id="addaudiosource"></a>

### addAudioSource

添加音频源

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/MediaAudioPlayer.addAudioSource.html)

```tsx
(source: VideoDecoder) => Promise<void>
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| source | `VideoDecoder` | 视频解码器实例。作为音频源添加到音频播放器中 |

<a id="removeaudiosource"></a>

### removeAudioSource

移除音频源

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/MediaAudioPlayer.removeAudioSource.html)

```tsx
(source: VideoDecoder) => Promise<void>
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| source | `VideoDecoder` | 视频解码器实例 |

<a id="stop"></a>

### stop

停止播放器

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/MediaAudioPlayer.stop.html)

```tsx
() => Promise<void>
```

<a id="destroy"></a>

### destroy

销毁播放器

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/MediaAudioPlayer.destroy.html)

```tsx
() => Promise<void>
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| MediaAudioPlayer | ✔️ |  |  |  |  |
| MediaAudioPlayer.start | ✔️ |  |  |  |  |
| MediaAudioPlayer.addAudioSource | ✔️ |  |  |  |  |
| MediaAudioPlayer.removeAudioSource | ✔️ |  |  |  |  |
| MediaAudioPlayer.stop | ✔️ |  |  |  |  |
| MediaAudioPlayer.destroy | ✔️ |  |  |  |  |
