# Taro.getConnectedBluetoothDevices(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/device/bluetooth/getConnectedBluetoothDevices)

根据 uuid 获取处于已连接状态的设备。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth/wx.getConnectedBluetoothDevices.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => void
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| services | `string[]` | 是 | 蓝牙设备主 service 的 uuid 列表 |
| complete | `(res: BluetoothError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: BluetoothError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| devices | `BluetoothDeviceInfo[]` | 搜索到的设备列表 |
| errMsg | `string` | 成功：ok，错误：详细信息 |

<a id="bluetoothdeviceinfo"></a>

### BluetoothDeviceInfo

搜索到的设备

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| deviceId | `string` | 用于区分设备的 id |
| name | `string` | 蓝牙设备名称，某些设备可能没有 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getConnectedBluetoothDevices({
  success: function (res) {
    console.log(res)
  }
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.getConnectedBluetoothDevices | ✔️ |  |  |
