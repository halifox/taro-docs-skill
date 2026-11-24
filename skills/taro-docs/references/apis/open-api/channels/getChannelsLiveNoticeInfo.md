# Taro.getChannelsLiveNoticeInfo(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/open-api/channels/getChannelsLiveNoticeInfo)

获取视频号直播预告信息

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/channels/wx.getChannelsLiveNoticeInfo.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => Promise<SuccessCallbackResult>
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
| finderUserName | `string` | 是 | 视频号 id，以“sph”开头的id，可在视频号助手获取 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| nonceId | `string` | 是 | 预告 nonceId |
| status | `number` | 是 | 预告状态：0可用 1取消 2已用 |
| startTime | `string` | 是 | 开始时间 |
| headUrl | `string` | 是 | 直播封面 |
| nickname | `string` | 是 | 视频号昵称 |
| reservable | `boolean` | 是 | 是否可预约 |
| otherInfos | `string[]` | 否 | 除最近的一条预告信息外，其他的预告信息列表（注意：每次最多返回按时间戳增序排列的15个预告信息，其中时间最近的那个预告信息会在接口其他的返回参数中展示，其余的预告信息会在该字段中展示）。 |

<a id="status"></a>

### Status

| 参数 | 说明 |
| --- | --- |
| 0 | 可用 |
| 1 | 取消 |
| 2 | 已用 |
