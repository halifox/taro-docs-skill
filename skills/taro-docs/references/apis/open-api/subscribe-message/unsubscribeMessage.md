# Taro.unsubscribeMessage(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/open-api/subscribe-message/unsubscribeMessage)

取消当前用户已订阅的消息

支持情况：微信小程序 支付宝小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://opendocs.alipay.com/mini/07vg26?pathHash=8c9630ac)

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
| entityIds | `string[]` | 是 | 需要取消订阅的消息模板 id 集合（注意：1、一次性模板 id 和长期性模板 id 不可同时使用，2、一次最多传入三个模板 id）。 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.unsubscribeMessage({
  entityIds: [
    'ac768fca1ce245ccae9404bb5243c49b',
    '9aa357acb7c6434aba294aded1cdfb7c',
  ],
  success(res) {
    console.log(res);
  },
  fail(err) {
    console.log(err);
  }
})
```
