# Taro.getSystemRiskInfo(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/swan/getSystemRiskInfo)

获取用于得到风控信息的加密信息对象。更多小程序风控能力参见[风控服务](https://smartprogram.baidu.com/docs/develop/serverapi/open_risk_power/)。
Web 态说明：Web 态小程序暂不支持获取用于得到风控信息的加密信息对象。

支持情况：微信小程序 百度小程序 H5 React Native Harmony

> [参考文档](https://smartprogram.baidu.com/docs/develop/api/open/swan-getSystemRiskInfo/)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => void
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
| success | `(res: SuccessCallbackResult) => any` | 否 | 接口调用成功的回调函数 |
| fail | `(err: any) => any` | 否 | 接口调用失败的回调函数 |
| complete | `(res: any) => any` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| content | `Object` | 用于获取风控信息的加密信息对象。<br>要获取风控信息，需要和[风控检测](https://smartprogram.baidu.com/docs/develop/serverapi/open_risk_power/#detectrisk/)接口联合使用，并作为风控检测接口的 xtoken 参数传入。 |

<a id="icontent"></a>

### IContent

| 参数 | 类型 |
| --- | --- |
| key | `string` |
| value | `string` |
