# Taro.requestOrderPayment(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/payment/requestOrderPayment)

创建自定义版交易组件订单，并发起支付。 仅接入了[自定义版交易组件](https://developers.weixin.qq.com/miniprogram/dev/framework/ministore/minishopopencomponent2/Introduction2)的小程序需要使用，普通小程序可直接使用 `Taro.requestPayment`。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/payment/wx.requestOrderPayment.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<TaroGeneral.CallbackResult>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| timeStamp | `string` | 是 | 时间戳，从 1970 年 1 月 1 日 00:00:00 至今的秒数，即当前的时间 |
| nonceStr | `string` | 是 | 随机字符串，长度为32个字符以下 |
| package | `string` | 是 | 统一下单接口返回的 prepay\_id 参数值，提交格式如：prepay\_id=\*\*\* |
| orderInfo | `any` | 否 | 订单信息，仅在需要校验的场景下需要传递，具体见[接口说明](https://developers.weixin.qq.com/miniprogram/dev/framework/ministore/minishopopencomponent2/API/order/requestOrderPayment) |
| extUserUin | `string` | 否 | 外部 APP 用户 ID |
| signType | `keyof SignType` | 否 | 签名算法 |
| paySign | `string` | 是 | 签名，具体签名方案参见 [小程序支付接口文档](https://pay.weixin.qq.com/wiki/doc/api/wxa/wxa_api.php?chapter=7_7&index=3) |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="signtype"></a>

### SignType

| 参数 | 说明 |
| --- | --- |
| MD5 | 仅在微信支付 v2 版本接口适用 |
| HMAC-SHA256 | 仅在微信支付 v2 版本接口适用 |
| RSA | 仅在微信支付 v3 版本接口适用 |

<a id="示例代码"></a>

## 示例代码

除 orderInfo 以外，其余字段与 [Taro.requestPayment](requestPayment.md) 一致

```tsx
Taro.requestOrderPayment({
  orderInfo: {},
  timeStamp: '',
  nonceStr: '',
  package: '',
  signType: 'MD5',
  paySign: '',
  success (res) { },
  fail (res) { }
})
```
