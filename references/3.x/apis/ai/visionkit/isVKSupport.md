# Taro.isVKSupport(version)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/ai/visionkit/isVKSupport)

判断支持版本

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/visionkit/wx.isVKSupport.html)

<a id="类型"></a>

## 类型

```tsx
(version: keyof IVersion) => boolean
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| version | `keyof IVersion` |

<a id="iversion"></a>

### IVersion

vision kit 版本

| 参数 | 说明 |
| --- | --- |
| v1 | 旧版本 |
| v2 | v2 版本，目前只有 iOS 基础库 2.22.0 以上支持 |
