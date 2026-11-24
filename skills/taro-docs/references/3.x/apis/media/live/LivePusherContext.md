# LivePusherContext

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/media/live/LivePusherContext)

`LivePusherContext` 实例，可通过 `Taro.createLivePusherContext` 获取。
`LivePusherContext` 与页面内唯一的 `live-pusher` 组件绑定，操作对应的 `live-pusher` 组件。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.html)

<a id="方法"></a>

## 方法

<a id="pause"></a>

### pause

暂停推流

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.pause.html)

```tsx
(option?: PauseOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `PauseOption` |

<a id="pausebgm"></a>

### pauseBGM

暂停背景音

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.pauseBGM.html)

```tsx
(option?: PauseBGMOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `PauseBGMOption` |

<a id="playbgm"></a>

### playBGM

播放背景音

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.playBGM.html)

```tsx
(option: PlayBGMOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `PlayBGMOption` |

<a id="resume"></a>

### resume

恢复推流

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.resume.html)

```tsx
(option?: ResumeOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `ResumeOption` |

<a id="resumebgm"></a>

### resumeBGM

恢复背景音

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.resumeBGM.html)

```tsx
(option?: ResumeBGMOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `ResumeBGMOption` |

<a id="sendmessage"></a>

### sendMessage

发送SEI消息

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.sendMessage.html)

```tsx
(option?: SendMessageOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `SendMessageOption` |

<a id="setbgmvolume"></a>

### setBGMVolume

设置背景音音量

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.setBGMVolume.html)

```tsx
(option: SetBGMVolumeOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `SetBGMVolumeOption` |

<a id="setmicvolume"></a>

### setMICVolume

设置麦克风音量

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.setMICVolume.html)

```tsx
(option: SetMICVolumeOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `SetMICVolumeOption` |

<a id="snapshot"></a>

### snapshot

快照

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.snapshot.html)

```tsx
(option?: SnapshotOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `SnapshotOption` |

<a id="start"></a>

### start

开始推流，同时开启摄像头预览

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.start.html)

```tsx
(option?: StartOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `StartOption` |

<a id="startpreview"></a>

### startPreview

开启摄像头预览

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.startPreview.html)

```tsx
(option?: StartPreviewOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `StartPreviewOption` |

<a id="stop"></a>

### stop

停止推流，同时停止摄像头预览

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.stop.html)

```tsx
(option?: StopOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `StopOption` |

<a id="stopbgm"></a>

### stopBGM

停止背景音

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.stopBGM.html)

```tsx
(option?: StopBGMOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `StopBGMOption` |

<a id="stoppreview"></a>

### stopPreview

关闭摄像头预览

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.stopPreview.html)

```tsx
(option?: StopPreviewOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `StopPreviewOption` |

<a id="switchcamera"></a>

### switchCamera

切换前后摄像头

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.switchCamera.html)

```tsx
(option?: SwitchCameraOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `SwitchCameraOption` |

<a id="toggletorch"></a>

### toggleTorch

切换手电筒

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePusherContext.toggleTorch.html)

```tsx
(option?: ToggleTorchOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `ToggleTorchOption` |

<a id="参数"></a>

## 参数

<a id="pauseoption"></a>

### PauseOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="pausebgmoption"></a>

### PauseBGMOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="playbgmoption"></a>

### PlayBGMOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| url | `string` | 是 | 加入背景混音的资源地址 |
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

<a id="resumebgmoption"></a>

### ResumeBGMOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="sendmessageoption"></a>

### SendMessageOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| msg | `string` | 是 | SEI消息 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="setbgmvolumeoption"></a>

### SetBGMVolumeOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| volume | `number` | 是 | 音量大小，范围是 0-1 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="setmicvolumeoption"></a>

### SetMICVolumeOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| volume | `number` | 是 | 音量大小，范围是 0-1 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="snapshotoption"></a>

### SnapshotOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="startoption"></a>

### StartOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="startpreviewoption"></a>

### StartPreviewOption

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

<a id="stopbgmoption"></a>

### StopBGMOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="stoppreviewoption"></a>

### StopPreviewOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="switchcameraoption"></a>

### SwitchCameraOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="toggletorchoption"></a>

### ToggleTorchOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| LivePusherContext | ✔️ |  |  |  |  |
| LivePusherContext.pause | ✔️ |  |  |  |  |
| LivePusherContext.pauseBGM | ✔️ |  |  |  |  |
| LivePusherContext.playBGM | ✔️ |  |  |  |  |
| LivePusherContext.resume | ✔️ |  |  |  |  |
| LivePusherContext.resumeBGM | ✔️ |  |  |  |  |
| LivePusherContext.sendMessage | ✔️ |  |  |  |  |
| LivePusherContext.setBGMVolume | ✔️ |  |  |  |  |
| LivePusherContext.setMICVolume | ✔️ |  |  |  |  |
| LivePusherContext.snapshot | ✔️ |  |  |  |  |
| LivePusherContext.start | ✔️ |  |  |  |  |
| LivePusherContext.startPreview | ✔️ |  |  |  |  |
| LivePusherContext.stop | ✔️ |  |  |  |  |
| LivePusherContext.stopBGM | ✔️ |  |  |  |  |
| LivePusherContext.stopPreview | ✔️ |  |  |  |  |
| LivePusherContext.switchCamera | ✔️ |  |  |  |  |
| LivePusherContext.toggleTorch | ✔️ |  |  |  |  |
