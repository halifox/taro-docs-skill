# Taro.createCanvasContext(canvasId, component)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/canvas/createCanvasContext)

创建 canvas 的绘图上下文 [CanvasContext](../../../apis/canvas/CanvasContext.md) 对象

**Tip**: 需要指定 canvasId，该绘图上下文只作用于对应的 `<canvas/>`；另外，Web 端需要在 `useReady` 回调中执行它，否则会因为底层 canvas 渲染出来之前而去获取 CanvasContext，导致其底层的 context 为 `undefined`，从而不能正常绘图。

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/canvas/wx.createCanvasContext.html)

<a id="类型"></a>

## 类型

```tsx
(canvasId: string, component?: TaroGeneral.IAnyObject) => CanvasContext
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| canvasId | `string` | 要获取上下文的 [canvas](../../../components/canvas.md) 组件 canvas-id 属性 |
| component | `TaroGeneral.IAnyObject` | 在自定义组件下，当前组件实例的this，表示在这个自定义组件下查找拥有 canvas-id 的 [canvas](../../../components/canvas.md) ，如果省略则不在任何自定义组件内查找 |

<a id="示例代码"></a>

## 示例代码

```tsx
import { useReady } from '@tarojs/taro'

useReady(() => {
  const context = Taro.createCanvasContext('canvas')
  context.setStrokeStyle("#00ff00")
  context.setLineWidth(5)
  context.rect(0, 0, 200, 200)
  context.stroke()
  context.setStrokeStyle("#ff0000")
  context.setLineWidth(2)
  context.moveTo(160, 100)
  context.arc(100, 100, 60, 0, 2 * Math.PI, true)
  context.moveTo(140, 100)
  context.arc(100, 100, 40, 0, Math.PI, false)
  context.moveTo(85, 80)
  context.arc(80, 80, 5, 0, 2 * Math.PI, true)
  context.moveTo(125, 80)
  context.arc(120, 80, 5, 0, 2 * Math.PI, true)
  context.stroke()
  context.draw()
})
```
