# Taro.pauseVoice()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/multimedia/audio/pauseVoice)

暂停正在播放的语音。再次调用 Taro.playVoice 播放同一个文件时，会从暂停处开始播放。如果想从头开始播放，需要先调用 Taro.stopVoice。

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.startRecord(params)
  .then(res => {
    const filePath = res.tempFilePath
    Taro.playVoice({ filePath })

    setTimeout(Taro.pauseVoice, 5000)
  })
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native | 支付宝小程序 | 百度小程序 |
| --- | --- | --- | --- | --- | --- |
| Taro.pauseVoice | ✔️ |  |  |  |  |
