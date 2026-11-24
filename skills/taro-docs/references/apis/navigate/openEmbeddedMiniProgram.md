# Taro.openEmbeddedMiniProgram(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/navigate/openEmbeddedMiniProgram)

打开半屏小程序。接入指引请参考 [半屏小程序能力](https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/openEmbeddedMiniProgram.html)。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/navigate/wx.openEmbeddedMiniProgram.html)

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

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| appId | `string` | 否 | 要打开的小程序 appId |
| path | `string` | 否 | 打开的页面路径，如果为空则打开首页。path 中 ? 后面的部分会成为 query，在小程序的 `App.onLaunch`、`App.onShow` 和 `Page.onLoad` 的回调函数或小游戏的 [Taro.onShow](openEmbeddedMiniProgram.md) 回调函数、[Taro.getLaunchOptionsSync](../base/weapp/life-cycle/getLaunchOptionsSync.md) 中可以获取到 query 数据。对于小游戏，可以只传入 query 部分，来实现传参效果，如：传入 "?foo=bar"。 |
| extraData | `TaroGeneral.IAnyObject` | 否 | 需要传递给目标小程序的数据，目标小程序可在 `App.onLaunch`，`App.onShow` 中获取到这份数据。如果跳转的是小游戏，可以在 [Taro.onShow](openEmbeddedMiniProgram.md)、[Taro.getLaunchOptionsSync](../base/weapp/life-cycle/getLaunchOptionsSync.md) 中可以获取到这份数据数据。 |
| envVersion | `keyof EnvVersion` | 否 | 要打开的小程序版本。仅在当前小程序为开发版或体验版时此参数有效。如果当前小程序是正式版，则打开的小程序必定是正式版。 |
| shortLink | `string` | 否 | 小程序链接，当传递该参数后，可以不传 appId 和 path。链接可以通过【小程序菜单】->【复制链接】获取。 |
| verify | `keyof Verify` | 否 | 校验方式 。默认为binding |
| noRelaunchIfPathUnchanged | `boolean` | 否 | 不 reLaunch 目标小程序，直接打开目标跳转的小程序退后台时的页面，需满足以下条件：1. 目标跳转的小程序生命周期未被销毁；2. 且目标当次启动的path、query、apiCategory与上次启动相同。默认值为 false 。 |
| allowFullScreen | `boolean` | 否 | 打开的小程序是否支持全屏 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="verify"></a>

### Verify

| 参数 | 说明 |
| --- | --- |
| binding | 校验小程序管理后台的绑定关系 |
| unionProduct | 校验目标打开链接是否为小程序联盟商品。 |

<a id="envversion"></a>

### EnvVersion

| 参数 | 说明 |
| --- | --- |
| develop | 开发版 |
| trial | 体验版 |
| release | 正式版 |
