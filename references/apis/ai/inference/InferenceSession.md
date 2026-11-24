# InferenceSession

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/ai/inference/InferenceSession)

<a id="方法"></a>

## 方法

<a id="destroy"></a>

### destroy

销毁 InferenceSession 实例

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/inference/InferenceSession.destroy.html)

```tsx
() => void
```

<a id="offerror"></a>

### offError

取消监听模型加载失败事件. 传入指定回调函数则只取消指定回调，不传则取消所有回调

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/inference/InferenceSession.offError.html)

```tsx
(callback?: OnErrorCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnErrorCallback` |

<a id="offload"></a>

### offLoad

取消监听模型加载完成事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/inference/InferenceSession.offLoad.html)

```tsx
(callback?: OnLoadCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnLoadCallback` |

<a id="onerror"></a>

### onError

监听模型加载失败事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/inference/InferenceSession.onError.html)

```tsx
(callback: OnErrorCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnErrorCallback` |

<a id="onload"></a>

### onLoad

监听模型加载完成事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/inference/InferenceSession.onLoad.html)

```tsx
(callback: OnLoadCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnLoadCallback` |

<a id="run"></a>

### run

运行推断
需要在 session.onLoad 回调后使用。接口参数为 Tensors 对象，返回 Promise。
一个 InferenceSession 被创建完成后可以重复多次调用 InferenceSession.run(), 直到调用 session.destroy() 进行销毁。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/inference/InferenceSession.destroy.html)

```tsx
(option: Tensors) => Promise<Tensors>
```

| 参数 | 类型 |
| --- | --- |
| option | `Tensors` |

<a id="参数"></a>

## 参数

<a id="type"></a>

### Type

<a id="tensor"></a>

### Tensor

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| shape | `number[]` | Tensor shape （Tensor 形状，例如 [1, 3, 224, 224] 即表示一个4唯Tensor，每个维度的长度分别为1, 3, 224, 224） |
| data | `ArrayBuffer` | Tensor 值，一段 ArrayBuffer |
| type | `keyof Type` | ArrayBuffer 值的类型，合法值有 uint8, int8, uint32, int32, float32 |

<a id="tensors"></a>

### Tensors

| 参数 | 类型 |
| --- | --- |
| \_\_index | `__index` |

<a id="onerrorcallback"></a>

### OnErrorCallback

模型加载失败回调函数

```tsx
(res: TaroGeneral.CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `TaroGeneral.CallbackResult` |

<a id="onloadcallback"></a>

### OnLoadCallback

模型加载完成回调函数

```tsx
(res: TaroGeneral.CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `TaroGeneral.CallbackResult` |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| InferenceSession.destroy | ✔️ |  |  |  |  |
| InferenceSession.offError | ✔️ |  |  |  |  |
| InferenceSession.offLoad | ✔️ |  |  |  |  |
| InferenceSession.onError | ✔️ |  |  |  |  |
| InferenceSession.onLoad | ✔️ |  |  |  |  |
| InferenceSession.run | ✔️ |  |  |  |  |
