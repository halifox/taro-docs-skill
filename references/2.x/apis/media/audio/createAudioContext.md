# Taro.createAudioContext(id, component)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/audio/createAudioContext)

创建 audio 上下文 AudioContext 对象。
**注意：1.6.0 版本开始，本接口不再维护。建议使用能力更强的 [Taro.createInnerAudioContext](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/wx.createInnerAudioContext.html) 接口**

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/wx.createAudioContext.html)

<a id="类型"></a>

## 类型

```tsx
(id: string, component?: Record<string, any>) => AudioContext
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| id | `string` | [audio](https://developers.weixin.qq.com/miniprogram/dev/component/audio.html) 组件的 id |
| component | `Record<string, any>` | 在自定义组件下，当前组件实例的this，以操作组件内 [audio](https://developers.weixin.qq.com/miniprogram/dev/component/audio.html) 组件 |

<a id="示例代码"></a>

## 示例代码

```tsx
const audioCtx = Taro.createAudioContext('myAudio')
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.createAudioContext | ✔️ |  |  |
