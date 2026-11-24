# Taro.tradePay(Option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/alipay/tradePay)

此接口是用于发起支付的 API，此 API 暂仅支持企业支付宝小程序使用

支持情况：微信小程序 支付宝小程序 H5 React Native Harmony

> [参考文档](https://opendocs.alipay.com/mini/api/openapi-pay)

<a id="类型"></a>

## 类型

```tsx
(Option: Option) => Promise<SuccessCallbackResult>
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| tradeNO | `string` | 否 | 接入小程序支付时传入此参数。此参数为支付宝交易号，注意参数有大小写区分（调用 小程序支付 时必填） |
| orderStr | `string` | 否 | 完整的支付参数拼接成的字符串，从服务端获取（调用 支付宝预授权 时必填） |
| success | `(res: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="resultcode"></a>

### ResultCode

| 参数 | 说明 |
| --- | --- |
| 4 | 无权限调用（N22104） |
| 9000 | 订单处理成功 |
| 8000 | 正在处理中。支付结果未知（有可能已经支付成功） |
| 4000 | 订单处理失败 |
| 6001 | 用户中途取消 |
| 6002 | 网络连接出错 |
| 6004 | 处理结果未知（有可能已经成功） |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| response | `{ resultCode: ResultCode; }` | success 回调函数会携带一个 Object 类型的对象，其属性如下： |
