# Taro.onVoIPChatMembersChanged(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/media/voip/onVoIPChatMembersChanged)

监听实时语音通话成员在线状态变化事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/voip/wx.onVoIPChatMembersChanged.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| callback | `Callback` |

<a id="result"></a>

### Result

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| openIdList | `string[]` | 还在实时语音通话中的成员 openId 名单 |
| errCode | `number` | 错误码 |
| errMsg | `string` | 调用结果 |

<a id="callback"></a>

### Callback

房间状态变化事件的回调函数

```tsx
(res: Result) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `Result` |
