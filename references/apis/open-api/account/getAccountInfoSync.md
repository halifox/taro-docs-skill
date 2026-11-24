# Taro.getAccountInfoSync()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/open-api/account/getAccountInfoSync)

获取当前帐号信息

支持情况：微信小程序 支付宝小程序 QQ 小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/account-info/wx.getAccountInfoSync.html)

<a id="类型"></a>

## 类型

```tsx
() => AccountInfo
```

<a id="参数"></a>

## 参数

<a id="accountinfo"></a>

### AccountInfo

帐号信息

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| miniProgram | `MiniProgram` | 小程序帐号信息 |
| plugin | `Plugin` | 插件帐号信息（仅在插件中调用时包含这一项） |

<a id="miniprogram"></a>

### MiniProgram

小程序帐号信息

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| appId | `string` | 小程序 appId |
| envVersion | "develop" or "trial" or "release" | 小程序版本<br>since: 2.10.0 |
| version | `string` | 线上小程序版本号<br>since: 2.10.2 |

<a id="plugin"></a>

### Plugin

插件帐号信息（仅在插件中调用时包含这一项）

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| appId | `string` | 插件 appId |
| version | `string` | 插件版本号 |

<a id="示例代码"></a>

## 示例代码

```tsx
const accountInfo = Taro.getAccountInfoSync();

console.log(accountInfo.miniProgram.appId) // 小程序 appId
console.log(accountInfo.plugin.appId) // 插件 appId
console.log(accountInfo.plugin.version) // 插件版本号， 'a.b.c' 这样的形式
```
