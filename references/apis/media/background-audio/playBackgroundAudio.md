# Taro.playBackgroundAudio(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/media/background-audio/playBackgroundAudio)

使用后台播放器播放音乐，对于微信客户端来说，只能同时有一个后台音乐在播放。当用户离开小程序后，音乐将暂停播放；当用户点击“显示在聊天顶部”时，音乐不会暂停播放；当用户在其他小程序占用了音乐播放器，原有小程序内的音乐将停止播放。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/background-audio/wx.playBackgroundAudio.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<TaroGeneral.CallbackResult>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| dataUrl | `string` | 是 | 音乐链接，目前支持的格式有 m4a, aac, mp3, wav |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| coverImgUrl | `string` | 否 | 封面URL |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |
| title | `string` | 否 | 音乐标题 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.playBackgroundAudio({
  dataUrl: '',
  title: '',
  coverImgUrl: ''
})
```
