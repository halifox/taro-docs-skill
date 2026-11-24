# Taro.getAppInfo()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/taro.extend/getAppInfo)

小程序获取和 Taro 相关的 App 信息

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

<a id="类型"></a>

## 类型

```tsx
() => AppInfo
```

<a id="参数"></a>

## 参数

<a id="appinfo"></a>

### AppInfo

应用信息

| 参数 | 类型 |
| --- | --- |
| platform | `string` |
| taroVersion | `string` |
| designWidth | number or ((size?: string or number) => number) |
