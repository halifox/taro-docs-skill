# Taro.scanCode(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/device/scan/scancode)

调起客户端扫码界面，扫码成功后返回对应的结果

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/scan/wx.scanCode.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<SuccessCallbackResult>
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| onlyFromCamera | `boolean` | 否 | 是否只能从相机扫码，不允许从相册选择图片 |
| scanType | `("barCode" \| "qrCode" \| "datamatrix" \| "pdf417")[]` | 否 | 扫码类型 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| charSet | `string` | 所扫码的字符集 |
| path | `string` | 当所扫的码为当前小程序二维码时，会返回此字段，内容为二维码携带的 path |
| rawData | `string` | 原始数据，base64编码 |
| result | `string` | 所扫码的内容 |
| scanType | `"QR_CODE" \| "AZTEC" \| "CODABAR" \| "CODE_39" \| "CODE_93" \| "CODE_128" \| "DATA_MATRIX" \| "EAN_8" \| "EAN_13" \| "ITF" \| "MAXICODE" \| "PDF_417" \| "RSS_14" \| "RSS_EXPANDED" \| "UPC_A" \| "UPC_E" \| "UPC_EAN_EXTENSION" \| "WX_CODE" \| "CODE_25"` | 所扫码的类型 |
| errMsg | `string` | 调用结果 |

<a id="scantype"></a>

### ScanType

扫码类型

| 参数 | 说明 |
| --- | --- |
| barCode | 一维码 |
| qrCode | 二维码 |
| datamatrix | Data Matrix 码 |
| pdf417 | PDF417 条码 |

<a id="qrtype"></a>

### QRType

所扫码的类型

| 参数 | 说明 |
| --- | --- |
| QR\_CODE | 二维码 |
| AZTEC | 一维码 |
| CODABAR | 一维码 |
| CODE\_39 | 一维码 |
| CODE\_93 | 一维码 |
| CODE\_128 | 一维码 |
| DATA\_MATRIX | 二维码 |
| EAN\_8 | 一维码 |
| EAN\_13 | 一维码 |
| ITF | 一维码 |
| MAXICODE | 一维码 |
| PDF\_417 | 二维码 |
| RSS\_14 | 一维码 |
| RSS\_EXPANDED | 一维码 |
| UPC\_A | 一维码 |
| UPC\_E | 一维码 |
| UPC\_EAN\_EXTENSION | 一维码 |
| WX\_CODE | 二维码 |
| CODE\_25 | 一维码 |

<a id="示例代码"></a>

## 示例代码

```tsx
// 允许从相机和相册扫码
Taro.scanCode({
  success: (res) => {
    console.log(res)
  }
})
      // 只允许从相机扫码
Taro.scanCode({
  onlyFromCamera: true,
  success: (res) => {
    console.log(res)
  }
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.scanCode | ✔️ | ✔️ |  |
