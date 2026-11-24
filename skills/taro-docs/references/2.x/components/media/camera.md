# Camera

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/components/media/camera)

系统相机

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/camera.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<CameraProps>
```

<a id="cameraprops"></a>

## CameraProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| mode | `"normal" \| "scanCode"` | `"normal"` | 否 | 模式，有效值为normal, scanCode |
| resolution | `"low" \| "medium" \| "high"` | `"medium"` | 否 | 分辨率，不支持动态修改 |
| devicePosition | `"front" \| "back"` | `"back"` | 否 | 摄像头朝向 |
| flash | `"auto" \| "on" \| "off" \| "torch"` | `"auto"` | 否 | 闪光灯 |
| frameSize | `"medium" \| "small" \| "large"` | `"medium"` | 否 | 指定期望的相机帧数据尺寸 |
| scanArea | `number[]` |  | 否 | 扫码识别区域，格式为[x, y, w, h]，<br>x,y是相对于camera显示区域的左上角，<br>w,h为区域宽度，单位px，仅在 mode="scanCode" 时生效 |
| onStop | `BaseEventOrigFunction<any>` |  | 否 | 摄像头在非正常终止时触发，<br>如退出后台等情况 |
| onError | `BaseEventOrigFunction<any>` |  | 否 | 用户不允许使用摄像头时触发 |
| onInitDone | `BaseEventOrigFunction<onInitDoneEventDetail>` |  | 否 | 相机初始化完成时触发 |
| onScanCode | `BaseEventOrigFunction<any>` |  | 否 | 在成功识别到一维码时触发，<br>仅在 mode="scanCode" 时生效 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| CameraProps.mode | ✔️ |  |  |
| CameraProps.resolution | ✔️ |  |  |
| CameraProps.devicePosition | ✔️ |  |  |
| CameraProps.flash | ✔️ |  |  |
| CameraProps.frameSize | ✔️ |  |  |
| CameraProps.scanArea | ✔️ |  |  |
| CameraProps.onStop | ✔️ |  |  |
| CameraProps.onError | ✔️ |  |  |
| CameraProps.onInitDone | ✔️ |  |  |
| CameraProps.onScanCode | ✔️ |  |  |

<a id="mode"></a>

### mode

mode 的合法值

| 参数 | 说明 |
| --- | --- |
| normal | 相机模式 |
| scanCode | 扫码模式 |

<a id="resolution"></a>

### resolution

resolution 的合法值

| 参数 | 说明 |
| --- | --- |
| low | 低 |
| medium | 中 |
| high | 高 |

<a id="deviceposition"></a>

### devicePosition

device-position 的合法值

| 参数 | 说明 |
| --- | --- |
| front | 前置 |
| back | 后置 |

<a id="flash"></a>

### flash

flash 的合法值

| 参数 | 说明 |
| --- | --- |
| auto | 自动 |
| on | 打开 |
| off | 关闭 |
| torch | 常亮 |

<a id="framesize"></a>

### frameSize

frame-size 的合法值

| 参数 | 说明 |
| --- | --- |
| small | 小尺寸帧数据 |
| medium | 中尺寸帧数据 |
| large | 大尺寸帧数据 |

<a id="oninitdoneeventdetail"></a>

### onInitDoneEventDetail

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| maxZoom | `number` | 最大变焦 |

<a id="api-支持度-1"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Camera | ✔️ |  |  |
