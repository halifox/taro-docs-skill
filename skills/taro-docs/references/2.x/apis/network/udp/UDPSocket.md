# UDPSocket

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/network/udp/UDPSocket)

一个 UDP Socket 实例，默认使用 IPv4 协议。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.html)

<a id="方法"></a>

## 方法

<a id="close"></a>

### close

关闭 UDP Socket 实例，相当于销毁。 在关闭之后，UDP Socket 实例不能再发送消息，每次调用 `UDPSocket.send` 将会触发错误事件，并且 message 事件回调函数也不会再也执行。在 `UDPSocket` 实例被创建后将被 Native 强引用，保证其不被 GC。在 `UDPSocket.close` 后将解除对其的强引用，让 UDPSocket 实例遵从 GC。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.close.html)

```tsx
() => void
```

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UDPSocket.close | ✔️ |  |  |

<a id="offclose"></a>

### offClose

取消监听关闭事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.offClose.html)

```tsx
(callback: OffCloseCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OffCloseCallback` | 关闭事件的回调函数 |

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UDPSocket.offClose | ✔️ |  |  |

<a id="offerror"></a>

### offError

取消监听错误事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.offError.html)

```tsx
(callback: OffErrorCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OffErrorCallback` | 错误事件的回调函数 |

<a id="api-支持度-2"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UDPSocket.offError | ✔️ |  |  |

<a id="offlistening"></a>

### offListening

取消监听开始监听数据包消息的事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.offListening.html)

```tsx
(callback: (res: CallbackResult) => void) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `(res: CallbackResult) => void` | 开始监听数据包消息的事件的回调函数 |

<a id="api-支持度-3"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UDPSocket.offListening | ✔️ |  |  |

<a id="offmessage"></a>

### offMessage

取消监听收到消息的事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.offMessage.html)

```tsx
(callback: (res: CallbackResult) => void) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `(res: CallbackResult) => void` | 收到消息的事件的回调函数 |

<a id="api-支持度-4"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UDPSocket.offMessage | ✔️ |  |  |

<a id="onclose"></a>

### onClose

监听关闭事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.onClose.html)

```tsx
(callback: OnCloseCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnCloseCallback` | 关闭事件的回调函数 |

<a id="api-支持度-5"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UDPSocket.onClose | ✔️ |  |  |

<a id="onerror"></a>

### onError

监听错误事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.onError.html)

```tsx
(callback: OnErrorCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnErrorCallback` | 错误事件的回调函数 |

<a id="api-支持度-6"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UDPSocket.onError | ✔️ |  |  |

<a id="onlistening"></a>

### onListening

监听开始监听数据包消息的事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.onListening.html)

```tsx
(callback: (res: CallbackResult) => void) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `(res: CallbackResult) => void` | 开始监听数据包消息的事件的回调函数 |

<a id="api-支持度-7"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UDPSocket.onListening | ✔️ |  |  |

<a id="onmessage"></a>

### onMessage

监听收到消息的事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.onMessage.html)

```tsx
(callback: OnMessageCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnMessageCallback` | 收到消息的事件的回调函数 |

<a id="api-支持度-8"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UDPSocket.onMessage | ✔️ |  |  |

<a id="send"></a>

### send

向指定的 IP 和 port 发送消息

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.send.html)

```tsx
(option: SendOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `SendOption` |

<a id="api-支持度-9"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UDPSocket.send | ✔️ |  |  |

<a id="bind"></a>

### bind

绑定一个系统随机分配的可用端口，或绑定一个指定的端口号

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.bind.html)

```tsx
(port: number) => number
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| port | `number` | 指定要绑定的端口号 |

<a id="api-支持度-10"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UDPSocket.bind | ✔️ |  |  |

<a id="参数"></a>

## 参数

<a id="offclosecallback"></a>

### OffCloseCallback

关闭事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="offerrorcallback"></a>

### OffErrorCallback

错误事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="onclosecallback"></a>

### OnCloseCallback

关闭事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="onerrorcallback"></a>

### OnErrorCallback

错误事件的回调函数

```tsx
(result: OnErrorCallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `OnErrorCallbackResult` |

<a id="onmessagecallback"></a>

### OnMessageCallback

收到消息的事件的回调函数

```tsx
(result: OnMessageCallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `OnMessageCallbackResult` |

<a id="onerrorcallbackresult"></a>

### OnErrorCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errMsg | `string` | 错误信息 |

<a id="onmessagecallbackresult"></a>

### OnMessageCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| message | `ArrayBuffer` | 收到的消息 |
| remoteInfo | `RemoteInfo` | 消息来源的结构化信息 |

<a id="remoteinfo"></a>

### RemoteInfo

消息来源的结构化信息

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| address | `string` | 发送消息的 socket 的地址 |
| family | `string` | 使用的协议族，为 IPv4 或者 IPv6 |
| port | `number` | 端口号 |
| size | `number` | message 的大小，单位：字节 |

<a id="sendoption"></a>

### SendOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| data | `string \| ArrayBuffer` | 是 | 需要发送的内容 |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="api-支持度-11"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UDPSocket.close | ✔️ |  |  |
| UDPSocket.offClose | ✔️ |  |  |
| UDPSocket.offError | ✔️ |  |  |
| UDPSocket.offListening | ✔️ |  |  |
| UDPSocket.offMessage | ✔️ |  |  |
| UDPSocket.onClose | ✔️ |  |  |
| UDPSocket.onError | ✔️ |  |  |
| UDPSocket.onListening | ✔️ |  |  |
| UDPSocket.onMessage | ✔️ |  |  |
| UDPSocket.send | ✔️ |  |  |
| UDPSocket.bind | ✔️ |  |  |
