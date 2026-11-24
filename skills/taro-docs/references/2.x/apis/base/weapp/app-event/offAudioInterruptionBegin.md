# Taro.offAudioInterruptionBegin(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/base/weapp/app-event/offAudioInterruptionBegin)

取消监听音频因为受到系统占用而被中断开始事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/app/app-event/wx.offAudioInterruptionBegin.html)

<a id="类型"></a>

## 类型

```tsx
(callback: (res: CallbackResult) => void) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `(res: CallbackResult) => void` | 音频因为受到系统占用而被中断开始事件的回调函数 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.offAudioInterruptionBegin | ✔️ |  |  |
