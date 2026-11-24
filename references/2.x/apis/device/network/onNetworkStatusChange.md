# Taro.onNetworkStatusChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/device/network/onNetworkStatusChange)

监听网络状态变化。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/network/wx.onNetworkStatusChange.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

<a id="callback"></a>

### Callback

网络状态变化事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="callbackresult"></a>

### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| isConnected | `boolean` | 当前是否有网络连接 |
| networkType | `"wifi" \| "2g" \| "3g" \| "4g" \| "unknown" \| "none"` | 网络类型 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.onNetworkStatusChange(function (res) {
  console.log(res.isConnected)
  console.log(res.networkType)
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.onNetworkStatusChange | ✔️ | ✔️ | ✔️ |
