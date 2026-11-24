# Taro.setBLEMTU(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/bluetooth-ble/setBLEMTU)

协商设置蓝牙低功耗的最大传输单元 (Maximum Transmission Unit, MTU)

- 需在 Taro.createBLEConnection 调用成功后调用
- 仅安卓系统 5.1 以上版本有效，iOS 因系统限制不支持。

支持情况：微信小程序 支付宝小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-ble/wx.setBLEMTU.html)

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

```tsx
FailCallbackResult | SuccessCallbackResult
```

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| deviceId | `string` | 是 | 蓝牙设备 id |
| mtu | `number` | 是 | 最大传输单元。设置范围为 (22,512) 区间内，单位 bytes |
| complete | `(res: Promised) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: FailCallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="failcallbackresult"></a>

### FailCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| mtu | `string` | 最终协商的 MTU 值。如果协商失败则无此参数。安卓客户端 8.0.9 开始支持。 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| mtu | `string` | 最终协商的 MTU 值，与传入参数一致。安卓客户端 8.0.9 开始支持。 |
