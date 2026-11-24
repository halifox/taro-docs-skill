# Taro.onNeedPrivacyAuthorization(listener)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/open-api/privacy/onNeedPrivacyAuthorization)

监听隐私接口需要用户授权事件。当需要用户进行隐私授权时会触发。触发该事件时，开发者需要弹出隐私协议说明，并在用户同意或拒绝授权后调用回调接口 resolve 触发原隐私接口或组件继续执行。隐私合规开发指南详情可见《小程序隐私协议开发指南》

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/privacy/wx.onNeedPrivacyAuthorization.html)

<a id="类型"></a>

## 类型

```tsx
(listener: Listener) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| listener | `Listener` |

<a id="resolveoption"></a>

### ResolveOption

resolve 是 onNeedPrivacyAuthorization 的回调参数，是一个接口函数。
当触发 needPrivacyAuthorization 事件时，触发该事件的隐私接口或组件会处于 pending 状态。
如果调用 resolve({ buttonId: 'disagree-btn'， event:'agree' })，则触发当前 needPrivacyAuthorization 事件的原隐私接口或组件会继续执行。其中 buttonId 为隐私同意授权按钮的id，为确保用户有同意的操作，基础库会检查对应的同意按钮是否被点击过。
如果调用 resolve({ event: 'disagree' })，则触发当前 needPrivacyAuthorization 事件的原隐私接口或组件会失败并返回 API:fail privacy permission is not authorized 的错误信息。
在调用 resolve({ event: 'agree'/'disagree' }) 之前，开发者可以调用 resolve({ event: 'exposureAuthorization' }) 把隐私弹窗曝光告知平台。

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| event | "exposureAuthorization" or "agree" or "disagree" | 是 | 用户操作类型 |
| buttonId | `string` | 否 | 同意授权按钮的id （仅event=agree时必填） |

<a id="eventinfo"></a>

### EventInfo

触发本次 onNeedPrivacyAuthorization 事件的关联信息

| 参数 | 类型 |
| --- | --- |
| referrer | `string` |

<a id="listener"></a>

### Listener

隐私授权监听函数

```tsx
(resolve: (option: ResolveOption) => void,eventInfo: EventInfo) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| resolve | `(option: ResolveOption) => void` | 事件回调函数 |
| eventInfo | `EventInfo` | 关联事件信息 |
