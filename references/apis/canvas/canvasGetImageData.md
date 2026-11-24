# Taro.canvasGetImageData(option, component)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/canvas/canvasGetImageData)

获取 canvas 区域隐含的像素数据。

支持情况：微信小程序 百度小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/canvas/wx.canvasGetImageData.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option, component?: TaroGeneral.IAnyObject) => Promise<SuccessCallbackResult>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| option | `Option` |  |
| component | `TaroGeneral.IAnyObject` | 在自定义组件下，当前组件实例的this，以操作组件内 [canvas](../../components/canvas.md) 组件 |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| canvasId | `string` | 是 | 画布标识，传入 [canvas](../../components/canvas.md) 组件的 `canvas-id` 属性。 |
| height | `number` | 是 | 将要被提取的图像数据矩形区域的高度 |
| width | `number` | 是 | 将要被提取的图像数据矩形区域的宽度 |
| x | `number` | 是 | 将要被提取的图像数据矩形区域的左上角横坐标 |
| y | `number` | 是 | 将要被提取的图像数据矩形区域的左上角纵坐标 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | `Uint8ClampedArray` | 图像像素点数据，一维数组，每四项表示一个像素点的 rgba |
| height | `number` | 图像数据矩形的高度 |
| width | `number` | 图像数据矩形的宽度 |
| errMsg | `string` | 调用结果 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.canvasGetImageData({
  canvasId: 'myCanvas',
  x: 0,
  y: 0,
  width: 100,
  height: 100,
  success: function (res) {
    console.log(res.width) // 100
    console.log(res.height) // 100
    console.log(res.data instanceof Uint8ClampedArray) // true
    console.log(res.data.length) // 100 * 100 * 4
  }
})
```
