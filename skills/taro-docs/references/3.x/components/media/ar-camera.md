# ArCamera

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/media/ar-camera)

AR 相机

支持情况：微信小程序 百度小程序 H5 React Native Harmony

> [参考文档](https://smartprogram.baidu.com/docs/develop/component/media_ar-camera/)

<a id="类型"></a>

## 类型

```tsx
ComponentType<ArCameraProps>
```

<a id="arcameraprops"></a>

## ArCameraProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| key | `string` |  | 否 | AR 项目唯一标识，在 DuMixAR 内容开放平台上传生成 AR 项目后获取 AR Key |
| type | "0" or "5" or "8" |  | 否 | AR 相机类型，在 DuMixAR 内容开放平台上传生成 AR 项目后获取 AR Type：<br>2D 跟踪类型：0<br>SLAM 类型：5<br>IMU 类型：8 |
| flash | "auto" or "on" or "off" | `"off"` | 否 | 闪光灯，值为 auto、on、off |
| onError | `CommonEventFunction` |  | 否 | 用户不允许使用摄像头或扫码失败时触发 |
| onLoad | `CommonEventFunction` |  | 否 | AR 加载成功时触发 |
| onMessage | `CommonEventFunction` |  | 否 | 开发者制作 AR 项目时可自定义按键，用户点击时会收到事件和数据，用户自定义事件格式参见代码示例 2：用户自定义事件 |
| onScanCode | `CommonEventFunction` |  | 否 | 扫描识图结束后触发 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- | --- |
| ArCameraProps.key |  | ✔️ |  |  |  |
| ArCameraProps.type |  | ✔️ |  |  |  |
| ArCameraProps.flash |  | ✔️ |  |  |  |
| ArCameraProps.onError |  | ✔️ |  |  |  |
| ArCameraProps.onLoad |  | ✔️ |  |  |  |
| ArCameraProps.onMessage |  | ✔️ |  |  |  |
| ArCameraProps.onScanCode |  | ✔️ |  |  |  |
