# CameraFrameListener

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/camera/CameraFrameListener)

CameraContext.onCameraFrame() 返回的监听器。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/camera/CameraFrameListener.html)

<a id="方法"></a>

## 方法

<a id="start"></a>

### start

开始监听帧数据

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/camera/CameraFrameListener.start.html)

```tsx
(option?: StartOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `StartOption` |

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| CameraFrameListener.start | ✔️ |  |  |

<a id="stop"></a>

### stop

停止监听帧数据

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/camera/CameraFrameListener.stop.html)

```tsx
(option?: StopOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `StopOption` |

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| CameraFrameListener.stop | ✔️ |  |  |

<a id="参数"></a>

## 参数

<a id="startoption"></a>

### StartOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="stopoption"></a>

### StopOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="api-支持度-2"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| CameraFrameListener.start | ✔️ |  |  |
| CameraFrameListener.stop | ✔️ |  |  |
