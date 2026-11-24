# Taro.onBLEMTUChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/device/bluetooth-ble/onBLEMTUChange)

监听蓝牙低功耗的最大传输单元变化事件（仅安卓触发）

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-ble/wx.onBLEMTUChange.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 蓝牙低功耗的最大传输单元变化事件的回调函数 |

<a id="callbackresult"></a>

### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| deviceId | `string` | 蓝牙设备ID |
| mtu | `string` | 最大传输单元 |

<a id="callback"></a>

### Callback

蓝牙低功耗的最大传输单元变化事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.onBLEMTUChange(function (res) {
  console.log('bluetooth mtu is', res.mtu)
})
```
