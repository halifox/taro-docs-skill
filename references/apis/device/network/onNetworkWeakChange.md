# Taro.onNetworkWeakChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/network/onNetworkWeakChange)

监听弱网状态变化事件

支持情况：微信小程序 百度小程序 抖音小程序 QQ 小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/network/wx.onNetworkWeakChange.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 弱网状态变化事件的回调函数 |

<a id="callback"></a>

### Callback

弱网状态变化事件的回调函数

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
| weakNet | `boolean` | 当前是否处于弱网状态 |
| networkType | `keyof NetworkType` | 当前网络类型 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.onNetworkWeakChange(function (res) {
  console.log(res.weakNet)
  console.log(res.networkType)
})
// 取消监听
Taro.offNetworkWeakChange()
```
