# Taro.onHCEMessage(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/nfc/onHCEMessage)

监听接收 NFC 设备消息事件，仅能注册一个监听

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/nfc/wx.onHCEMessage.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 接收 NFC 设备消息事件的回调函数 |

<a id="callback"></a>

### Callback

接收 NFC 设备消息事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="callbackresult"></a>

### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | `ArrayBuffer` | `messageType=1` 时 ,客户端接收到 NFC 设备的指令 |
| messageType | `keyof MessageType` | 消息类型 |
| reason | `number` | `messageType=2` 时，原因 |

<a id="messagetype"></a>

### MessageType

消息类型

| 参数 | 说明 |
| --- | --- |
| 1 | HCE APDU Command类型，小程序需对此指令进行处理，并调用 sendHCEMessage 接口返回处理指令 |
| 2 | 设备离场事件类型 |
