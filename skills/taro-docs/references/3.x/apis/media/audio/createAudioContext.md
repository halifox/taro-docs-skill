# Taro.createAudioContext(id, component)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/media/audio/createAudioContext)

创建 audio 上下文 AudioContext 对象。
**注意：1.6.0 版本开始，本接口不再维护。建议使用能力更强的 [Taro.createInnerAudioContext](createInnerAudioContext.md) 接口**

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/wx.createAudioContext.html)

<a id="类型"></a>

## 类型

```tsx
(id: string, component?: TaroGeneral.IAnyObject) => AudioContext
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| id | `string` | [audio](../../../../components/media/audio.md) 组件的 id |
| component | `TaroGeneral.IAnyObject` | 在自定义组件下，当前组件实例的this，以操作组件内 [audio](../../../../components/media/audio.md) 组件 |

<a id="示例代码"></a>

## 示例代码

```tsx
const audioCtx = Taro.createAudioContext('myAudio')
```
