# Taro.setInnerAudioOption(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/audio/setInnerAudioOption)

设置 [InnerAudioContext](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/InnerAudioContext.html) 的播放选项。设置之后对当前小程序全局生效。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/wx.setInnerAudioOption.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<CallbackResult>
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| mixWithOther | `boolean` | 否 | 是否与其他音频混播，设置为 true 之后，不会终止其他应用或微信内的音乐 |
| obeyMuteSwitch | `boolean` | 否 | （仅在 iOS 生效）是否遵循静音开关，设置为 false 之后，即使是在静音模式下，也能播放声音 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.setInnerAudioOption | ✔️ |  |  |
