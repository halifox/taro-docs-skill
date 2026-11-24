# Taro.getSystemSetting()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/base/system/getSystemSetting)

获取设备设置

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> H5: 不支持 bluetoothEnabled、locationEnabled、wifiEnabled

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/system/wx.getSystemSetting.html)

<a id="类型"></a>

## 类型

```tsx
() => Result
```

<a id="参数"></a>

## 参数

<a id="result"></a>

### Result

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| bluetoothEnabled | `boolean` | 否 | 蓝牙的系统开关 |
| locationEnabled | `boolean` | 否 | 地理位置的系统开关 |
| wifiEnabled | `boolean` | 否 | Wi-Fi 的系统开关 |
| deviceOrientation | `keyof DeviceOrientation` | 否 | 设备方向 |

<a id="deviceorientation"></a>

### DeviceOrientation

设备方向合法值

| 参数 | 说明 |
| --- | --- |
| portrait | 竖屏 |
| landscape | 横屏 |

<a id="示例代码"></a>

## 示例代码

```tsx
const systemSetting = Taro.getSystemSetting()

console.log(systemSetting.bluetoothEnabled)
console.log(systemSetting.deviceOrientation)
console.log(systemSetting.locationEnabled)
console.log(systemSetting.wifiEnabled)
```
