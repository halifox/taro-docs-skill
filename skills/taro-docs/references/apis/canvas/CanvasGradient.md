# CanvasGradient

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/canvas/CanvasGradient)

创建 canvas 的绘图上下文 CanvasContext 对象

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/canvas/CanvasGradient.html)

<a id="方法"></a>

## 方法

<a id="addcolorstop"></a>

### addColorStop

添加颜色的渐变点。小于最小 stop 的部分会按最小 stop 的 color 来渲染，大于最大 stop 的部分会按最大 stop 的 color 来渲染

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/canvas/CanvasGradient.addColorStop.html)

```tsx
(stop: number, color: string) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| stop | `number` | 表示渐变中开始与结束之间的位置，范围 0-1。 |
| color | `string` | 渐变点的颜色。 |

<a id="示例代码"></a>

#### 示例代码

```tsx
const ctx = Taro.createCanvasContext('myCanvas')
// Create circular gradient
const grd = ctx.createLinearGradient(30, 10, 120, 10)
grd.addColorStop(0, 'red')
grd.addColorStop(0.16, 'orange')
grd.addColorStop(0.33, 'yellow')
grd.addColorStop(0.5, 'green')
grd.addColorStop(0.66, 'cyan')
grd.addColorStop(0.83, 'blue')
grd.addColorStop(1, 'purple')
// Fill with gradient
ctx.setFillStyle(grd)
ctx.fillRect(10, 10, 150, 80)
ctx.draw()
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | 京东小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| CanvasGradient | ✔️ |  |  |  |  |  |  |  |  | ✔️ |
| CanvasGradient.addColorStop | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  |  |  | ✔️ |
