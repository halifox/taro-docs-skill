# Taro.onBLECharacteristicValueChange(CALLBACK)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/device/ble/onBLECharacteristicValueChange)

使用方式同 [`wx.onBLECharacteristicValueChange`](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth/wx.onBLECharacteristicValueChange.html)。

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.onBLECharacteristicValueChange(res => {
  console.log(`characteristic ${res.characteristicId} has changed, now is ${res.value}`)
  console.log(res.value)
})
```

> API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.openBluetoothAdapter | ✔️ |  |  |
| Taro.closeBluetoothAdapter | ✔️ |  |  |
| Taro.getBluetoothAdapterState | ✔️ |  |  |
| Taro.onBluetoothAdapterStateChange | ✔️ |  |  |
| Taro.startBluetoothDevicesDiscovery | ✔️ |  |  |
| Taro.stopBluetoothDevicesDiscovery | ✔️ |  |  |
| Taro.getBluetoothDevices | ✔️ |  |  |
| Taro.getConnectedBluetoothDevices | ✔️ |  |  |
| Taro.onBluetoothDeviceFound | ✔️ |  |  |
| Taro.createBLEConnection | ✔️ |  |  |
| Taro.closeBLEConnection | ✔️ |  |  |
| Taro.getBLEDeviceServices | ✔️ |  |  |
| Taro.getBLEDeviceCharacteristics | ✔️ |  |  |
| Taro.readBLECharacteristicValue | ✔️ |  |  |
| Taro.writeBLECharacteristicValue | ✔️ |  |  |
| Taro.notifyBLECharacteristicValueChange | ✔️ |  |  |
| Taro.onBLEConnectionStateChange | ✔️ |  |  |
| Taro.onBLECharacteristicValueChange | ✔️ |  |  |
