# Login

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/open/login)

联合登录 / 手机号授权内嵌组件

支持情况：微信小程序 百度小程序 H5 React Native Harmony

> [参考文档](https://smartprogram.baidu.com/docs/develop/component/login/)

<a id="类型"></a>

## 类型

```tsx
ComponentType<LoginProps>
```

<a id="loginprops"></a>

## LoginProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| buttonClass | `string` |  | 否 | 组件中用户授权按钮的类名，可用于自定义样式 |
| checkedColor | `string` | `"#3388FF"` | 否 | 组件中用户授权勾选框选中时的颜色，同 CSS 的 color |
| themeColor | `string` | `"#3388FF"` | 否 | 主题颜色，设置后将应用于 “用户授权按钮背景色” 和 “用户授权勾选框选中时的颜色”<br>注：theme-color 的优先级低于 button-class 和 checked-color，且当 button-class 存在时，theme-color 不生效 |
| onGetPhoneNumber | `CommonEventFunction` |  | 否 | 用户完成授权后，获取用户手机号：<br>detail.errMsg 值为"getPhoneNumber:ok" 时代表用户信息获取成功；<br>detail.errMsg 值为"getPhoneNumber:fail auth deny"时代表用户信息获取失败。<br>参考 用户数据的签名验证和加解密 对用户数据进行处理获得用户手机号。<br>用户手机号信息解密后数据示例：{"mobile":"15000000000"}<br>1. 非个人开发者可申请；<br>2. 审核通过后，进入小程序首页,在左侧导航栏单击“设置 -> 开发设置”。下拉页面，在“获取用户手机号权限申请”中单击“申请开通” |
| onLoadError | `CommonEventFunction` |  | 否 | 组件加载失败回调 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- | --- |
| LoginProps.buttonClass |  | ✔️ |  |  |  |
| LoginProps.checkedColor |  | ✔️ |  |  |  |
| LoginProps.themeColor |  | ✔️ |  |  |  |
| LoginProps.onGetPhoneNumber |  | ✔️ |  |  |  |
| LoginProps.onLoadError |  | ✔️ |  |  |  |
