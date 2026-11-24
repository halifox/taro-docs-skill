# RewardedVideoAd

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/ad/RewardedVideoAd)

激励视频广告组件。激励视频广告组件是一个原生组件，层级比普通组件高。激励视频广告是一个单例（小游戏端是全局单例，小程序端是页面内单例，在小程序端的单例对象不允许跨页面使用），默认是隐藏的，需要调用 RewardedVideoAd.show() 将其显示。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.html)

<a id="方法"></a>

## 方法

<a id="load"></a>

### load

加载激励视频广告。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.load.html)

```tsx
() => Promise<any>
```

<a id="show"></a>

### show

显示激励视频广告。激励视频广告将从屏幕下方推入。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.show.html)

```tsx
() => Promise<any>
```

<a id="destroy"></a>

### destroy

销毁激励视频广告实例。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.destroy.html)

```tsx
() => void
```

<a id="offclose"></a>

### offClose

取消监听用户点击 `关闭广告` 按钮的事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.offClose.html)

```tsx
(callback: OnCloseCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnCloseCallback` |

<a id="offerror"></a>

### offError

取消监听激励视频错误事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.offError.html)

```tsx
(callback: OnErrorCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnErrorCallback` |

<a id="offload"></a>

### offLoad

取消监听激励视频广告加载事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.offLoad.html)

```tsx
(callback: OnLoadCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnLoadCallback` |

<a id="onclose"></a>

### onClose

监听用户点击 `关闭广告` 按钮的事件。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.onClose.html)

```tsx
(callback: OnCloseCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnCloseCallback` |

<a id="onerror"></a>

### onError

监听激励视频错误事件。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.onError.html)

```tsx
(callback: OnErrorCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnErrorCallback` |

<a id="onload"></a>

### onLoad

监听激励视频广告加载事件。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ad/RewardedVideoAd.onLoad.html)

```tsx
(callback: OnLoadCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `OnLoadCallback` |

<a id="参数"></a>

## 参数

<a id="onerrorcallbackresult"></a>

### OnErrorCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errCode | string or number or symbol | 错误码<br>[参考地址](../../../apis/General.md#aderrcode) |
| errMsg | `string` | 错误信息 |

<a id="onclosecallbackresult"></a>

### OnCloseCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| isEnded | `boolean` | 视频是否是在用户完整观看的情况下被关闭的 |

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
(res: TaroGeneral.CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `TaroGeneral.CallbackResult` |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| RewardedVideoAd.load | ✔️ |  |  |  |  |
| RewardedVideoAd.show | ✔️ |  |  |  |  |
| RewardedVideoAd.destroy | ✔️ |  |  |  |  |
| RewardedVideoAd.offClose | ✔️ |  |  |  |  |
| RewardedVideoAd.offError | ✔️ |  |  |  |  |
| RewardedVideoAd.offLoad | ✔️ |  |  |  |  |
| RewardedVideoAd.onClose | ✔️ |  |  |  |  |
| RewardedVideoAd.onError | ✔️ |  |  |  |  |
| RewardedVideoAd.onLoad | ✔️ |  |  |  |  |
