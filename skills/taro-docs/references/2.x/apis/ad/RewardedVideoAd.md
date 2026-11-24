# RewardedVideoAd

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/ad/RewardedVideoAd)

激励视频广告组件。激励视频广告组件是一个原生组件，层级比普通组件高。激励视频广告是一个单例（小游戏端是全局单例，小程序端是页面内单例，在小程序端的单例对象不允许跨页面使用），默认是隐藏的，需要调用 RewardedVideoAd.show() 将其显示。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.html)

<a id="方法"></a>

## 方法

<a id="load"></a>

### load

加载激励视频广告。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.load.html)

```tsx
() => Promise<any>
```

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RewardedVideoAd.load | ✔️ |  |  |

<a id="show"></a>

### show

显示激励视频广告。激励视频广告将从屏幕下方推入。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.show.html)

```tsx
() => Promise<any>
```

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RewardedVideoAd.show | ✔️ |  |  |

<a id="destroy"></a>

### destroy

销毁激励视频广告实例。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.destroy.html)

```tsx
() => void
```

<a id="api-支持度-2"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RewardedVideoAd.destroy | ✔️ |  |  |

<a id="offclose"></a>

### offClose

取消监听用户点击 `关闭广告` 按钮的事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.offClose.html)

```tsx
(callback: OffCloseCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OffCloseCallback` |

<a id="api-支持度-3"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RewardedVideoAd.offClose | ✔️ |  |  |

<a id="offerror"></a>

### offError

取消监听激励视频错误事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.offError.html)

```tsx
(callback: OffErrorCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OffErrorCallback` |

<a id="api-支持度-4"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RewardedVideoAd.offError | ✔️ |  |  |

<a id="offload"></a>

### offLoad

取消监听激励视频广告加载事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.offLoad.html)

```tsx
(callback: OffLoadCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OffLoadCallback` |

<a id="api-支持度-5"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RewardedVideoAd.offLoad | ✔️ |  |  |

<a id="onclose"></a>

### onClose

监听用户点击 `关闭广告` 按钮的事件。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.onClose.html)

```tsx
(callback: OnCloseCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnCloseCallback` |

<a id="api-支持度-6"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RewardedVideoAd.onClose | ✔️ |  |  |

<a id="onerror"></a>

### onError

监听激励视频错误事件。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.onError.html)

```tsx
(callback: OnErrorCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnErrorCallback` |

<a id="api-支持度-7"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RewardedVideoAd.onError | ✔️ |  |  |

<a id="onload"></a>

### onLoad

监听激励视频广告加载事件。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.onLoad.html)

```tsx
(callback: OnLoadCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnLoadCallback` |

<a id="api-支持度-8"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RewardedVideoAd.onLoad | ✔️ |  |  |

<a id="参数"></a>

## 参数

<a id="onerrorcallbackresult"></a>

### OnErrorCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errCode | `1000 \| 1001 \| 1002 \| 1003 \| 1004 \| 1005 \| 1006 \| 1007 \| 1008` | 错误码<br>[参考地址](../../../apis/General.md#aderrcode) |
| errMsg | `string` | 错误信息 |

<a id="onclosecallbackresult"></a>

### OnCloseCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| isEnded | `boolean` | 视频是否是在用户完整观看的情况下被关闭的 |

<a id="offclosecallback"></a>

### OffCloseCallback

用户点击 `关闭广告` 按钮的事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="offerrorcallback"></a>

### OffErrorCallback

激励视频错误事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="offloadcallback"></a>

### OffLoadCallback

激励视频广告加载事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="onclosecallback"></a>

### OnCloseCallback

用户点击 `关闭广告` 按钮的事件的回调函数

```tsx
(result: OnCloseCallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `OnCloseCallbackResult` |

<a id="onerrorcallback"></a>

### OnErrorCallback

激励视频错误事件的回调函数

```tsx
(result: OnErrorCallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `OnErrorCallbackResult` |

<a id="onloadcallback"></a>

### OnLoadCallback

激励视频广告加载事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="api-支持度-9"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RewardedVideoAd.load | ✔️ |  |  |
| RewardedVideoAd.show | ✔️ |  |  |
| RewardedVideoAd.destroy | ✔️ |  |  |
| RewardedVideoAd.offClose | ✔️ |  |  |
| RewardedVideoAd.offError | ✔️ |  |  |
| RewardedVideoAd.offLoad | ✔️ |  |  |
| RewardedVideoAd.onClose | ✔️ |  |  |
| RewardedVideoAd.onError | ✔️ |  |  |
| RewardedVideoAd.onLoad | ✔️ |  |  |
