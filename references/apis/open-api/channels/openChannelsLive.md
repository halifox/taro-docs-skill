# Taro.openChannelsLive(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/open-api/channels/openChannelsLive)

打开视频号直播

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/channels/wx.openChannelsLive.html)

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
| finderUserName | `string` | 是 | 视频号 id，以“sph”开头的id，可在视频号助手获取 |
| feedId | `string` | 否 | 直播 feedId，通过 getChannelsLiveInfo 接口获取 |
| nonceId | `string` | 否 | 直播 nonceId，通过 getChannelsLiveInfo 接口获取 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |
