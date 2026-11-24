# Taro.canvasGetImageData(param, componentInstance)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/interface/canvas/canvasGetImageData)

获取 canvas 区域隐含的像素数据。

<a id="参数"></a>

## 参数

<a id="object-param"></a>

### object param

| Name | Type | Description |
| --- | --- | --- |
| canvasId | `String` | 画布标识，传入 <Canvas> 组件的 canvasId 属性。 |
| x | `Number` | 将要被提取的图像数据矩形区域的左上角横坐标 |
| y | `Number` | 将要被提取的图像数据矩形区域的左上角纵坐标 |
| width | `Number` | 将要被提取的图像数据矩形区域的宽度 |
| height | `Number` | 将要被提取的图像数据矩形区域的高度 |
| [success] | `function` | 接口调用成功的回调函数 |
| [fail] | `function` | 接口调用失败的回调函数 |
| [complete] | `function` | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="component-componentinstance"></a>

### Component componentInstance

在自定义组件下，当前组件实例的this，以操作组件内的 <Canvas> 组件。

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.canvasGetImageData | ✔️ | ✔️ |  |
