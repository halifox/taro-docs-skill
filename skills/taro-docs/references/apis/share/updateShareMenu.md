# Taro.updateShareMenu(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/share/updateShareMenu)

更新转发属性

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/share/wx.updateShareMenu.html)

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

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| activityId | `string` | 否 | 动态消息的 activityId。通过 [updatableMessage.createActivityId](https://developers.weixin.qq.com/miniprogram/dev/api-backend/open-api/updatable-message/updatableMessage.createActivityId.html) 接口获取 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| isUpdatableMessage | `boolean` | 否 | 是否是动态消息，详见[动态消息](https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/share/updatable-message.html) |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |
| templateInfo | `UpdatableMessageFrontEndTemplateInfo` | 否 | 动态消息的模板信息 |
| withShareTicket | `boolean` | 否 | 是否使用带 shareTicket 的转发[详情](https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/share.html) |

<a id="updatablemessagefrontendtemplateinfo"></a>

### UpdatableMessageFrontEndTemplateInfo

动态消息的模板信息

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| parameterList | `UpdatableMessageFrontEndParameter[]` | 参数列表 |

<a id="updatablemessagefrontendparameter"></a>

### UpdatableMessageFrontEndParameter

参数列表

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| name | `string` | 参数名 |
| value | `string` | 参数值 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.updateShareMenu({
  withShareTicket: true,
  success () { }
})
```
