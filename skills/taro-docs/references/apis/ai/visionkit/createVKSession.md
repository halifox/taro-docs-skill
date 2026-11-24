# Taro.createVKSession(version)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/ai/visionkit/createVKSession)

创建 vision kit 会话对象

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/visionkit/wx.createVKSession.html)

<a id="类型"></a>

## 类型

```tsx
(version: keyof IVersion) => VKSession
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

<a id="itrack"></a>

### ITrack

跟踪配置

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| plane | `IPlane` | 平面跟踪配置 |

<a id="iplane"></a>

### IPlane

平面跟踪配置

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| mode | `keyof IPlaneMode` | 平面跟踪配置模式 |

<a id="iplanemode"></a>

### IPlaneMode

平面跟踪配置模式合法值

| 参数 | 说明 |
| --- | --- |
| 1 | 检测横向平面 |
| 2 | 检测纵向平面，只有 v2 版本支持 |
| 3 | 检测横向和纵向平面，只有 v2 版本支持 |
