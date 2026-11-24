# Taro.joinVoIPChat(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/media/voip/joinVoIPChat)

加入 (创建) 实时语音通话，更多信息可见 [实时语音指南](https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/voip-chat.html)

调用前需要用户授权 `scope.record`，若房间类型为视频房间需要用户授权 `scope.camera`。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/voip/wx.joinVoIPChat.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<Promised>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="promised"></a>

### Promised

```tsx
FailCallbackResult | SuccessCallbackResult
```

<a id="option"></a>

### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| roomType | `RoomType` | `"voice"` | 否 | 房间类型 |
| signature | `string` |  | 是 | 签名，用于验证小游戏的身份 |
| nonceStr | `string` |  | 是 | 验证所需的随机字符串 |
| timeStamp | `number` |  | 是 | 验证所需的时间戳 |
| groupId | `string` |  | 是 | 小游戏内此房间/群聊的 ID。同一时刻传入相同 groupId 的用户会进入到同个实时语音房间。 |
| muteConfig | `MuteConfig` |  | 否 | 静音设置 |
| complete | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="roomtype"></a>

### RoomType

房间类型

| 参数 | 说明 |
| --- | --- |
| voice | 音频房间，用于语音通话 |
| video | 视频房间，结合 [voip-room](../../../../components/media/voip-room.md) 组件可显示成员画面 |

<a id="muteconfig"></a>

### MuteConfig

静音设置

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| muteMicrophone | `boolean` | 否 | 是否静音麦克风 |
| muteEarphone | `boolean` | 否 | 是否静音耳机 |

<a id="failcallbackresult"></a>

### FailCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errMsg | `string` | 错误信息 |
| errCode | `keyof VoipErrCode` | 错误码 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| openIdList | `string[]` | 还在实时语音通话中的成员 openId 名单 |
| errCode | `number` | 错误码 |
| errMsg | `string` | 调用结果 |

<a id="voiperrcode"></a>

### VoipErrCode

Voip 错误码

| 参数 | 说明 |
| --- | --- |
| -1 | 当前已在房间内 |
| -2 | 录音设备被占用，可能是当前正在使用微信内语音通话或系统通话 |
| -3 | 加入会话期间退出（可能是用户主动退出，或者退后台、来电等原因），因此加入失败 |
| -1000 | 系统错误 |
