# TCPSocket

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/network/tcp/TCPSocket)

一个 TCP Socket 实例，默认使用 IPv4 协议

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/tcp/TCPSocket.html)

<a id="方法"></a>

## 方法

<a id="connect"></a>

### connect

在给定的套接字上启动连接

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/tcp/TCPSocket.connect.html)

```tsx
(option: Option) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="示例代码"></a>

#### 示例代码

```tsx
const tcp = Taro.createTCPSocket()
tcp.connect({ address: '192.168.193.2', port: 8848 })
```

<a id="write"></a>

### write

在 socket 上发送数据

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/tcp/TCPSocket.write.html)

```tsx
(data: string | ArrayBuffer) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | string or ArrayBuffer | 要发送的数据 |

<a id="示例代码-1"></a>

#### 示例代码

```tsx
const tcp = Taro.createTCPSocket()
tcp.write('hello, how are you')
```

<a id="close"></a>

### close

关闭连接

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/tcp/TCPSocket.close.html)

```tsx
() => void
```

<a id="示例代码-2"></a>

#### 示例代码

```tsx
const tcp = Taro.createTCPSocket()
tcp.close()
```

<a id="onclose"></a>

### onClose

监听关闭事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/tcp/TCPSocket.onClose.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 当一个 socket 完全关闭就发出该事件的回调函数 |

<a id="offclose"></a>

### offClose

取消监听当一个 socket 完全关闭就发出该事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/tcp/TCPSocket.offClose.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 当一个 socket 完全关闭就发出该事件的回调函数 |

<a id="onconnect"></a>

### onConnect

监听当一个 socket 连接成功建立的时候触发该事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/tcp/TCPSocket.onConnect.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 当一个 socket 连接成功建立的时候触发该事件的回调函数 |

<a id="offconnect"></a>

### offConnect

取消监听当一个 socket 连接成功建立的时候触发该事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/tcp/TCPSocket.offConnect.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 当一个 socket 连接成功建立的时候触发该事件的回调函数 |

<a id="onerror"></a>

### onError

监听当错误发生时触发

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/tcp/TCPSocket.onError.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 监听当错误发生时触发的回调函数 |

<a id="offerror"></a>

### offError

取消监听当错误发生时触发

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/tcp/TCPSocket.offError.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 监听当错误发生时触发的回调函数 |

<a id="onmessage"></a>

### onMessage

监听当接收到数据的时触发该事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/tcp/TCPSocket.onMessage.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 当接收到数据的时触发该事件的回调函数 |

<a id="offmessage"></a>

### offMessage

取消监听当接收到数据的时触发该事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/tcp/TCPSocket.offMessage.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 当接收到数据的时触发该事件的回调函数 |

<a id="参数"></a>

## 参数

<a id="connect-1"></a>

### connect

<a id="option"></a>

#### Option

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| address | `string` | 套接字要连接的地址 |
| port | `number` | 套接字要连接的端口 |

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

<a id="onconnect-1"></a>

### onConnect

<a id="callback-1"></a>

#### Callback

当一个 socket 连接成功建立的时候触发该事件的回调函数

```tsx
(args: unknown[]) => void
```

| 参数 | 类型 |
| --- | --- |
| args | `unknown[]` |

<a id="onerror-1"></a>

### onError

<a id="callback-2"></a>

#### Callback

监听当错误发生时触发的回调函数

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

<a id="onmessage-1"></a>

### onMessage

<a id="callback-3"></a>

#### Callback

当接收到数据的时触发该事件的回调函数

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
| size | `number` | message 的大小，单位：字节 |

<a id="localinfo"></a>

#### LocalInfo

接收端地址信息

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| address | `string` | 接收消息的 socket 的地址 |
| family | `string` | 使用的协议族，为 IPv4 或者 IPv6 |
| port | `number` | 端口号 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| TCPSocket | ✔️ |  |  |  |  |
| TCPSocket.connect | ✔️ |  |  |  |  |
| TCPSocket.write | ✔️ |  |  |  |  |
| TCPSocket.close | ✔️ |  |  |  |  |
| TCPSocket.onClose | ✔️ |  |  |  |  |
| TCPSocket.offClose | ✔️ |  |  |  |  |
| TCPSocket.onConnect | ✔️ |  |  |  |  |
| TCPSocket.offConnect | ✔️ |  |  |  |  |
| TCPSocket.onError | ✔️ |  |  |  |  |
| TCPSocket.offError | ✔️ |  |  |  |  |
| TCPSocket.onMessage | ✔️ |  |  |  |  |
| TCPSocket.offMessage | ✔️ |  |  |  |  |
