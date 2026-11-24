# SubscriptionsSetting

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/open-api/settings/SubscriptionsSetting)

订阅消息设置

注意事项

- itemSettings 只返回用户勾选过订阅面板中的“总是保持以上选择，不再询问”的订阅消息。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/setting/SubscriptionsSetting.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| mainSwitch | `boolean` | 订阅消息总开关，true 为开启，false 为关闭 |
| itemSettings | `{ [TEMPLATE_ID: string]: string; }` | 每一项订阅消息的订阅状态。itemSettings对象的键为一次性订阅消息的模板id或系统订阅消息的类型<br>- 一次性订阅消息使用方法详见 [Taro.requestSubscribeMessage](../../../../apis/open-api/subscribe-message/requestSubscribeMessage.md)<br>- 永久订阅消息（仅小游戏可用）使用方法详见 [Taro.requestSubscribeSystemMessage](https://developers.weixin.qq.com/minigame/dev/api/open-api/subscribe-message/wx.requestSubscribeSystemMessage.html) |

<a id="参数"></a>

## 参数

<a id="templatereflex"></a>

### TemplateReflex

模版消息订阅类型

| 参数 | 说明 |
| --- | --- |
| accept | 表示用户同意订阅该条id对应的模板消息 |
| reject | 表示用户拒绝订阅该条id对应的模板消息 |
| ban | 表示已被后台封禁 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getSetting({
  withSubscriptions: true,
  success (res) {
    console.log(res.authSetting)
    // res.authSetting = {
    //   "scope.userInfo": true,
    //   "scope.userLocation": true
    // }
    console.log(res.subscriptionsSetting)
    // res.subscriptionsSetting = {
    //   mainSwitch: true, // 订阅消息总开关
    //   itemSettings: {   // 每一项开关
    //     SYS_MSG_TYPE_INTERACTIVE: 'accept', // 小游戏系统订阅消息
    //     SYS_MSG_TYPE_RANK: 'accept'
    //     zun-LzcQyW-edafCVvzPkK4de2Rllr1fFpw2A_x0oXE: 'reject', // 普通一次性订阅消息
    //     ke_OZC_66gZxALLcsuI7ilCJSP2OJ2vWo2ooUPpkWrw: 'ban',
    //   }
    // }
  }
})
```
