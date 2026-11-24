# Taro.arrayBufferToBase64(buffer)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/base/arrayBufferToBase64)

将 ArrayBuffer 数据转成 Base64 字符串。

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/wx.arrayBufferToBase64.html)

<a id="类型"></a>

## 类型

```tsx
(buffer: ArrayBuffer) => string
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| buffer | `ArrayBuffer` | 要转换成 Base64 字符串的 ArrayBuffer 对象 |

<a id="示例代码"></a>

## 示例代码

```tsx
const arrayBuffer = new Uint8Array([11, 22, 33])
const base64 = Taro.arrayBufferToBase64(arrayBuffer)
```
