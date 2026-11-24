# Taro.getAvailableAudioSources(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/audio/getAvailableAudioSources)

获取当前支持的音频输入源

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/wx.getAvailableAudioSources.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => Promise<SuccessCallbackResult>
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| audioSources | `("auto" \| "buildInMic" \| "headsetMic" \| "mic" \| "camcorder" \| "voice_communication" \| "voice_recognition")[]` | 支持的音频输入源列表，可在 [RecorderManager.start()](https://developers.weixin.qq.com/miniprogram/dev/api/media/recorder/RecorderManager.start.html) 接口中使用。返回值定义参考 https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource |
| errMsg | `string` | 调用结果 |

<a id="audiosources"></a>

### audioSources

支持的音频输入源

| 参数 | 说明 |
| --- | --- |
| auto | 自动设置，默认使用手机麦克风，插上耳麦后自动切换使用耳机麦克风，所有平台适用 |
| buildInMic | 手机麦克风，仅限 iOS |
| headsetMic | 耳机麦克风，仅限 iOS |
| mic | 麦克风（没插耳麦时是手机麦克风，插耳麦时是耳机麦克风），仅限 Android |
| camcorder | 同 mic，适用于录制音视频内容，仅限 Android |
| voice\_communication | 同 mic，适用于实时沟通，仅限 Android |
| voice\_recognition | 同 mic，适用于语音识别，仅限 Android |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.getAvailableAudioSources | ✔️ |  |  |
