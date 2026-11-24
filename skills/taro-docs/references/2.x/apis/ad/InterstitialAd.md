# InterstitialAd

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/ad/InterstitialAd)

插屏广告组件。插屏广告组件是一个原生组件，层级比普通组件高。插屏广告组件每次创建都会返回一个全新的实例（小程序端的插屏广告实例不允许跨页面使用），默认是隐藏的，需要调用 InterstitialAd.show() 将其显示。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/InterstitialAd.html)

<a id="方法"></a>

## 方法

<a id="destroy"></a>

### destroy

销毁插屏广告实例。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/InterstitialAd.destroy.html)

```tsx
() => void
```

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| InterstitialAd.destroy | ✔️ |  |  |

<a id="offclose"></a>

### offClose

取消监听插屏广告关闭事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/InterstitialAd.offClose.html)

```tsx
(callback: OffCloseCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OffCloseCallback` |

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| InterstitialAd.offClose | ✔️ |  |  |

<a id="offerror"></a>

### offError

取消监听插屏错误事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/InterstitialAd.offError.html)

```tsx
(callback: OffErrorCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OffErrorCallback` |

<a id="api-支持度-2"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| InterstitialAd.offError | ✔️ |  |  |

<a id="offload"></a>

### offLoad

取消监听插屏广告加载事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/InterstitialAd.offLoad.html)

```tsx
(callback: OffLoadCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OffLoadCallback` |

<a id="api-支持度-3"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| InterstitialAd.offLoad | ✔️ |  |  |

<a id="onclose"></a>

### onClose

监听插屏广告关闭事件。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/InterstitialAd.onClose.html)

```tsx
(callback: OnCloseCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnCloseCallback` |

<a id="api-支持度-4"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| InterstitialAd.onClose | ✔️ |  |  |

<a id="onerror"></a>

### onError

监听插屏错误事件。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/InterstitialAd.onError.html)

```tsx
(callback: OnErrorCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnErrorCallback` |

<a id="api-支持度-5"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| InterstitialAd.onError | ✔️ |  |  |

<a id="onload"></a>

### onLoad

监听插屏广告加载事件。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/InterstitialAd.onLoad.html)

```tsx
(callback: OnLoadCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnLoadCallback` |

<a id="api-支持度-6"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| InterstitialAd.onLoad | ✔️ |  |  |

<a id="load"></a>

### load

加载插屏广告。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/InterstitialAd.load.html)

```tsx
() => Promise<any>
```

<a id="api-支持度-7"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| InterstitialAd.load | ✔️ |  |  |

<a id="show"></a>

### show

显示插屏广告。

**错误码信息表**

如果插屏广告显示失败，InterstitialAd.show() 方法会返回一个rejected Promise，开发者可以获取到错误码及对应的错误信息。

| 代码 | 异常情况 | 理由 |
| --- | --- | --- |
| 2001 | 触发频率限制 | 小程序启动一定时间内不允许展示插屏广告 |
| 2002 | 触发频率限制 | 距离小程序插屏广告或者激励视频广告上次播放时间间隔不足，不允许展示插屏广告 |
| 2003 | 触发频率限制 | 当前正在播放激励视频广告或者插屏广告，不允许再次展示插屏广告 |
| 2004 | 广告渲染失败 | 该项错误不是开发者的异常情况，或因小程序页面切换导致广告渲染失败 |
| 2005 | 广告调用异常 | 插屏广告实例不允许跨页面调用 |

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/InterstitialAd.show.html)

```tsx
() => Promise<any>
```

<a id="api-支持度-8"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| InterstitialAd.show | ✔️ |  |  |

<a id="参数"></a>

## 参数

<a id="offclosecallback"></a>

### OffCloseCallback

插屏广告关闭事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="offerrorcallback"></a>

### OffErrorCallback

插屏错误事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="offloadcallback"></a>

### OffLoadCallback

插屏广告加载事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="onclosecallback"></a>

### OnCloseCallback

插屏广告关闭事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="onerrorcallback"></a>

### OnErrorCallback

插屏错误事件的回调函数

```tsx
(result: OnErrorCallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `OnErrorCallbackResult` |

<a id="onloadcallback"></a>

### OnLoadCallback

插屏广告加载事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="onerrorcallbackresult"></a>

### OnErrorCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errCode | `1000 \| 1001 \| 1002 \| 1003 \| 1004 \| 1005 \| 1006 \| 1007 \| 1008` | 错误码<br>[参考地址](../../../apis/General.md#aderrcode) |
| errMsg | `string` | 错误信息 |

<a id="api-支持度-9"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| InterstitialAd.destroy | ✔️ |  |  |
| InterstitialAd.offClose | ✔️ |  |  |
| InterstitialAd.offError | ✔️ |  |  |
| InterstitialAd.offLoad | ✔️ |  |  |
| InterstitialAd.onClose | ✔️ |  |  |
| InterstitialAd.onError | ✔️ |  |  |
| InterstitialAd.onLoad | ✔️ |  |  |
| InterstitialAd.load | ✔️ |  |  |
| InterstitialAd.show | ✔️ |  |  |
