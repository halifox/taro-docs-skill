# Taro.createInterstitialAd(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/ad/createInterstitialAd)

创建插屏广告组件。
请通过 getSystemInfoSync 返回对象的 SDKVersion 判断基础库版本号后再使用该 API。每次调用该方法创建插屏广告都会返回一个全新的实例（小程序端的插屏广告实例不允许跨页面使用）。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/wx.createInterstitialAd.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => InterstitialAd
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| adUnitId | `string` | 广告单元 id |
