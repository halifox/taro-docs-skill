# DownloadTask

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/network/download/DownloadTask)

<a id="方法"></a>

## 方法

<a id="abort"></a>

### abort

中断下载任务

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/download/DownloadTask.abort.html)

```tsx
() => void
```

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| DownloadTask.abort | ✔️ |  |  |

<a id="offheadersreceived"></a>

### offHeadersReceived

取消监听 HTTP Response Header 事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/download/DownloadTask.offHeadersReceived.html)

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
| DownloadTask.offHeadersReceived | ✔️ |  |  |

<a id="offprogressupdate"></a>

### offProgressUpdate

取消监听下载进度变化事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/download/DownloadTask.offProgressUpdate.html)

```tsx
(callback: OffProgressUpdateCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OffProgressUpdateCallback` | 下载进度变化事件的回调函数 |

<a id="api-支持度-2"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| DownloadTask.offProgressUpdate | ✔️ |  |  |

<a id="onheadersreceived"></a>

### onHeadersReceived

监听 HTTP Response Header 事件。会比请求完成事件更早

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/download/DownloadTask.onHeadersReceived.html)

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
| DownloadTask.onHeadersReceived | ✔️ |  |  |

<a id="onprogressupdate"></a>

### onProgressUpdate

监听下载进度变化事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/download/DownloadTask.onProgressUpdate.html)

```tsx
(callback: OnProgressUpdateCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnProgressUpdateCallback` | 下载进度变化事件的回调函数 |

<a id="api-支持度-4"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| DownloadTask.onProgressUpdate | ✔️ |  |  |

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

下载进度变化事件的回调函数

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

下载进度变化事件的回调函数

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
| progress | `number` | 下载进度百分比 |
| totalBytesExpectedToWrite | `number` | 预期需要下载的数据总长度，单位 Bytes |
| totalBytesWritten | `number` | 已经下载的数据长度，单位 Bytes |

<a id="api-支持度-5"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| DownloadTask.abort | ✔️ |  |  |
| DownloadTask.offHeadersReceived | ✔️ |  |  |
| DownloadTask.offProgressUpdate | ✔️ |  |  |
| DownloadTask.onHeadersReceived | ✔️ |  |  |
| DownloadTask.onProgressUpdate | ✔️ |  |  |
