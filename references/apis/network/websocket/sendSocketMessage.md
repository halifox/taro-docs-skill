# Taro.sendSocketMessage(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/network/websocket/sendSocketMessage)

通过 WebSocket 连接发送数据。需要先 Taro.connectSocket，并在 Taro.onSocketOpen 回调之后才能发送。

支持情况：微信小程序 百度小程序 支付宝小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/websocket/wx.sendSocketMessage.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<TaroGeneral.CallbackResult>
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
| data | string or ArrayBuffer | 是 | 需要发送的内容 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
let socketOpen = false
const socketMsgQueue = []
Taro.connectSocket({
  url: 'test.php'
})
Taro.onSocketOpen(function(res) {
  socketOpen = true
  for (let i = 0; i < socketMsgQueue.length; i++){
    sendSocketMessage(socketMsgQueue[i])
  }
  socketMsgQueue = []
})
function sendSocketMessage(msg) {
  if (socketOpen) {
    Taro.sendSocketMessage({
      data:msg
    })
  } else {
    socketMsgQueue.push(msg)
  }
}
```
