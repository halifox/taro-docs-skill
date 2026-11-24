# OffscreenCanvas

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/canvas/OffscreenCanvas)

离屏 canvas 实例，可通过 Taro.createOffscreenCanvas 创建。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/canvas/OffscreenCanvas.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| width | `number` | 画布宽度 |
| height | `number` | 画布高度 |

<a id="createimage"></a>

### createImage

创建一个图片对象。支持在 2D Canvas 和 WebGL Canvas 下使用, 但不支持混用 2D 和 WebGL 的方法

> 注意不允许混用 webgl 和 2d 画布创建的图片对象，使用时请注意尽量使用 canvas 自身的 createImage 创建图片对象。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/canvas/OffscreenCanvas.createImage.html)

```tsx
() => Image
```

<a id="getcontext"></a>

### getContext

该方法返回 OffscreenCanvas 的绘图上下文

> 当前仅支持获取 WebGL 绘图上下文

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/canvas/OffscreenCanvas.getContext.html)

```tsx
(contextType: "webgl" | "2d") => RenderingContext
```

| 参数 | 类型 |
| --- | --- |
| contextType | "webgl" or "2d" |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | 抖音小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| OffscreenCanvas | ✔️ |  |  |  |  |  |
| OffscreenCanvas.createImage | ✔️ |  |  |  |  |  |
| OffscreenCanvas.getContext | ✔️ | ✔️ |  |  |  |  |
