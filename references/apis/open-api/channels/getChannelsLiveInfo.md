# Taro.getChannelsLiveInfo(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/open-api/channels/getChannelsLiveInfo)

获取视频号直播信息

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/channels/wx.getChannelsLiveInfo.html)

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
| feedId | `string` | 是 | 直播 feedId |
| nonceId | `string` | 是 | 直播 nonceId |
| description | `string` | 是 | 直播主题 |
| status | `number` | 是 | 直播状态，2直播中，3直播结束 |
| headUrl | `string` | 是 | 视频号头像 |
| nickname | `string` | 是 | 视频号昵称 |
| replayStatus | `number` | 是 | 直播回放状态 |
| otherInfos | `string[]` | 否 | 除最近的一条直播外，其他的直播列表（注意：每次最多返回按时间戳增序排列的15个直播信息，其中时间最近的那个直播会在接口其他的返回参数中展示，其余的直播会在该字段中展示）。 |

<a id="status"></a>

### Status

| 参数 | 说明 |
| --- | --- |
| 2 | 直播中 |
| 3 | 直播结束 |

<a id="replaystatus"></a>

### ReplayStatus

| 参数 | 说明 |
| --- | --- |
| 0 | 未生成 |
| 1 | 已生成 |
| 3 | 生成中 |
| 6 | 已过期 |
