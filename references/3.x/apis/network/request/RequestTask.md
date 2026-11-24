# RequestTask

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/network/request/RequestTask)

网络请求任务对象

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/request/RequestTask.html)

<a id="方法"></a>

## 方法

<a id="abort"></a>

### abort

中断请求任务

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/request/RequestTask.abort.html)

```tsx
() => void
```

<a id="onheadersreceived"></a>

### onHeadersReceived

监听 HTTP Response Header 事件。会比请求完成事件更早

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/request/RequestTask.onHeadersReceived.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | HTTP Response Header 事件的回调函数 |

<a id="offheadersreceived"></a>

### offHeadersReceived

取消监听 HTTP Response Header 事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/request/RequestTask.offHeadersReceived.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | HTTP Response Header 事件的回调函数 |

<a id="onchunkreceived"></a>

### onChunkReceived

监听 Transfer-Encoding Chunk Received 事件。当接收到新的chunk时触发。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/request/RequestTask.onChunkReceived.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | Transfer-Encoding Chunk Received 事件的回调函数 |

<a id="offchunkreceived"></a>

### offChunkReceived

移除 Transfer-Encoding Chunk Received 事件的监听函数

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/network/request/RequestTask.offChunkReceived.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | Transfer-Encoding Chunk Received 事件的回调函数 |

<a id="参数"></a>

## 参数

<a id="onheadersreceived-1"></a>

### onHeadersReceived

<a id="callback"></a>

#### Callback

HTTP Response Header 事件的回调函数

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
| header | `TaroGeneral.IAnyObject` | 开发者服务器返回的 HTTP Response Header |

<a id="onchunkreceived-1"></a>

### onChunkReceived

<a id="callback-1"></a>

#### Callback

Transfer-Encoding Chunk Received 事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="callbackresult-1"></a>

#### CallbackResult

开发者服务器每次返回新 chunk 时的 Response

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | `ArrayBuffer` | 返回的chunk buffer |

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

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| RequestTask | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| RequestTask.abort | ✔️ |  |  | ✔️ |  |  |  |  | ✔️ | ✔️ |
| RequestTask.onHeadersReceived | ✔️ |  |  |  |  |  |  |  | ✔️ | ✔️ |
| RequestTask.offHeadersReceived | ✔️ |  |  |  |  |  |  |  | ✔️ | ✔️ |
| RequestTask.onChunkReceived | ✔️ |  |  |  |  |  |  |  |  |  |
| RequestTask.offChunkReceived | ✔️ |  |  |  |  |  |  |  |  |  |
