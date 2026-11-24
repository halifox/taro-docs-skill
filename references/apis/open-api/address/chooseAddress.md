# Taro.chooseAddress(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/open-api/address/chooseAddress)

获取用户收货地址。调起用户编辑收货地址原生界面，并在编辑完成后返回用户选择的地址。

支持情况：微信小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/address/wx.chooseAddress.html)

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
| complete | `(res: SuccessCallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| userName | `string` | 收货人姓名 |
| postalCode | `string` | 邮编<br>API 支持度: weapp, qq |
| provinceName | `string` | 国标收货地址第一级地址 |
| cityName | `string` | 国标收货地址第二级地址 |
| countyName | `string` | 国标收货地址第三级地址 |
| streetName | `string` | 国标收货地址第四级地址<br>API 支持度: weapp, qq |
| detailInfo | `string` | 详细收货地址信息 |
| detailInfoNew | `string` | 新选择器详细收货地址信息<br>API 支持度: weapp, qq |
| nationalCode | `string` | 收货地址国家码<br>API 支持度: weapp, qq |
| telNumber | `string` | 收货人手机号码 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.chooseAddress({
  success: function (res) {
    console.log(res.userName)
    console.log(res.postalCode)
    console.log(res.provinceName)
    console.log(res.cityName)
    console.log(res.countyName)
    console.log(res.detailInfo)
    console.log(res.nationalCode)
    console.log(res.telNumber)
  }
})
```
