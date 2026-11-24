# Taro.startBeaconDiscovery(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/iBeacon/startBeaconDiscovery)

开始搜索附近的 iBeacon 设备

支持情况：微信小程序 支付宝小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/ibeacon/wx.startBeaconDiscovery.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<TaroGeneral.IBeaconError>
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
| uuids | `string[]` |  | 是 | iBeacon 设备广播的 uuid 列表 |
| complete | `(res: TaroGeneral.IBeaconError) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.IBeaconError) => void` |  | 否 | 接口调用失败的回调函数 |
| ignoreBluetoothAvailable | `boolean` | `false` | 否 | 是否校验蓝牙开关，仅在 iOS 下有效 |
| success | `(res: TaroGeneral.IBeaconError) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.startBeaconDiscovery({
  success: function (res) { }
})
```
