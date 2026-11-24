# Taro.pauseVoice(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/audio/pauseVoice)

暂停正在播放的语音。再次调用 [Taro.playVoice](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/wx.playVoice.html) 播放同一个文件时，会从暂停处开始播放。如果想从头开始播放，需要先调用 [Taro.stopVoice](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/wx.stopVoice.html)。
**注意：1.6.0 版本开始，本接口不再维护。建议使用能力更强的 [Taro.createInnerAudioContext](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/wx.createInnerAudioContext.html) 接口**

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/wx.pauseVoice.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => void
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.startRecord({
  success: function (res) {
    var tempFilePath = res.tempFilePath
      Taro.playVoice({
      filePath: tempFilePath
    })
    setTimeout(function() {
        //暂停播放
      Taro.pauseVoice()
    }, 5000)
  }
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.pauseVoice | ✔️ |  |  |
