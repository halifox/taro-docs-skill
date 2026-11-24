# Taro.getBatteryInfoSync()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/battery/getBatteryInfoSync)

Taro.getBatteryInfo 的同步版本

支持情况：微信小程序 百度小程序 支付宝小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/battery/wx.getBatteryInfoSync.html)

<a id="类型"></a>

## 类型

```tsx
() => Result
```

<a id="参数"></a>

## 参数

<a id="result"></a>

### Result

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| isCharging | `boolean` | 是否正在充电中 |
| level | `number` | 设备电量，范围 1 - 100 |
