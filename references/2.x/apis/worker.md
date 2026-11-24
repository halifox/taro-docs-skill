# Worker

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/worker/)

<a id="方法"></a>

## 方法

<a id="onmessage"></a>

### onMessage

监听主线程/Worker 线程向当前线程发送的消息的事件。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/worker/Worker.onMessage.html)

```tsx
(callback: OnMessageCallback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `OnMessageCallback` | 主线程/Worker 线程向当前线程发送的消息的事件的回调函数 |

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Worker.onMessage | ✔️ |  |  |

<a id="postmessage"></a>

### postMessage

向主线程/Worker 线程发送的消息。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/worker/Worker.postMessage.html)

```tsx
(message: Record<string, any>) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| message | `Record<string, any>` | 需要发送的消息，必须是一个可序列化的 JavaScript key-value 形式的对象。 |

<a id="示例代码"></a>

#### 示例代码

worker 线程中

```tsx
worker.postMessage({
  msg: 'hello from worker'
})
```

主线程中

```tsx
const worker = Taro.createWorker('workers/request/index.js')
worker.postMessage({
  msg: 'hello from main'
})
```

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Worker.postMessage | ✔️ |  |  |

<a id="terminate"></a>

### terminate

结束当前 Worker 线程。仅限在主线程 worker 对象上调用。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/worker/Worker.terminate.html)

```tsx
() => void
```

<a id="api-支持度-2"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Worker.terminate | ✔️ |  |  |

<a id="参数"></a>

## 参数

<a id="onmessagecallback"></a>

### OnMessageCallback

```tsx
(result: OnMessageCallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `OnMessageCallbackResult` |

<a id="onmessagecallbackresult"></a>

### OnMessageCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| message | `Record<string, any>` | 主线程/Worker 线程向当前线程发送的消息 |

<a id="api-支持度-3"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Worker.onMessage | ✔️ |  |  |
| Worker.postMessage | ✔️ |  |  |
| Worker.terminate | ✔️ |  |  |
