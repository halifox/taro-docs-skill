# Taro.requestPayment(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/open-api/payment/requestPayment)

发起微信支付。了解更多信息，请查看[微信支付接口文档](https://pay.weixin.qq.com/wiki/doc/api/wxa/wxa_api.php?chapter=7_3&index=1)

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/payment/wx.requestPayment.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<CallbackResult>
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| nonceStr | `string` | 是 | 随机字符串，长度为32个字符以下 |
| package | `string` | 是 | 统一下单接口返回的 prepay\_id 参数值，提交格式如：prepay\_id=\*\*\* |
| paySign | `string` | 是 | 签名，具体签名方案参见 [小程序支付接口文档](https://pay.weixin.qq.com/wiki/doc/api/wxa/wxa_api.php?chapter=7_7&index=3) |
| timeStamp | `string` | 是 | 时间戳，从 1970 年 1 月 1 日 00:00:00 至今的秒数，即当前的时间 |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| signType | `"MD5" \| "HMAC-SHA256"` | 否 | 签名算法 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="signtype"></a>

### signType

| 参数 | 说明 |
| --- | --- |
| MD5 | MD5 |
| HMAC-SHA256 | HMAC-SHA256 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.requestPayment({
  timeStamp: '',
  nonceStr: '',
  package: '',
  signType: 'MD5',
  paySign: '',
  success: function (res) { },
  fail: function (res) { }
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.requestPayment | ✔️ | ✔️ |  |
