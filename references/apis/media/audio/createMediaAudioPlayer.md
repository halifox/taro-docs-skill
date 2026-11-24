# Taro.createMediaAudioPlayer()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/media/audio/createMediaAudioPlayer)

创建媒体音频播放器对象 [MediaAudioPlayer](MediaAudioPlayer.md) 对象，可用于播放视频解码器 [VideoDecoder](../video-decoder/VideoDecoder.md) 输出的音频

**注意事项**

- iOS 7.0.15 mediaAudioPlayer 播放网络视频资源会出现音频卡顿，本地视频没有这个问题，将下一个客户端版本修复。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/wx.createMediaAudioPlayer.html)

<a id="类型"></a>

## 类型

```tsx
() => MediaAudioPlayer
```

<a id="示例代码"></a>

## 示例代码

```tsx
// 创建视频解码器，具体参数见 createVideoDecoder 文档
const videoDecoder = Taro.createVideoDecoder()
// 创建媒体音频播放器
const mediaAudioPlayer = Taro.createMediaAudioPlayer()
// 启动视频解码器
videoDecoder.start()
// 启动播放器
mediaAudioPlayer.start().then(() => {
  // 添加播放器音频来源
  mediaAudioPlayer.addAudioSource(videoDecoder).then(res => {
    videoDecoder.getFrameData() // 建议在 requestAnimationFrame 里获取每一帧视频数据
    console.log(res)
  })

  // 移除播放器音频来源
  mediaAudioPlayer.removeAudioSource(videoDecoder).then()
  // 停止播放器
  mediaAudioPlayer.stop().then()
  // 销毁播放器
  mediaAudioPlayer.destroy().then()
  // 设置播放器音量
  mediaAudioPlayer.volume = 0.5
})
```
