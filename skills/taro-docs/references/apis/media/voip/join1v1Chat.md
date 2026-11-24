# Taro.join1v1Chat(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/media/voip/join1v1Chat)

加入（创建）双人通话

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/voip/wx.join1v1Chat.html)

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

<a id="caller"></a>

### Caller

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| nickname | `string` | 是 | 昵称 |
| headImage | `string` | 否 | 头像 |
| openid | `string` | 是 | 小程序内 openid |

<a id="listener"></a>

### Listener

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| nickname | `string` | 是 | 昵称 |
| headImage | `string` | 否 | 头像 |
| openid | `string` | 是 | 小程序内 openid |

<a id="roomtype"></a>

### RoomType

| 参数 | 说明 |
| --- | --- |
| voice | 语音通话 |
| video | 视频通话 |

<a id="option"></a>

### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| caller | `Caller` |  | 是 | 呼叫方信息 |
| listener | `Listener` |  | 是 | 接听方信息 |
| backgroundType | `keyof ColorType` | `0` | 否 | 窗口背景色 |
| roomType | `keyof RoomType` |  | 否 | 通话类型 |
| minWindowType | `keyof ColorType` | `1` | 否 | 小窗样式 |
| disableSwitchVoice | `boolean` | `false` | 否 | 不允许切换到语音通话 |
| complete | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="chaterrcode"></a>

### ChatErrCode

| 参数 | 说明 |
| --- | --- |
| -20000 | 未开通双人通话 |
| -20001 | 当前设备不支持 |
| -20002 | 正在通话中 |
| -20003 | 其它小程序正在通话中 |
| -30000 | 内部系统错误 |
| -30001 | 微信缺失相机权限 |
| -30002 | 微信缺失录音权限 |
| -30003 | 小程序缺失录音权限 |
| -30004 | 小程序缺失相机权限 |
| -1 | 当前已在房间内 |
| -2 | 录音设备被占用，可能是当前正在使用微信内语音通话或系统通话 |
| -3 | 加入会话期间退出（可能是用户主动退出，或者退后台、来电等原因），因此加入失败 |
| -1000 | 系统错误 |

<a id="failcallbackresult"></a>

### FailCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errMsg | `string` | 错误信息 |
| errCode | `keyof ChatErrCode` | 错误码 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errCode | `number` | 错误码 |
| errMsg | `string` | 调用结果 |

<a id="promised"></a>

### Promised

```tsx
FailCallbackResult | SuccessCallbackResult
```
