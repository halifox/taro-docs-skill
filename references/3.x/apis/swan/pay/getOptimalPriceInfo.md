# Taro.getOptimalPriceInfo(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/swan/pay/getOptimalPriceInfo)

获取商品使用百度平台券后的价格
通过百度收银台支付的商品，用户在支付时可以享受百度平台券提供的优惠。
使用 API swan.getOptimalPriceInfo 可以提前获知用户在支付时享受的优惠价格。（当用户有多张平台券时，按照平台最优优惠价格计算，与支付时默认选中的优惠券对应的优惠一致）

支持情况：微信小程序 百度小程序 H5 React Native Harmony

> [参考文档](https://smartprogram.baidu.com/docs/develop/api/open/payment_swan-getOptimalPriceInfo/)

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
| productsInfo | `ProductInfo[]` | 是 | 商品信息 |
| success | `(res: SuccessCallbackResult) => any` | 否 | 接口调用成功的回调函数 |
| fail | `(err: TaroGeneral.CallbackResult) => any` | 否 | 接口调用失败的回调函数 |

<a id="productinfo"></a>

### ProductInfo

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| appKey | `string` | 支付的 appKey |
| products | `Product[]` | 商品信息 |

<a id="product"></a>

### Product

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| amount | `number` | 是 | 商品单价(原价) |
| promotionTag | `string` | 否 | 商品标识 |
| productId | `string` | 是 | 开发者自定义商品 ID，在success回调中，会与减免信息一起返回。 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| productsInfo | `ProductInfoSuccess[]` | 商品信息 |

<a id="productinfosuccess"></a>

### ProductInfoSuccess

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| appKey | `string` | 支付的 appKey |
| products | `ProductSuccess[]` | 减免后的商品信息 |

<a id="productsuccess"></a>

### ProductSuccess

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| amount | `number` | 商品单价(原价) |
| productId | `string` | 开发者自定义商品 ID |
| promotionTag | `string` | 商品标识 |
| reduceAmount | `number` | 百度平台券减免金额 |
| afterPayAmount | `number` | 百度平台券减免后金额 |
