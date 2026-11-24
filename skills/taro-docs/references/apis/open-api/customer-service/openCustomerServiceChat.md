# Taro.openCustomerServiceChat(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/open-api/customer-service/openCustomerServiceChat)

打开微信客服。了解更多信息，可以参考微信客服介绍：[https://work.weixin.qq.com/kf/。](https://work.weixin.qq.com/kf/%E3%80%82)

支持情况：微信小程序 H5 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/service-chat/wx.openCustomerServiceChat.html)

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

<a id="extinfo"></a>

### ExtInfo

| 参数 | 类型 |
| --- | --- |
| url | `string` |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| extInfo | `ExtInfo` | 是 | 客服信息 |
| corpId | `string` | 是 | 企业ID |
| showMessageCard | `boolean` | 否 | 是否发送小程序气泡消息，默认值：false |
| sendMessageTitle | `string` | 否 | 气泡消息标题 |
| sendMessagePath | `string` | 否 | 气泡消息小程序路径 |
| sendMessageImg | `string` | 否 | 气泡消息图片 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.openCustomerServiceChat({
  extInfo: {url: ''},
  corpId: '',
  success: function (res) { }
})
```
