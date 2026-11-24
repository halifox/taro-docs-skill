# Taro.canvasPutImageData(param, componentInstance)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/interface/canvas/canvasPutImageData)

将像素数据绘制到画布。在自定义组件下，第二个参数传入自定义组件实例 this，以操作组件内 <Canvas> 组件。

<a id="参数"></a>

## 参数

<a id="object-param"></a>

### object param

| Name | Type | Description |
| --- | --- | --- |
| canvasId | `String` | 画布标识，传入 <Canvas> 组件的 canvasId 属性。 |
| data | `Uint8ClampedArray` | 图像像素点数据，一维数组，每四项表示一个像素点的 rgba |
| x | `Number` | 源图像数据在目标画布中的位置偏移量（x 轴方向的偏移量） |
| y | `Number` | 源图像数据在目标画布中的位置偏移量（y 轴方向的偏移量） |
| width | `Number` | 源图像数据矩形区域的宽度 |
| height | `Number` | 源图像数据矩形区域的高度 |
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
| Taro.canvasPutImageData | ✔️ | ✔️ |  |
