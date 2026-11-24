# Taro.onSocketMessage(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/network/webSocket/onSocketMessage)

监听 WebSocket 接受到服务器的消息事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/websocket/wx.onSocketMessage.html)

<a id="类型"></a>

## 类型

```tsx
<T = any>(callback: Callback<T>) => void
```

<a id="参数"></a>

## 参数

<a id="callback"></a>

### Callback

WebSocket 接受到服务器的消息事件的回调函数

```tsx
(result: CallbackResult<T>) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult<T>` |

<a id="callbackresult"></a>

### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | `T` | 服务器返回的消息 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.connectSocket({
  url: 'test.php'
})
Taro.onSocketMessage(function (res) {
  console.log('收到服务器内容：' + res.data)
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | H5 | React Native |
| --- | --- | --- | --- | --- | --- |
| Taro.onSocketMessage | ✔️ | ✔️ | ✔️ |  |  |
