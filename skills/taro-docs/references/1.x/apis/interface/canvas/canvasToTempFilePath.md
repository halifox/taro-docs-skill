# Taro.canvasToTempFilePath(param, componentInstance)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/interface/canvas/canvasToTempFilePath)

把当前画布指定区域的内容导出生成指定大小的图片。在 draw() 回调里调用该方法才能保证图片导出成功。

<a id="参数"></a>

## 参数

<a id="object-param"></a>

### object param

| Name | Type | Description |
| --- | --- | --- |
| [x] | `Number` | 指定的画布区域的左上角横坐标，默认值 0 |
| [y] | `Number` | 指定的画布区域的左上角纵坐标，默认值 0 |
| [width] | `Number` | 指定的画布区域的宽度，默认值 canvas宽度-x |
| [height] | `Number` | 指定的画布区域的高度，默认值 canvas宽度-y |
| [destWidth] | `Number` | 输出的图片的宽度，默认值 width\*屏幕像素密度 |
| [destHeight] | `Number` | 输出的图片的高度，默认值 height\*屏幕像素密度 |
| canvasId | `String` | 画布标识，传入 <Canvas> 组件的 canvasId |
| [fileType] | `String` | 目标文件的类型，默认值 png |
| quality | `Number` | 图片的质量，目前仅对 jpg 有效。取值范围为 (0, 1]，不在范围内时当作 1.0 处理。 |
| [success] | `function` | 接口调用成功的回调函数 |
| [fail] | `function` | 接口调用失败的回调函数 |
| [complete] | `function` | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="component-componentinstance"></a>

### Component componentInstance

在自定义组件下，当前组件实例的this，以操作组件内 <Canvas> 组件

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.canvasToTempFilePath | ✔️ | ✔️ |  |
