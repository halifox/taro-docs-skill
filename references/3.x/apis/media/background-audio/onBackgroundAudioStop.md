# Taro.onBackgroundAudioStop(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/media/background-audio/onBackgroundAudioStop)

监听音乐停止。

**bug & tip：**

1. `bug`: `iOS` `6.3.30` Taro.seekBackgroundAudio 会有短暂延迟

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/background-audio/wx.onBackgroundAudioStop.html)

<a id="类型"></a>

## 类型

```tsx
(callback: (res: TaroGeneral.CallbackResult) => void) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `(res: TaroGeneral.CallbackResult) => void` | 音乐停止事件的回调函数 |
