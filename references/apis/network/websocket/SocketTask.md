# SocketTask

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/network/websocket/SocketTask)

WebSocket 任务，可通过 [Taro.connectSocket()](SocketTask.md) 接口创建返回。

支持情况：微信小程序 百度小程序 支付宝小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/websocket/SocketTask.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| socketTaskId | `number` | websocket 当前的连接 ID。 |
| readyState | `number` | websocket 当前的连接状态。 |
| errMsg | `string` | websocket 接口调用结果。 |
| CONNECTING | `number` | websocket 状态值：连接中。 |
| OPEN | `number` | websocket 状态值：已连接。 |
| CLOSING | `number` | websocket 状态值：关闭中。 |
| CLOSED | `number` | websocket 状态值：已关闭。 |
| ws | `WebSocket` | 浏览器 websocket 实例。（h5 端独有） |

<a id="send"></a>

### send

通过 WebSocket 连接发送数据

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/websocket/SocketTask.send.html)

```tsx
(option: SendOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `SendOption` |

<a id="close"></a>

### close

关闭 WebSocket 连接

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/websocket/SocketTask.close.html)

```tsx
(option: CloseOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `CloseOption` |

<a id="onopen"></a>

### onOpen

监听 WebSocket 连接打开事件

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/websocket/SocketTask.onOpen.html)

```tsx
(callback: OnOpenCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnOpenCallback` | WebSocket 连接打开事件的回调函数 |

<a id="onclose"></a>

### onClose

监听 WebSocket 连接关闭事件

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/websocket/SocketTask.onClose.html)

```tsx
(callback: OnCloseCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnCloseCallback` | WebSocket 连接关闭事件的回调函数 |

<a id="onerror"></a>

### onError

监听 WebSocket 错误事件

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/websocket/SocketTask.onError.html)

```tsx
(callback: OnErrorCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnErrorCallback` | WebSocket 错误事件的回调函数 |

<a id="onmessage"></a>

### onMessage

监听 WebSocket 接受到服务器的消息事件

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/websocket/SocketTask.onMessage.html)

```tsx
<T = any>(callback: OnMessageCallback<T>) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `T` | WebSocket 接受到服务器的消息事件的回调函数 |

<a id="参数"></a>

## 参数

<a id="closeoption"></a>

### CloseOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| code | `number` | 否 | 一个数字值表示关闭连接的状态号，表示连接被关闭的原因。 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| reason | `string` | 否 | 一个可读的字符串，表示连接被关闭的原因。这个字符串必须是不长于 123 字节的 UTF-8 文本（不是字符）。 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="onclosecallback"></a>

### OnCloseCallback

WebSocket 连接关闭事件的回调函数

```tsx
(result: OnCloseCallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `OnCloseCallbackResult` |

<a id="onclosecallbackresult"></a>

### OnCloseCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| code | `number` | 一个数字值表示关闭连接的状态号，表示连接被关闭的原因。 |
| reason | `string` | 一个可读的字符串，表示连接被关闭的原因。 |

<a id="onerrorcallback"></a>

### OnErrorCallback

WebSocket 错误事件的回调函数

```tsx
(result: OnErrorCallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `OnErrorCallbackResult` |

<a id="onerrorcallbackresult"></a>

### OnErrorCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errMsg | `string` | 错误信息 |

<a id="onmessagecallback"></a>

### OnMessageCallback

WebSocket 接受到服务器的消息事件的回调函数

```tsx
(result: OnMessageCallbackResult<T>) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `OnMessageCallbackResult<T>` |

<a id="onmessagecallbackresult"></a>

### OnMessageCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | `T` | 服务器返回的消息 |

<a id="onopencallback"></a>

### OnOpenCallback

WebSocket 连接打开事件的回调函数

```tsx
(result: OnOpenCallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `OnOpenCallbackResult` |

<a id="onopencallbackresult"></a>

### OnOpenCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| header | `TaroGeneral.IAnyObject` | 连接成功的 HTTP 响应 Header |

<a id="sendoption"></a>

### SendOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| data | string or ArrayBuffer | 是 | 需要发送的内容 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| SocketTask | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |  | ✔️ | ✔️ |
| SocketTask.send | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| SocketTask.close | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| SocketTask.onOpen | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| SocketTask.onClose | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| SocketTask.onError | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| SocketTask.onMessage | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
