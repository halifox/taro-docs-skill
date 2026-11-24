# Taro.onSocketOpen(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/network/websocket/onSocketOpen)

监听 WebSocket 连接打开事件

支持情况：微信小程序 百度小程序 支付宝小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/websocket/wx.onSocketOpen.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | WebSocket 连接打开事件的回调函数 |

<a id="callback"></a>

### Callback

WebSocket 连接打开事件的回调函数

```tsx
(result: OpenCallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `OpenCallbackResult` |

<a id="opencallbackresult"></a>

### OpenCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| header | `TaroGeneral.IAnyObject` | 连接成功的 HTTP 响应 Header |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.connectSocket({
  url: 'test.php'
})
Taro.onSocketOpen(function (res) {
  console.log('WebSocket连接已打开！')
})
```
