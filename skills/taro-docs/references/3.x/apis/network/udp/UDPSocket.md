# UDPSocket

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/network/udp/UDPSocket)

一个 UDP Socket 实例，默认使用 IPv4 协议。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.html)

<a id="方法"></a>

## 方法

<a id="bind"></a>

### bind

绑定一个系统随机分配的可用端口，或绑定一个指定的端口号

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.bind.html)

```tsx
(port: number) => number
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| port | `number` | 指定要绑定的端口号，不传则返回系统随机分配的可用端口 |

<a id="示例代码"></a>

#### 示例代码

```tsx
const udp = Taro.createUDPSocket()
udp.close()
```

<a id="setttl"></a>

### setTTL

设置 IP\_TTL 套接字选项，用于设置一个 IP 数据包传输时允许的最大跳步数

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.setTTL.html)

```tsx
(ttl: number) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| ttl | `number` | ttl 参数可以是 0 到 255 之间 |

<a id="示例代码-1"></a>

#### 示例代码

```tsx
const udp = Taro.createUDPSocket()
udp.onListening(function () {
  udp.setTTL(64)
})
udp.bind()
```

<a id="send"></a>

### send

向指定的 IP 和 port 发送消息

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.send.html)

```tsx
(option: Option) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="示例代码-2"></a>

#### 示例代码

```tsx
const udp = Taro.createUDPSocket()
udp.bind()
udp.send({
  address: '192.168.193.2',
  port: 8848,
  message: 'hello, how are you'
})
```

<a id="connect"></a>

### connect

预先连接到指定的 IP 和 port，需要配合 write 方法一起使用

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.connect.html)

```tsx
(option: Option) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="write"></a>

### write

用法与 send 方法相同，如果没有预先调用 connect 则与 send 无差异（注意即使调用了 connect 也需要在本接口填入地址和端口参数）

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.write.html)

```tsx
() => void
```

<a id="close"></a>

### close

关闭 UDP Socket 实例，相当于销毁。 在关闭之后，UDP Socket 实例不能再发送消息，每次调用 `UDPSocket.send` 将会触发错误事件，并且 message 事件回调函数也不会再也执行。在 `UDPSocket` 实例被创建后将被 Native 强引用，保证其不被 GC。在 `UDPSocket.close` 后将解除对其的强引用，让 UDPSocket 实例遵从 GC。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.close.html)

```tsx
() => void
```

<a id="onclose"></a>

### onClose

监听关闭事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.onClose.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 关闭事件的回调函数 |

<a id="offclose"></a>

### offClose

取消监听关闭事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.offClose.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 关闭事件的回调函数 |

<a id="onerror"></a>

### onError

监听错误事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.onError.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 错误事件的回调函数 |

<a id="offerror"></a>

### offError

取消监听错误事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.offError.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 错误事件的回调函数 |

<a id="onlistening"></a>

### onListening

监听开始监听数据包消息的事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.onListening.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 监听开始监听数据包消息的事件 |

<a id="offlistening"></a>

### offListening

取消监听开始监听数据包消息的事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.offListening.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 监听开始监听数据包消息的事件 |

<a id="onmessage"></a>

### onMessage

监听收到消息的事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.onMessage.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 收到消息的事件的回调函数 |

<a id="offmessage"></a>

### offMessage

取消监听收到消息的事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/udp/UDPSocket.offMessage.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 收到消息的事件的回调函数 |

<a id="参数"></a>

## 参数

<a id="connect-1"></a>

### connect

<a id="option"></a>

#### Option

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| address | `string` | 要发消息的地址 |
| port | `number` | 要发送消息的端口号 |

<a id="onclose-1"></a>

### onClose

<a id="callback"></a>

#### Callback

当一个 socket 完全关闭就发出该事件的回调函数

```tsx
(args: unknown[]) => void
```

| 参数 | 类型 |
| --- | --- |
| args | `unknown[]` |

<a id="onerror-1"></a>

### onError

<a id="callback-1"></a>

#### Callback

错误事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="callbackresult"></a>

#### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errMsg | `string` | 错误信息 |

<a id="onlistening-1"></a>

### onListening

<a id="callback-2"></a>

#### Callback

监听开始监听数据包消息的事件

```tsx
(args: unknown[]) => void
```

| 参数 | 类型 |
| --- | --- |
| args | `unknown[]` |

<a id="onmessage-1"></a>

### onMessage

<a id="callback-3"></a>

#### Callback

收到消息的事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="callbackresult-1"></a>

#### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| message | `ArrayBuffer` | 收到的消息 |
| remoteInfo | `RemoteInfo` | 发送端地址信息 |
| localInfo | `LocalInfo` | 接收端地址信息 |

<a id="remoteinfo"></a>

#### RemoteInfo

发送端地址信息

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| address | `string` | 发送消息的 socket 的地址 |
| family | `string` | 使用的协议族，为 IPv4 或者 IPv6 |
| port | `number` | 端口号 |

<a id="localinfo"></a>

#### LocalInfo

接收端地址信息

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| address | `string` | 接收消息的 socket 的地址 |
| family | `string` | 使用的协议族，为 IPv4 或者 IPv6 |
| port | `number` | 端口号 |
| size | `number` | message 的大小，单位：字节 |

<a id="send-1"></a>

### send

<a id="option-1"></a>

#### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| address | `string` |  | 是 | 要发消息的地址。在基础库 <= 2.9.3 版本必须是和本机同网段的 IP 地址，或安全域名列表内的域名地址；之后版本可以是任意 IP 和域名 |
| port | `number` |  | 是 | 要发送消息的端口号 |
| message | string or ArrayBuffer |  | 是 | 要发送的数据 |
| offset | `number` | `0` | 否 | 发送数据的偏移量，仅当 message 为 ArrayBuffer 类型时有效 |
| length | `number` | `message.byteLength` | 否 | 发送数据的长度，仅当 message 为 ArrayBuffer 类型时有效 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| UDPSocket | ✔️ |  |  |  |  |
| UDPSocket.bind | ✔️ |  |  |  |  |
| UDPSocket.setTTL | ✔️ |  |  |  |  |
| UDPSocket.send | ✔️ |  |  |  |  |
| UDPSocket.connect | ✔️ |  |  |  |  |
| UDPSocket.write | ✔️ |  |  |  |  |
| UDPSocket.close | ✔️ |  |  |  |  |
| UDPSocket.onClose | ✔️ |  |  |  |  |
| UDPSocket.offClose | ✔️ |  |  |  |  |
| UDPSocket.onError | ✔️ |  |  |  |  |
| UDPSocket.offError | ✔️ |  |  |  |  |
| UDPSocket.onListening | ✔️ |  |  |  |  |
| UDPSocket.offListening | ✔️ |  |  |  |  |
| UDPSocket.onMessage | ✔️ |  |  |  |  |
| UDPSocket.offMessage | ✔️ |  |  |  |  |
