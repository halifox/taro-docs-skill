# DownloadTask

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/network/download/DownloadTask)

一个可以监听下载进度变化事件，以及取消下载任务的对象

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/download/DownloadTask.html)

<a id="方法"></a>

## 方法

<a id="abort"></a>

### abort

中断下载任务

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/download/DownloadTask.abort.html)

```tsx
() => void
```

<a id="onprogressupdate"></a>

### onProgressUpdate

监听下载进度变化事件

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/download/DownloadTask.onProgressUpdate.html)

```tsx
(callback: OnProgressUpdateCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnProgressUpdateCallback` | 下载进度变化事件的回调函数 |

<a id="offprogressupdate"></a>

### offProgressUpdate

取消监听下载进度变化事件

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/download/DownloadTask.offProgressUpdate.html)

```tsx
(callback: OnProgressUpdateCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnProgressUpdateCallback` | 下载进度变化事件的回调函数 |

<a id="onheadersreceived"></a>

### onHeadersReceived

监听 HTTP Response Header 事件。会比请求完成事件更早

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/download/DownloadTask.onHeadersReceived.html)

```tsx
(callback: OnHeadersReceivedCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnHeadersReceivedCallback` | HTTP Response Header 事件的回调函数 |

<a id="offheadersreceived"></a>

### offHeadersReceived

取消监听 HTTP Response Header 事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/download/DownloadTask.offHeadersReceived.html)

```tsx
(callback: OnHeadersReceivedCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnHeadersReceivedCallback` | HTTP Response Header 事件的回调函数 |

<a id="参数"></a>

## 参数

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
| header | `TaroGeneral.IAnyObject` | 开发者服务器返回的 HTTP Response Header |

<a id="onprogressupdatecallbackresult"></a>

### OnProgressUpdateCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| progress | `number` | 下载进度百分比 |
| totalBytesExpectedToWrite | `number` | 预期需要下载的数据总长度，单位 Bytes |
| totalBytesWritten | `number` | 已经下载的数据长度，单位 Bytes |

<a id="downloadtaskpromise"></a>

### DownloadTaskPromise

<a id="示例代码"></a>

## 示例代码

```tsx
const downloadTask = Taro.downloadFile({
  url: 'http://example.com/audio/123', //仅为示例，并非真实的资源
  success (res) {
    Taro.playVoice({
      filePath: res.tempFilePath
    })
  }
})

downloadTask.onProgressUpdate((res) => {
  console.log('下载进度', res.progress)
  console.log('已经下载的数据长度', res.totalBytesWritten)
  console.log('预期需要下载的数据总长度', res.totalBytesExpectedToWrite)
})

downloadTask.abort() // 取消下载任务
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DownloadTask | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| DownloadTask.abort | ✔️ |  |  | ✔️ | ✔️ |  |  | ✔️ | ✔️ |
| DownloadTask.onProgressUpdate | ✔️ |  |  | ✔️ | ✔️ |  |  | ✔️ | ✔️ |
| DownloadTask.offProgressUpdate | ✔️ |  |  | ✔️ | ✔️ |  |  | ✔️ | ✔️ |
| DownloadTask.onHeadersReceived | ✔️ |  |  |  | ✔️ |  |  |  | ✔️ |
| DownloadTask.offHeadersReceived | ✔️ |  |  |  | ✔️ |  |  |  | ✔️ |
