# Taro.addCard(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/open-api/card/addCard)

批量添加卡券。只有通过 [认证](https://developers.weixin.qq.com/miniprogram/product/renzheng.html) 的小程序或文化互动类目的小游戏才能使用。更多文档请参考 [微信卡券接口文档](https://mp.weixin.qq.com/cgi-bin/announce?action=getannouncement&key=1490190158&version=1&lang=zh_CN&platform=2)。

**cardExt 说明**
cardExt 是卡券的扩展参数，其值是一个 JSON 字符串。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/card/wx.addCard.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<SuccessCallbackResult>
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
| cardList | `RequestInfo[]` | 是 | 需要添加的卡券列表 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="requestinfo"></a>

### RequestInfo

需要添加的卡券列表

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| cardExt | `string` | 卡券的扩展参数。需将 CardExt 对象 JSON 序列化为**字符串**传入 |
| cardId | `string` | 卡券 ID |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| cardList | `AddCardResponseInfo[]` | 卡券添加结果列表 |
| errMsg | `string` | 调用结果 |

<a id="addcardresponseinfo"></a>

### AddCardResponseInfo

卡券添加结果列表

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| cardExt | `string` | 卡券的扩展参数，结构请参考下文 |
| cardId | `string` | 用户领取到卡券的 ID |
| code | `string` | 加密 code，为用户领取到卡券的code加密后的字符串，解密请参照：[code 解码接口](https://mp.weixin.qq.com/wiki?t=resource/res_main&id=mp1499332673_Unm7V) |
| isSuccess | `boolean` | 是否成功 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.addCard({
  cardList: [
    {
      cardId: '',
      cardExt: '{"code": "", "openid": "", "timestamp": "", "signature":""}'
    }, {
      cardId: '',
      cardExt: '{"code": "", "openid": "", "timestamp": "", "signature":""}'
    }
  ],
  success: function (res) {
    console.log(res.cardList) // 卡券添加结果
  }
})
```
