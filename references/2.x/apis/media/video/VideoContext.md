# VideoContext

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/video/VideoContext)

<a id="方法"></a>

## 方法

<a id="exitfullscreen"></a>

### exitFullScreen

退出全屏

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.exitFullScreen.html)

```tsx
() => void
```

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| VideoContext.exitFullScreen | ✔️ |  |  |

<a id="hidestatusbar"></a>

### hideStatusBar

隐藏状态栏，仅在iOS全屏下有效

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.hideStatusBar.html)

```tsx
() => void
```

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| VideoContext.hideStatusBar | ✔️ |  |  |

<a id="pause"></a>

### pause

暂停视频

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.pause.html)

```tsx
() => void
```

<a id="api-支持度-2"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| VideoContext.pause | ✔️ |  |  |

<a id="play"></a>

### play

播放视频

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.play.html)

```tsx
() => void
```

<a id="api-支持度-3"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| VideoContext.play | ✔️ |  |  |

<a id="playbackrate"></a>

### playbackRate

设置倍速播放

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.playbackRate.html)

```tsx
(rate: number) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| rate | `number` | 倍率，支持 0.5/0.8/1.0/1.25/1.5，2.6.3 起支持 2.0 倍速 |

<a id="api-支持度-4"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| VideoContext.playbackRate | ✔️ |  |  |

<a id="requestfullscreen"></a>

### requestFullScreen

进入全屏

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.requestFullScreen.html)

```tsx
(option: RequestFullScreenOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `RequestFullScreenOption` |

<a id="api-支持度-5"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| VideoContext.requestFullScreen | ✔️ |  |  |

<a id="seek"></a>

### seek

跳转到指定位置

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.seek.html)

```tsx
(position: number) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| position | `number` | 跳转到的位置，单位 s |

<a id="api-支持度-6"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| VideoContext.seek | ✔️ |  |  |

<a id="senddanmu"></a>

### sendDanmu

发送弹幕

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.sendDanmu.html)

```tsx
(data: Danmu) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | `Danmu` | 弹幕内容 |

<a id="api-支持度-7"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| VideoContext.sendDanmu | ✔️ |  |  |

<a id="showstatusbar"></a>

### showStatusBar

显示状态栏，仅在iOS全屏下有效

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.showStatusBar.html)

```tsx
() => void
```

<a id="api-支持度-8"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| VideoContext.showStatusBar | ✔️ |  |  |

<a id="stop"></a>

### stop

停止视频

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/VideoContext.stop.html)

```tsx
() => void
```

<a id="api-支持度-9"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| VideoContext.stop | ✔️ |  |  |

<a id="参数"></a>

## 参数

<a id="requestfullscreenoption"></a>

### RequestFullScreenOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| direction | `0 \| 90 \| -90` | 否 | 设置全屏时视频的方向，不指定则根据宽高比自动判断。<br><br>可选值：<br>- 0: 正常竖向;<br>- 90: 屏幕逆时针90度;<br>- -90: 屏幕顺时针90度; |

<a id="danmu"></a>

### Danmu

弹幕内容

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| text | `string` | 是 | 弹幕文字 |
| color | `string` | 否 | 弹幕颜色 |

<a id="api-支持度-10"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| VideoContext.exitFullScreen | ✔️ |  |  |
| VideoContext.hideStatusBar | ✔️ |  |  |
| VideoContext.pause | ✔️ |  |  |
| VideoContext.play | ✔️ |  |  |
| VideoContext.playbackRate | ✔️ |  |  |
| VideoContext.requestFullScreen | ✔️ |  |  |
| VideoContext.seek | ✔️ |  |  |
| VideoContext.sendDanmu | ✔️ |  |  |
| VideoContext.showStatusBar | ✔️ |  |  |
| VideoContext.stop | ✔️ |  |  |
