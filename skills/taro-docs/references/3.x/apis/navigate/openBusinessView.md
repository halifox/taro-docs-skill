# Taro.openBusinessView(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/navigate/openBusinessView)

商户通过调用订单详情接口打开微信支付分小程序，引导用户查看订单详情（小程序端）

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://pay.weixin.qq.com/wiki/doc/apiv3/apis/chapter6_1_25.shtml)

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

<a id="scoreenableextradata"></a>

### ScoreEnableExtraData

wxpayScoreEnable 业务参数

> [参考文档](https://pay.weixin.qq.com/wiki/doc/apiv3/apis/chapter6_1_9.shtml)

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| apply\_permissions\_token | `string` | 用于跳转到微信侧小程序授权数据,跳转到微信侧小程序传入，有效期为1小时；apply\_permissions\_token可以从[《商户预授权API》](https://pay.weixin.qq.com/wiki/doc/apiv3/apis/chapter6_1_2.shtml)接口的返回参数中获取。<br>示例值：1230000109 |

<a id="scoreusedextradata"></a>

### ScoreUsedExtraData

wxpayScoreUse 业务参数

> [参考文档](https://pay.weixin.qq.com/wiki/doc/apiv3/apis/chapter6_1_13.shtml)

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| mch\_id | `string` | 商户号：微信支付分配的商户号。<br>示例值：1230000109 |
| package | `string` | 可在【创建订单】接口的返回字段package中获取。<br>示例值：XXXXXXXX |
| timestamp | `string` | 时间戳：生成签名时间戳，单位秒。<br>示例值：1530097563 |
| nonce\_str | `string` | 随机字符串：生成签名随机串。由数字、大小写字母组成，长度不超过32位。<br>示例值：zyx53Nkey8o4bHpxTQvd8m7e92nG5mG2 |
| sign\_type | `string` | 签名方式：签名类型，仅支持HMAC-SHA256。<br>示例值：HMAC-SHA256 |
| sign | `string` | 签名：使用字段mch\_id、service\_id、out\_order\_no、timestamp、nonce\_str、sign\_type按照签名生成算法计算得出的签名值。<br>示例值：029B52F67573D7E3BE74904BF9AEA |

<a id="scoredetailextradata"></a>

### ScoreDetailExtraData

wxpayScoreDetail 业务参数

> [参考文档](https://pay.weixin.qq.com/wiki/doc/apiv3/apis/chapter6_1_25.shtml)

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| mch\_id | `string` | 商户号：微信支付分配的商户号。<br>示例值：1230000109 |
| service\_id | `string` | 服务ID<br>示例值：88888888000011 |
| out\_order\_no | `string` | 商户服务订单号：商户系统内部服务订单号（不是交易单号）。<br>示例值：234323JKHDFE1243252 |
| timestamp | `string` | 时间戳：生成签名时间戳，单位秒。<br>示例值：1530097563 |
| nonce\_str | `string` | 随机字符串：生成签名随机串。由数字、大小写字母组成，长度不超过32位。<br>示例值：zyx53Nkey8o4bHpxTQvd8m7e92nG5mG2 |
| sign\_type | `string` | 签名方式：签名类型，仅支持HMAC-SHA256。<br>示例值：HMAC-SHA256 |
| sign | `string` | 签名：使用字段mch\_id、service\_id、out\_order\_no、timestamp、nonce\_str、sign\_type按照签名生成算法计算得出的签名值。<br>示例值：029B52F67573D7E3BE74904BF9AEA |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| businessType | `string` | 是 | 跳转类型：固定配置：wxpayScoreDetail<br>示例值：wxpayScoreDetail<br>memberof: Option |
| extraData | ScoreEnableExtraData or ScoreUsedExtraData or ScoreDetailExtraData | 是 | 业务参数：需要传递给支付分的业务数据 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="示例代码"></a>

## 示例代码

```tsx
if (Taro.openBusinessView) {
  Taro.openBusinessView({
    businessType: 'wxpayScoreDetail',
    extraData: {
      mch_id: '1230000109',
      service_id: '88888888000011',
      out_order_no: '1234323JKHDFE1243252',
      timestamp: '1530097563',
      nonce_str: 'zyx53Nkey8o4bHpxTQvd8m7e92nG5mG2',
      sign_type: 'HMAC-SHA256',
      sign: '029B52F67573D7E3BE74904BF9AEA'
    },
    success() {
      //dosomething
    },
    fail() {
      //dosomething
    },
    complete() {
      //dosomething
    }
  });
} else {
  //引导用户升级微信版本
}
```
