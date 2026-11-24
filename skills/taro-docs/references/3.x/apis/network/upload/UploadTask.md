# UploadTask

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/network/upload/UploadTask)

一个可以监听上传进度变化事件，以及取消上传任务的对象

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/upload/UploadTask.html)

<a id="方法"></a>

## 方法

<a id="abort"></a>

### abort

中断上传任务

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/upload/UploadTask.abort.html)

```tsx
() => void
```

<a id="onprogressupdate"></a>

### onProgressUpdate

监听上传进度变化事件

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/upload/UploadTask.onProgressUpdate.html)

```tsx
(callback: OnProgressUpdateCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnProgressUpdateCallback` | 上传进度变化事件的回调函数 |

<a id="offprogressupdate"></a>

### offProgressUpdate

取消监听上传进度变化事件

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/upload/UploadTask.offProgressUpdate.html)

```tsx
(callback: OnProgressUpdateCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnProgressUpdateCallback` | 上传进度变化事件的回调函数 |

<a id="onheadersreceived"></a>

### onHeadersReceived

监听 HTTP Response Header 事件。会比请求完成事件更早

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/upload/UploadTask.onHeadersReceived.html)

```tsx
(callback: OnHeadersReceivedCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnHeadersReceivedCallback` | HTTP Response Header 事件的回调函数 |

<a id="offheadersreceived"></a>

### offHeadersReceived

取消监听 HTTP Response Header 事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/upload/UploadTask.offHeadersReceived.html)

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
| header | `TaroGeneral.IAnyObject` | 开发者服务器返回的 HTTP Response Header |

<a id="onprogressupdatecallbackresult"></a>

### OnProgressUpdateCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| progress | `number` | 上传进度百分比 |
| totalBytesExpectedToSend | `number` | 预期需要上传的数据总长度，单位 Bytes |
| totalBytesSent | `number` | 已经上传的数据长度，单位 Bytes |

<a id="uploadtaskpromise"></a>

### UploadTaskPromise

<a id="示例代码"></a>

## 示例代码

```tsx
const uploadTask = Taro.uploadFile({
  url: 'http://example.weixin.qq.com/upload', //仅为示例，非真实的接口地址
  filePath: tempFilePaths[0],
  name: 'file',
  formData:{
    'user': 'test'
  },
  success (res){
    const data = res.data
    //do something
  }
})

uploadTask.onProgressUpdate((res) => {
  console.log('上传进度', res.progress)
  console.log('已经上传的数据长度', res.totalBytesSent)
  console.log('预期需要上传的数据总长度', res.totalBytesExpectedToSend)
})

uploadTask.abort() // 取消上传任务
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| UploadTask | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| UploadTask.abort | ✔️ |  |  | ✔️ | ✔️ |  |  | ✔️ | ✔️ |
| UploadTask.onProgressUpdate | ✔️ |  |  | ✔️ | ✔️ |  |  | ✔️ | ✔️ |
| UploadTask.offProgressUpdate | ✔️ |  |  | ✔️ | ✔️ |  |  | ✔️ | ✔️ |
| UploadTask.onHeadersReceived | ✔️ |  |  |  | ✔️ |  |  | ✔️ | ✔️ |
| UploadTask.offHeadersReceived | ✔️ |  |  |  | ✔️ |  |  | ✔️ | ✔️ |
