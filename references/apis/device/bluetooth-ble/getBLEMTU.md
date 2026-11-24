# Taro.getBLEMTU(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/bluetooth-ble/getBLEMTU)

获取蓝牙低功耗的最大传输单元。需在 [Taro.createBLEConnection](createBLEConnection.md) 调用成功后调用。

注意:

- 小程序中 MTU 为 ATT\_MTU，包含 Op-Code 和 Attribute Handle 的长度，实际可以传输的数据长度为 ATT\_MTU - 3
- iOS 系统中 MTU 为固定值；安卓系统中，MTU 会在系统协商成功之后发生改变，建议使用 [Taro.onBLEMTUChange](onBLEMTUChange.md) 监听。

支持情况：微信小程序 支付宝小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-ble/wx.getBLEMTU.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<SuccessCallbackResult>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| deviceId | `string` |  | 是 | 蓝牙设备 id |
| writeType | `keyof WriteType` | `"write"` | 否 | 写模式 （iOS 特有参数） |
| complete | `(res: TaroGeneral.BluetoothError) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.BluetoothError) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| mtu | `number` | 最大传输单元 |

<a id="writetype"></a>

### WriteType

写模式合法值

| 参数 | 说明 |
| --- | --- |
| write | 有回复写 |
| writeNoResponse | 无回复写 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getBLEMTU({
  deviceId: '',
  writeType: 'write',
  success (res) {
    console.log(res)
  }
})
```
