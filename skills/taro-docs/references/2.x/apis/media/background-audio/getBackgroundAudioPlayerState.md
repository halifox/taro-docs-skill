# Taro.getBackgroundAudioPlayerState(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/background-audio/getBackgroundAudioPlayerState)

获取后台音乐播放状态。
**注意：1.2.0 版本开始，本接口不再维护。建议使用能力更强的 [Taro.getBackgroundAudioManager](https://developers.weixin.qq.com/miniprogram/dev/api/media/background-audio/wx.getBackgroundAudioManager.html) 接口**

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/background-audio/wx.getBackgroundAudioPlayerState.html)

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
| currentPosition | `number` | 选定音频的播放位置（单位：s），只有在音乐播放中时返回 |
| dataUrl | `string` | 歌曲数据链接，只有在音乐播放中时返回 |
| downloadPercent | `number` | 音频的下载进度百分比，只有在音乐播放中时返回 |
| duration | `number` | 选定音频的长度（单位：s），只有在音乐播放中时返回 |
| status | `0 \| 1 \| 2` | 播放状态 |
| errMsg | `string` | 调用结果 |

<a id="status"></a>

### status

| 参数 | 说明 |
| --- | --- |
| 0 | 暂停中 |
| 1 | 播放中 |
| 2 | 没有音乐播放 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getBackgroundAudioPlayerState({
  success: function (res) {
    var status = res.status
    var dataUrl = res.dataUrl
    var currentPosition = res.currentPosition
    var duration = res.duration
    var downloadPercent = res.downloadPercent
  }
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.getBackgroundAudioPlayerState | ✔️ |  |  |
