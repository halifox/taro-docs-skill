# Taro.getRecorderManager()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/media/recorder/getRecorderManager)

获取**全局唯一**的录音管理器 RecorderManager

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/recorder/wx.getRecorderManager.html)

<a id="类型"></a>

## 类型

```tsx
() => RecorderManager
```

<a id="示例代码"></a>

## 示例代码

```tsx
const recorderManager = Taro.getRecorderManager()
recorderManager.onStart(() => {
  console.log('recorder start')
})
recorderManager.onPause(() => {
  console.log('recorder pause')
})
recorderManager.onStop((res) => {
  console.log('recorder stop', res)
  const { tempFilePath } = res
})
recorderManager.onFrameRecorded((res) => {
  const { frameBuffer } = res
  console.log('frameBuffer.byteLength', frameBuffer.byteLength)
})
const options = {
  duration: 10000,
  sampleRate: 44100,
  numberOfChannels: 1,
  encodeBitRate: 192000,
  format: 'aac',
  frameSize: 50
}
recorderManager.start(options)
```
