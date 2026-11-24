# FunctionalPageNavigator

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/navig/functional-page-navigator)

仅在插件中有效，用于跳转到插件功能页

支持情况：微信小程序 H5 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/functional-page-navigator.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<FunctionalPageNavigatorProps>
```

<a id="functionalpagenavigatorprops"></a>

## FunctionalPageNavigatorProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| version | `keyof Version` | `"release"` | 否 | 跳转到的小程序版本，有效值 develop（开发版），trial（体验版），release（正式版）；线上版本必须设置为 release |
| name | `keyof Name` |  | 否 | 要跳转到的功能页 |
| args | `object` |  | 否 | 功能页参数，参数格式与具体功能页相关 |
| onSuccess | `CommonEventFunction` |  | 否 | 功能页返回，且操作成功时触发， detail 格式与具体功能页相关 |
| onFail | `CommonEventFunction` |  | 否 | 功能页返回，且操作失败时触发， detail 格式与具体功能页相关 |
| onCancel | `CommonEventFunction` |  | 否 | 因用户操作从功能页返回时触发 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- |
| FunctionalPageNavigatorProps.version | ✔️ |  |  |  |
| FunctionalPageNavigatorProps.name | ✔️ |  |  |  |
| FunctionalPageNavigatorProps.args | ✔️ |  |  |  |
| FunctionalPageNavigatorProps.onSuccess | ✔️ |  |  |  |
| FunctionalPageNavigatorProps.onFail | ✔️ |  |  |  |
| FunctionalPageNavigatorProps.onCancel | ✔️ |  |  |  |

<a id="version"></a>

### Version

version 的合法值

| 参数 | 说明 |
| --- | --- |
| develop | 开发版 |
| trial | 体验版 |
| release | 正式版 |

<a id="name"></a>

### Name

name 的合法值

| 参数 | 说明 |
| --- | --- |
| loginAndGetUserInfo | [用户信息功能页](https://developers.weixin.qq.com/miniprogram/dev/framework/plugin/functional-pages/user-info.html) |
| requestPayment | [支付功能页](https://developers.weixin.qq.com/miniprogram/dev/framework/plugin/functional-pages/request-payment.html) |
| chooseAddress | [收货地址功能页](https://developers.weixin.qq.com/miniprogram/dev/framework/plugin/functional-pages/choose-address.html) |
