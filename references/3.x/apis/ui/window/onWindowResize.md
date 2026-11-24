# Taro.onWindowResize(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/ui/window/onWindowResize)

监听窗口尺寸变化事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/window/wx.onWindowResize.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 窗口尺寸变化事件的回调函数 |

<a id="callback"></a>

### Callback

窗口尺寸变化事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="callbackresult"></a>

### CallbackResult

| 参数 | 类型 |
| --- | --- |
| size | `Size` |

<a id="size"></a>

### Size

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| windowHeight | `number` | 变化后的窗口高度，单位 px |
| windowWidth | `number` | 变化后的窗口宽度，单位 px |
