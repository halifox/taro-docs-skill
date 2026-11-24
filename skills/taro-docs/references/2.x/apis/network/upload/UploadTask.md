# UploadTask

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/network/upload/UploadTask)

一个可以监听上传进度变化事件，以及取消上传任务的对象

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/upload/UploadTask.html)

<a id="方法"></a>

## 方法

<a id="abort"></a>

### abort

中断上传任务

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/upload/UploadTask.abort.html)

```tsx
() => void
```

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UploadTask.abort | ✔️ |  |  |

<a id="offheadersreceived"></a>

### offHeadersReceived

取消监听 HTTP Response Header 事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/upload/UploadTask.offHeadersReceived.html)

```tsx
(callback: OffHeadersReceivedCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OffHeadersReceivedCallback` | HTTP Response Header 事件的回调函数 |

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UploadTask.offHeadersReceived | ✔️ |  |  |

<a id="offprogressupdate"></a>

### offProgressUpdate

取消监听上传进度变化事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/upload/UploadTask.offProgressUpdate.html)

```tsx
(callback: OffProgressUpdateCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OffProgressUpdateCallback` | 上传进度变化事件的回调函数 |

<a id="api-支持度-2"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UploadTask.offProgressUpdate | ✔️ |  |  |

<a id="onheadersreceived"></a>

### onHeadersReceived

监听 HTTP Response Header 事件。会比请求完成事件更早

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/upload/UploadTask.onHeadersReceived.html)

```tsx
(callback: OnHeadersReceivedCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnHeadersReceivedCallback` | HTTP Response Header 事件的回调函数 |

<a id="api-支持度-3"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UploadTask.onHeadersReceived | ✔️ |  |  |

<a id="headersreceived"></a>

### headersReceived

```tsx
(callback: OnHeadersReceivedCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnHeadersReceivedCallback` | HTTP Response Header 事件的回调函数 |

<a id="onprogressupdate"></a>

### onProgressUpdate

监听上传进度变化事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/upload/UploadTask.onProgressUpdate.html)

```tsx
(callback: OnProgressUpdateCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnProgressUpdateCallback` | 上传进度变化事件的回调函数 |

<a id="api-支持度-4"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UploadTask.onProgressUpdate | ✔️ |  |  |

<a id="progress"></a>

### progress

```tsx
(callback: OnProgressUpdateCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnProgressUpdateCallback` | 上传进度变化事件的回调函数 |

<a id="参数"></a>

## 参数

<a id="offheadersreceivedcallback"></a>

### OffHeadersReceivedCallback

HTTP Response Header 事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="offprogressupdatecallback"></a>

### OffProgressUpdateCallback

上传进度变化事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="onheadersreceivedcallback"></a>

### OnHeadersReceivedCallback

HTTP Response Header 事件的回调函数

```tsx
(result: OnHeadersReceivedCallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `OnHeadersReceivedCallbackResult` |

<a id="onprogressupdatecallback"></a>

### OnProgressUpdateCallback

上传进度变化事件的回调函数

```tsx
(result: OnProgressUpdateCallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `OnProgressUpdateCallbackResult` |

<a id="onheadersreceivedcallbackresult"></a>

### OnHeadersReceivedCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| header | `Record<string, any>` | 开发者服务器返回的 HTTP Response Header |

<a id="onprogressupdatecallbackresult"></a>

### OnProgressUpdateCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| progress | `number` | 上传进度百分比 |
| totalBytesExpectedToSend | `number` | 预期需要上传的数据总长度，单位 Bytes |
| totalBytesSent | `number` | 已经上传的数据长度，单位 Bytes |

<a id="api-支持度-5"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| UploadTask.abort | ✔️ |  |  |
| UploadTask.offHeadersReceived | ✔️ |  |  |
| UploadTask.offProgressUpdate | ✔️ |  |  |
| UploadTask.onHeadersReceived | ✔️ |  |  |
| UploadTask.onProgressUpdate | ✔️ |  |  |
