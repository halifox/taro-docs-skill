# Taro.createRewardedVideoAd(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/ad/createRewardedVideoAd)

创建激励视频广告组件。

支持情况：微信小程序 百度小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/wx.createRewardedVideoAd.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => RewardedVideoAd
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| adUnitId | `string` |  | 是 | 小程序广告位 ID<br>API 支持度: weapp, tt, swan |
| multiton | `boolean` | `false` | 否 | 是否启用多例模式<br>API 支持度: weapp |
| appSid | `string` |  | 否 | 小程序应用 ID<br>API 支持度: swan<br>swan: 必填 |
