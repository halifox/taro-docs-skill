# Taro.reserveChannelsLive(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/open-api/channels/reserveChannelsLive)

预约视频号直播

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/channels/wx.reserveChannelsLive.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => void
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
| noticeId | `string` | 预告 id，通过 [getChannelsLiveNoticeInfo](getChannelsLiveNoticeInfo.md) 接口获取 |
