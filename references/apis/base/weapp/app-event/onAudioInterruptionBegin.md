# Taro.onAudioInterruptionBegin(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/base/weapp/app-event/onAudioInterruptionBegin)

监听音频因为受到系统占用而被中断开始事件。以下场景会触发此事件：闹钟、电话、FaceTime 通话、微信语音聊天、微信视频聊天。此事件触发后，小程序内所有音频会暂停。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/app/app-event/wx.onAudioInterruptionBegin.html)

<a id="类型"></a>

## 类型

```tsx
(callback: (res: TaroGeneral.CallbackResult) => void) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `(res: TaroGeneral.CallbackResult) => void` | 音频因为受到系统占用而被中断开始事件的回调函数 |
