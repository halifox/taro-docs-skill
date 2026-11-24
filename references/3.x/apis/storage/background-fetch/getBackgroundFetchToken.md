# Taro.getBackgroundFetchToken(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/storage/background-fetch/getBackgroundFetchToken)

获取设置过的自定义登录态。若无，则返回 fail。

支持情况：微信小程序 QQ 小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/storage/background-fetch/wx.getBackgroundFetchToken.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => Promise<TaroGeneral.CallbackResult>
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
| success | `(res: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| token | `string` | 自定义的登录态 |
| errMsg | `string` | 接口调用结果 |
