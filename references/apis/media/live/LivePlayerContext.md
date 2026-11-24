# LivePlayerContext

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/media/live/LivePlayerContext)

`LivePlayerContext` 实例，可通过 `Taro.createLivePlayerContext` 获取。
`LivePlayerContext` 通过 `id` 跟一个 `live-player` 组件绑定，操作对应的 `live-player` 组件。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.html)

<a id="方法"></a>

## 方法

<a id="exitcasting"></a>

### exitCasting

退出投屏。仅支持在 tap 事件回调内调用。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.exitCasting.html)

```tsx
(option?: ExitCastingOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `ExitCastingOption` |

<a id="exitfullscreen"></a>

### exitFullScreen

退出全屏

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.exitFullScreen.html)

```tsx
(option?: ExitFullScreenOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `ExitFullScreenOption` |

<a id="exitpictureinpicture"></a>

### exitPictureInPicture

退出小窗，该方法可在任意页面调用

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.exitPictureInPicture.html)

```tsx
(option?: ExitPictureInPictureOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `ExitPictureInPictureOption` |

<a id="mute"></a>

### mute

静音

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.mute.html)

```tsx
(option?: MuteOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `MuteOption` |

<a id="pause"></a>

### pause

暂停

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.pause.html)

```tsx
(option?: PauseOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `PauseOption` |

<a id="play"></a>

### play

播放

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.play.html)

```tsx
(option?: PlayOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `PlayOption` |

<a id="reconnectcasting"></a>

### reconnectCasting

重连投屏设备。仅支持在 tap 事件回调内调用。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.reconnectCasting.html)

```tsx
(option?: ReconnectCastingOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `ReconnectCastingOption` |

<a id="requestfullscreen"></a>

### requestFullScreen

进入全屏

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.requestFullScreen.html)

```tsx
(option: RequestFullScreenOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `RequestFullScreenOption` |

<a id="requestpictureinpicture"></a>

### requestPictureInPicture

进入全屏

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.requestPictureInPicture.html)

```tsx
(option: RequestPictureInPictureOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `RequestPictureInPictureOption` |

<a id="resume"></a>

### resume

恢复

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.resume.html)

```tsx
(option?: ResumeOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `ResumeOption` |

<a id="snapshot"></a>

### snapshot

截图

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.snapshot.html)

```tsx
(option?: SnapshotOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `SnapshotOption` |

<a id="startcasting"></a>

### startCasting

开始投屏, 拉起半屏搜索设备。仅支持在 tap 事件回调内调用

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.startCasting.html)

```tsx
(option?: StartCastingOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `StartCastingOption` |

<a id="stop"></a>

### stop

停止

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.stop.html)

```tsx
(option?: StopOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `StopOption` |

<a id="switchcasting"></a>

### switchCasting

切换投屏设备。仅支持在 tap 事件回调内调用。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.switchCasting.html)

```tsx
(option?: SwitchCastingOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `SwitchCastingOption` |

<a id="参数"></a>

## 参数

<a id="exitcastingoption"></a>

### ExitCastingOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="exitfullscreenoption"></a>

### ExitFullScreenOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="exitpictureinpictureoption"></a>

### ExitPictureInPictureOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="muteoption"></a>

### MuteOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="pauseoption"></a>

### PauseOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="playoption"></a>

### PlayOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="reconnectcastingoption"></a>

### ReconnectCastingOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="requestfullscreenoption"></a>

### RequestFullScreenOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| direction | 0 or 90 or -90 | 否 | 设置全屏时的方向<br><br>可选值：<br>- 0: 正常竖向;<br>- 90: 屏幕逆时针90度;<br>- -90: 屏幕顺时针90度; |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="requestpictureinpictureoption"></a>

### RequestPictureInPictureOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="resumeoption"></a>

### ResumeOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="snapshotoption"></a>

### SnapshotOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SnapshotSuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="snapshotsuccesscallbackresult"></a>

### SnapshotSuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| height | `string` | 图片的高度 |
| tempImagePath | `string` | 图片文件的临时路径 |
| width | `string` | 图片的宽度 |
| errMsg | `string` | 调用结果 |

<a id="startcastingoption"></a>

### StartCastingOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="stopoption"></a>

### StopOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="switchcastingoption"></a>

### SwitchCastingOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| LivePlayerContext | ✔️ |  |  |  |  |
| LivePlayerContext.exitCasting | ✔️ |  |  |  |  |
| LivePlayerContext.exitFullScreen | ✔️ |  |  |  |  |
| LivePlayerContext.exitPictureInPicture | ✔️ |  |  |  |  |
| LivePlayerContext.mute | ✔️ |  |  |  |  |
| LivePlayerContext.pause | ✔️ |  |  |  |  |
| LivePlayerContext.play | ✔️ |  |  |  |  |
| LivePlayerContext.reconnectCasting | ✔️ |  |  |  |  |
| LivePlayerContext.requestFullScreen | ✔️ |  |  |  |  |
| LivePlayerContext.requestPictureInPicture | ✔️ |  |  |  |  |
| LivePlayerContext.resume | ✔️ |  |  |  |  |
| LivePlayerContext.snapshot | ✔️ |  |  |  |  |
| LivePlayerContext.startCasting | ✔️ |  |  |  |  |
| LivePlayerContext.stop | ✔️ |  |  |  |  |
| LivePlayerContext.switchCasting | ✔️ |  |  |  |  |
