# Taro.base64ToArrayBuffer(base64)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/base/base64ToArrayBuffer)

将 Base64 字符串转成 ArrayBuffer 数据。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/wx.base64ToArrayBuffer.html)

<a id="类型"></a>

## 类型

```tsx
(base64: string) => ArrayBuffer
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| base64 | `string` | 要转化成 ArrayBuffer 对象的 Base64 字符串 |

<a id="示例代码"></a>

## 示例代码

```tsx
const base64 = 'CxYh'
const arrayBuffer = Taro.base64ToArrayBuffer(base64)
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.base64ToArrayBuffer | ✔️ | ✔️ |  |
