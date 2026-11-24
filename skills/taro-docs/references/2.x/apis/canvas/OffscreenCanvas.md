# OffscreenCanvas

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/canvas/OffscreenCanvas)

离屏 canvas 实例，可通过 Taro.createOffscreenCanvas 创建。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/canvas/OffscreenCanvas.html)

<a id="方法"></a>

## 方法

<a id="getcontext"></a>

### getContext

该方法返回 OffscreenCanvas 的绘图上下文

---

当前仅支持获取 WebGL 绘图上下文

```tsx
(contextType: string) => RenderingContext
```

| 参数 | 类型 |
| --- | --- |
| contextType | `string` |

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| OffscreenCanvas.getContext | ✔️ |  |  |

<a id="api-支持度-1"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| OffscreenCanvas.getContext | ✔️ |  |  |
