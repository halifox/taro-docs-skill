# RequestTask

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/network/request/RequestTask)

网络请求任务对象

<a id="方法"></a>

## 方法

<a id="abort"></a>

### abort

中断请求任务

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/request/RequestTask.abort.html)

```tsx
() => void
```

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RequestTask.abort | ✔️ |  |  |

<a id="offheadersreceived"></a>

### offHeadersReceived

取消监听 HTTP Response Header 事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/request/RequestTask.offHeadersReceived.html)

```tsx
(callback: (res: CallbackResult) => void) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `(res: CallbackResult) => void` | HTTP Response Header 事件的回调函数 |

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RequestTask.offHeadersReceived | ✔️ |  |  |

<a id="onheadersreceived"></a>

### onHeadersReceived

监听 HTTP Response Header 事件。会比请求完成事件更早

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/request/RequestTask.onHeadersReceived.html)

```tsx
(callback: (result: OnHeadersReceivedCallbackResult) => void) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `(result: OnHeadersReceivedCallbackResult) => void` | HTTP Response Header 事件的回调函数 |

<a id="api-支持度-2"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RequestTask.onHeadersReceived | ✔️ |  |  |

<a id="参数"></a>

## 参数

<a id="onheadersreceivedcallbackresult"></a>

### OnHeadersReceivedCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| header | `Record<string, any>` | 开发者服务器返回的 HTTP Response Header |

<a id="示例代码"></a>

## 示例代码

<a id="示例-1"></a>

### 示例 1

回调函数(Callback)用法：

```tsx
const requestTask = Taro.request({
  url: 'test.php', //仅为示例，并非真实的接口地址
  data: {
    x: '' ,
    y: ''
  },
  header: {
    'content-type': 'application/json' // 默认值
  },
  success: function (res) {
    console.log(res.data)
  }
})
requestTask.abort()
```

<a id="示例-2"></a>

### 示例 2

Promise 用法：

```tsx
const requestTask = Taro.request({
  url: 'test.php', //仅为示例，并非真实的接口地址
  data: {
    x: '' ,
    y: ''
  },
  header: {
    'content-type': 'application/json' // 默认值
  },
  success: function (res) {
    console.log(res.data)
  }
})
requestTask.then(res => {
  console.log(res.data)
})
requestTask.abort()
```

<a id="示例-3"></a>

### 示例 3

async/await 用法：

```tsx
const requestTask = Taro.request(params)
const res = await requestTask
requestTask.abort()
```

<a id="api-支持度-3"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RequestTask.abort | ✔️ |  |  |
| RequestTask.offHeadersReceived | ✔️ |  |  |
| RequestTask.onHeadersReceived | ✔️ |  |  |
