# CameraContext

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/camera/CameraContext)

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/camera/CameraContext.html)

<a id="方法"></a>

## 方法

<a id="startrecord"></a>

### startRecord

开始录像

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/camera/CameraContext.startRecord.html)

```tsx
(option: StartRecordOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `StartRecordOption` |

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| CameraContext.startRecord | ✔️ |  |  |

<a id="stoprecord"></a>

### stopRecord

结束录像

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/camera/CameraContext.stopRecord.html)

```tsx
(option?: StopRecordOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `StopRecordOption` |

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| CameraContext.stopRecord | ✔️ |  |  |

<a id="takephoto"></a>

### takePhoto

拍摄照片

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/camera/CameraContext.takePhoto.html)

```tsx
(option: TakePhotoOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `TakePhotoOption` |

<a id="api-支持度-2"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| CameraContext.takePhoto | ✔️ |  |  |

<a id="oncameraframe"></a>

### onCameraFrame

获取 Camera 实时帧数据

---

注： 使用该接口需同时在 [camera](https://developers.weixin.qq.com/miniprogram/dev/component/camera.html) 组件属性中指定 frame-size。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/camera/CameraContext.onCameraFrame.html)

```tsx
(callback: OnCameraFrameCallback) => CameraFrameListener
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnCameraFrameCallback` | 回调函数 |

<a id="示例代码"></a>

#### 示例代码

```tsx
const context = wx.createCameraContext()
const listener = context.onCameraFrame((frame) => {
  console.log(frame.data instanceof ArrayBuffer, frame.width, frame.height)
})
listener.start()
```

<a id="api-支持度-3"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| CameraContext.onCameraFrame | ✔️ |  |  |

<a id="参数"></a>

## 参数

<a id="startrecordoption"></a>

### StartRecordOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |
| timeoutCallback | `StartRecordTimeoutCallback` | 否 | 超过30s或页面 `onHide` 时会结束录像 |

<a id="startrecordtimeoutcallback"></a>

### StartRecordTimeoutCallback

超过30s或页面 `onHide` 时会结束录像

```tsx
(result: StartRecordTimeoutCallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `StartRecordTimeoutCallbackResult` |

<a id="startrecordtimeoutcallbackresult"></a>

### StartRecordTimeoutCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| tempThumbPath | `string` | 封面图片文件的临时路径 |
| tempVideoPath | `string` | 视频的文件的临时路径 |

<a id="stoprecordoption"></a>

### StopRecordOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: StopRecordSuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="stoprecordsuccesscallbackresult"></a>

### StopRecordSuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| tempThumbPath | `string` | 封面图片文件的临时路径 |
| tempVideoPath | `string` | 视频的文件的临时路径 |
| errMsg | `string` | 调用结果 |

<a id="takephotooption"></a>

### TakePhotoOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| quality | `"high" \| "normal" \| "low"` | 否 | 成像质量 |
| success | `(result: TakePhotoSuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="takephotosuccesscallbackresult"></a>

### TakePhotoSuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| tempImagePath | `string` | 照片文件的临时路径，安卓是jpg图片格式，ios是png |
| errMsg | `string` | 调用结果 |

<a id="oncameraframecallback"></a>

### OnCameraFrameCallback

回调函数

```tsx
(result: OnCameraFrameCallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `OnCameraFrameCallbackResult` |

<a id="oncameraframecallbackresult"></a>

### OnCameraFrameCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | `ArrayBuffer` | 图像像素点数据，一维数组，每四项表示一个像素点的 rgba |
| height | `number` | 图像数据矩形的高度 |
| width | `number` | 图像数据矩形的宽度 |

<a id="quality"></a>

### quality

| 参数 | 说明 |
| --- | --- |
| high | 高质量 |
| normal | 普通质量 |
| low | 低质量 |

<a id="api-支持度-4"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| CameraContext.startRecord | ✔️ |  |  |
| CameraContext.stopRecord | ✔️ |  |  |
| CameraContext.takePhoto | ✔️ |  |  |
| CameraContext.onCameraFrame | ✔️ |  |  |
