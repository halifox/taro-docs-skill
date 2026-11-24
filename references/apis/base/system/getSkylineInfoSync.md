# Taro.getSkylineInfoSync()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/base/system/getSkylineInfoSync)

获取当前运行环境对于 Skyline 渲染引擎 的支持情况
基础库 2.26.2 开始支持

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/system/wx.getSkylineInfoSync.html)

<a id="类型"></a>

## 类型

```tsx
() => Result
```

<a id="参数"></a>

## 参数

<a id="result"></a>

### Result

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| isSupported | `boolean` | 是 | 当前运行环境是否支持 Skyline 渲染引擎 |
| version | `string` | 是 | 当前运行环境 Skyline 渲染引擎 的版本号，形如 0.9.7 |
| reason | `string` | 否 | 当前运行环境不支持 Skyline 渲染引擎 的原因，仅在 isSupported 为 false 时出现 |
