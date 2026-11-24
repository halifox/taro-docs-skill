# VideoContext

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/media/video/VideoContext)

VideoContext 实例，可通过 [Taro.createVideoContext](createVideoContext.md) 获取。

VideoContext 通过 id 跟一个 video 组件绑定，操作对应的 video 组件。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.html)

<a id="方法"></a>

## 方法

<a id="exitbackgroundplayback"></a>

### exitBackgroundPlayback

退出后台音频播放模式。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.exitBackgroundPlayback.html)

```tsx
() => void
```

<a id="exitfullscreen"></a>

### exitFullScreen

退出全屏

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.exitFullScreen.html)

```tsx
() => void
```

<a id="exitpictureinpicture"></a>

### exitPictureInPicture

退出小窗，该方法可在任意页面调用

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.exitPictureInPicture.html)

```tsx
(option: ExitPictureInPictureOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `ExitPictureInPictureOption` |

<a id="hidestatusbar"></a>

### hideStatusBar

隐藏状态栏，仅在iOS全屏下有效

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.hideStatusBar.html)

```tsx
() => void
```

<a id="pause"></a>

### pause

暂停视频

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.pause.html)

```tsx
() => void
```

<a id="play"></a>

### play

播放视频

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.play.html)

```tsx
() => void
```

<a id="playbackrate"></a>

### playbackRate

设置倍速播放

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.playbackRate.html)

```tsx
(rate: number) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| rate | `number` | 倍率，支持 0.5/0.8/1.0/1.25/1.5，2.6.3 起支持 2.0 倍速 |

<a id="requestbackgroundplayback"></a>

### requestBackgroundPlayback

进入后台音频播放模式。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.requestBackgroundPlayback.html)

```tsx
() => void
```

<a id="requestfullscreen"></a>

### requestFullScreen

进入全屏

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.requestFullScreen.html)

```tsx
(option: RequestFullScreenOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `RequestFullScreenOption` |

<a id="seek"></a>

### seek

跳转到指定位置

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.seek.html)

```tsx
(position: number) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| position | `number` | 跳转到的位置，单位 s |

<a id="senddanmu"></a>

### sendDanmu

发送弹幕

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.sendDanmu.html)

```tsx
(data: Danmu) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | `Danmu` | 弹幕内容 |

<a id="showstatusbar"></a>

### showStatusBar

显示状态栏，仅在iOS全屏下有效

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.showStatusBar.html)

```tsx
() => void
```

<a id="stop"></a>

### stop

停止视频

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.stop.html)

```tsx
() => void
```

<a id="参数"></a>

## 参数

<a id="exitpictureinpictureoption"></a>

### ExitPictureInPictureOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| success | `(result: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="requestfullscreenoption"></a>

### RequestFullScreenOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| direction | 0 or 90 or -90 | 否 | 设置全屏时视频的方向，不指定则根据宽高比自动判断。<br><br>可选值：<br>- 0: 正常竖向;<br>- 90: 屏幕逆时针90度;<br>- -90: 屏幕顺时针90度; |

<a id="danmu"></a>

### Danmu

弹幕内容

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| text | `string` | 是 | 弹幕文字 |
| color | `string` | 否 | 弹幕颜色 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| VideoContext | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| VideoContext.exitBackgroundPlayback | ✔️ |  |  |  |  | ✔️ |
| VideoContext.exitFullScreen | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| VideoContext.exitPictureInPicture | ✔️ |  |  |  |  |  |
| VideoContext.hideStatusBar | ✔️ |  |  |  |  |  |
| VideoContext.pause | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| VideoContext.play | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| VideoContext.playbackRate | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| VideoContext.requestBackgroundPlayback | ✔️ |  |  |  |  | ✔️ |
| VideoContext.requestFullScreen | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| VideoContext.seek | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| VideoContext.sendDanmu | ✔️ |  |  |  |  |  |
| VideoContext.showStatusBar | ✔️ |  |  |  |  |  |
| VideoContext.stop | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
