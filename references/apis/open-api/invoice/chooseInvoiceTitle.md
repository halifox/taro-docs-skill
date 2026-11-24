# Taro.chooseInvoiceTitle(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/open-api/invoice/chooseInvoiceTitle)

选择用户的发票抬头。当前小程序必须关联一个公众号，且这个公众号是完成了[微信认证](https://mp.weixin.qq.com/wiki?t=resource/res_main&id=mp1496554031_RD4xe)的，才能调用 chooseInvoiceTitle。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/invoice/wx.chooseInvoiceTitle.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => Promise<SuccessCallbackResult>
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
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| bankAccount | `string` | 银行账号 |
| bankName | `string` | 银行名称 |
| companyAddress | `string` | 单位地址 |
| errMsg | `string` | 错误信息 |
| taxNumber | `string` | 抬头税号 |
| telephone | `string` | 手机号码 |
| title | `string` | 抬头名称 |
| type | `keyof InvoiceType` | 抬头类型 |

<a id="invoicetype"></a>

### InvoiceType

抬头类型

| 参数 | 类型 |
| --- | --- |
| 0 | `"单位"` |
| 1 | `"个人"` |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.chooseInvoiceTitle({
  success: function(res) {}
})
```
