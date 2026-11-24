# Taro.getOpenUserInfo(Option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/alipay/getOpenUserInfo)

此接口可获取支付宝会员的基础信息（头像图片地址、昵称、性别、国家码、省份、所在市区），接入方法请参考 获取会员基础信息介绍。如需获取支付宝会员标识（user\_id），请调用 my.getAuthCode 和 alipay.system.oauth.token 接口。

支持情况：微信小程序 支付宝小程序 H5 React Native Harmony

> [参考文档](https://docs.alipay.com/mini/api/ch8chh)

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
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| response | `string` | 返回一个 Object 类型的对象 res。使用 JSON.parse(res.response).response 解析 |
