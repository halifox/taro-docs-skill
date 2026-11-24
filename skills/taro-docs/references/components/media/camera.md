# Camera

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/media/camera)

系统相机

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony

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
| mode | `keyof Mode` | `"normal"` | 否 | 模式，有效值为normal, scanCode |
| resolution | `keyof Resolution` | `"medium"` | 否 | 分辨率，不支持动态修改 |
| devicePosition | `keyof DevicePosition` | `"back"` | 否 | 摄像头朝向 |
| flash | `keyof Flash` | `"auto"` | 否 | 闪光灯 |
| frameSize | `keyof FrameSize` | `"medium"` | 否 | 指定期望的相机帧数据尺寸 |
| outputDimension | "360P" or "540P" or "720P" or "1080P" or "max" | `"720P"` | 否 | 相机拍照，录制的分辨率。 |
| onStop | `CommonEventFunction` |  | 否 | 摄像头在非正常终止时触发，<br>如退出后台等情况 |
| onError | `CommonEventFunction` |  | 否 | 用户不允许使用摄像头时触发 |
| onInitDone | `CommonEventFunction<onInitDoneEventDetail>` |  | 否 | 相机初始化完成时触发 |
| onReady | `CommonEventFunction<onInitDoneEventDetail>` |  | 否 | 相机初始化成功时触发。 |
| onScanCode | `CommonEventFunction<onScanCodeEventDetail>` |  | 否 | 在成功识别到一维码时触发，<br>仅在 mode="scanCode" 时生效 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | 京东小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| CameraProps.mode | ✔️ |  | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ |  |  |
| CameraProps.resolution | ✔️ |  |  | ✔️ |  |  |  |  |  | ✔️ |
| CameraProps.devicePosition | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ |  | ✔️ |
| CameraProps.flash | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ |  | ✔️ |
| CameraProps.frameSize | ✔️ |  | ✔️ | ✔️ |  |  |  |  |  |  |
| CameraProps.outputDimension |  |  | ✔️ |  |  |  |  |  |  |  |
| CameraProps.onStop | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ |  | ✔️ |
| CameraProps.onError | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ |  | ✔️ |
| CameraProps.onInitDone | ✔️ |  |  | ✔️ |  |  |  | ✔️ |  | ✔️ |
| CameraProps.onReady |  |  | ✔️ |  |  |  |  |  |  |  |
| CameraProps.onScanCode | ✔️ |  | ✔️ | ✔️ | ✔️ |  |  | ✔️ |  |  |

<a id="mode"></a>

### Mode

mode 的合法值

| 参数 | 说明 |
| --- | --- |
| normal | 相机模式 |
| scanCode | 扫码模式 |

<a id="resolution"></a>

### Resolution

resolution 的合法值

| 参数 | 说明 |
| --- | --- |
| low | 低 |
| medium | 中 |
| high | 高 |

<a id="deviceposition"></a>

### DevicePosition

device-position 的合法值

| 参数 | 说明 |
| --- | --- |
| front | 前置 |
| back | 后置 |

<a id="flash"></a>

### Flash

flash 的合法值

| 参数 | 说明 |
| --- | --- |
| auto | 自动 |
| on | 打开 |
| off | 关闭 |
| torch | 常亮 |

<a id="framesize"></a>

### FrameSize

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

<a id="onscancodeeventdetail"></a>

### onScanCodeEventDetail

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| charSet | `string` | 字符集 |
| rawData | `string` | 原始数据 |
| type | `string` | 码类型 |
| result | `string` | 识别结果 |
| fullResult | `string` | 识别结果(完整) |

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | 支付宝小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| onScanCodeEventDetail.rawData | ✔️ |  |  |  |  |  |
| onScanCodeEventDetail.fullResult |  | ✔️ |  |  |  |  |
