# Taro.notifyBLECharacteristicValueChange(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/bluetooth-ble/notifyBLECharacteristicValueChange)

启用低功耗蓝牙设备特征值变化时的 notify 功能，订阅特征值。注意：必须设备的特征值支持 notify 或者 indicate 才可以成功调用。

另外，必须先启用 `notifyBLECharacteristicValueChange` 才能监听到设备 `characteristicValueChange` 事件

**注意**

- 订阅操作成功后需要设备主动更新特征值的 value，才会触发 Taro.onBLECharacteristicValueChange 回调。
- 安卓平台上，在调用 `notifyBLECharacteristicValueChange` 成功后立即调用 `writeBLECharacteristicValue` 接口，在部分机型上会发生 10008 系统错误

支持情况：微信小程序 支付宝小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-ble/wx.notifyBLECharacteristicValueChange.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<Promised>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="promised"></a>

### Promised

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errMsg | `string` | 成功：ok，错误：详细信息 |

<a id="option"></a>

### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| characteristicId | `string` |  | 是 | 蓝牙特征值的 uuid |
| deviceId | `string` |  | 是 | 蓝牙设备 id |
| serviceId | `string` |  | 是 | 蓝牙特征值对应服务的 uuid |
| state | `boolean` |  | 是 | 是否启用 notify |
| type | `keyof Type` | `"indication"` | 否 | 设置特征订阅类型，有效值有 notification 和 indication |
| complete | `(res: TaroGeneral.BluetoothError) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.BluetoothError) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.BluetoothError) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="type"></a>

### Type

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.notifyBLECharacteristicValueChange({
  state: true, // 启用 notify 功能
  // 这里的 deviceId 需要已经通过 createBLEConnection 与对应设备建立链接
  deviceId,
  // 这里的 serviceId 需要在 getBLEDeviceServices 接口中获取
  serviceId,
  // 这里的 characteristicId 需要在 getBLEDeviceCharacteristics 接口中获取
  characteristicId,
  success: function (res) {
    console.log('notifyBLECharacteristicValueChange success', res.errMsg)
  }
})
```
