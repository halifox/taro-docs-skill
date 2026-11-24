# Taro.onSocketError(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/network/webSocket/onSocketError)

监听 WebSocket 错误事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/websocket/wx.onSocketError.html)

<a id="类型"></a>

## 类型

```tsx
(callback: (result: Callback) => void) => void
```

<a id="参数"></a>

## 参数

<a id="callback"></a>

### Callback

WebSocket 错误事件的回调函数

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
| errMsg | `string` | 错误信息 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.connectSocket({
  url: 'test.php'
})
Taro.onSocketOpen(function (res){
  console.log('WebSocket连接已打开！')
})
Taro.onSocketError(function (res){
  console.log('WebSocket连接打开失败，请检查！')
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | H5 | React Native |
| --- | --- | --- | --- | --- | --- |
| Taro.onSocketError | ✔️ | ✔️ | ✔️ |  |  |
