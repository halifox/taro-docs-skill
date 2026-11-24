# Taro.onBLEConnectionStateChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/device/bluetooth-ble/onBLEConnectionStateChange)

监听低功耗蓝牙连接状态的改变事件。包括开发者主动连接或断开连接，设备丢失，连接异常断开等等

支持情况：微信小程序 支付宝小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-ble/wx.onBLEConnectionStateChange.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 低功耗蓝牙连接状态的改变事件的回调函数 |

<a id="callbackresult"></a>

### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| connected | `boolean` | 是否处于已连接状态 |
| deviceId | `string` | 蓝牙设备ID |

<a id="callback"></a>

### Callback

低功耗蓝牙连接状态的改变事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.onBLEConnectionStateChange(function (res) {
  // 该方法回调中可以用于处理连接意外断开等异常情况
  console.log(`device ${res.deviceId} state has changed, connected: ${res.connected}`)
})
```
