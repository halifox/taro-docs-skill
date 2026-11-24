# InlinePaymentPanel

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/open/inline-payment-panel)

内嵌支付组件

支持情况：微信小程序 百度小程序 H5 React Native Harmony

> [参考文档](https://smartprogram.baidu.com/docs/develop/component/inline_payment_panel/)

<a id="类型"></a>

## 类型

```tsx
ComponentType<InlinePaymentPanelProps>
```

<a id="inlinepaymentpanelprops"></a>

## InlinePaymentPanelProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| totalAmount | `string` |  | 否 | 总金额，金额单位分，tip：仅支持整数型字符串 |
| dealId | `string` |  | 否 | 百度收银台的财务结算凭证，详见平台术语 |
| appKey | `string` |  | 否 | 支付能力开通后分配的支付 appKey，详见平台术语 |
| promotionTag | string or string[] |  | 否 | 平台营销信息，此处传当前订单中可使用平台券的 spuid，同时需在 支付能力中搭配使用传入该参数；注：仅与百度合作平台类目券的开发者需要填写该参数 |
| enablePageBackModal | `boolean` | `false` | 否 | 是否设置挽留弹窗 |
| customStyle | `string` |  | 否 | 自定义样式设置 |
| styleType | "tiny" or "small" or "default" or "medium" or "large" | `"default"` | 否 | 自定义样式档位配置，各档位配置项包括支付渠道/优惠券条高度、渠道图标大小、支付渠道文案字体大小、营销文案字体大小、选择器图标大小 |
| onGetPaymentInfo | `CommonEventFunction` |  | 否 | 获取支付相关信息，具体信息在返回值的 detail 字段中 |
| onError | `CommonEventFunction` |  | 否 | 当发生错误时触发 error 事件，具体信息在返回值的 detail 字段中，例如 {detail: {errMsg: "something is wrong"}} |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- | --- |
| InlinePaymentPanelProps.totalAmount |  | ✔️ |  |  |  |
| InlinePaymentPanelProps.dealId |  | ✔️ |  |  |  |
| InlinePaymentPanelProps.appKey |  | ✔️ |  |  |  |
| InlinePaymentPanelProps.promotionTag |  | ✔️ |  |  |  |
| InlinePaymentPanelProps.enablePageBackModal |  | ✔️ |  |  |  |
| InlinePaymentPanelProps.customStyle |  | ✔️ |  |  |  |
| InlinePaymentPanelProps.styleType |  | ✔️ |  |  |  |
| InlinePaymentPanelProps.onGetPaymentInfo |  | ✔️ |  |  |  |
| InlinePaymentPanelProps.onError |  | ✔️ |  |  |  |
