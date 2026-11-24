# Taro.closeBLEConnection(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/bluetooth-ble/closeBLEConnection)

断开与低功耗蓝牙设备的连接。

支持情况：微信小程序 支付宝小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-ble/wx.closeBLEConnection.html)

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

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| deviceId | `string` | 是 | 用于区分设备的 id |
| complete | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.closeBLEConnection({
  deviceId,
  success: function (res) {
    console.log(res)
  }
})
```
