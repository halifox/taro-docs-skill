# Taro.offBeaconServiceChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/device/iBeacon/offBeaconServiceChange)

取消监听 iBeacon 服务状态变化事件

支持情况：微信小程序 支付宝小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/ibeacon/wx.offBeaconServiceChange.html)

<a id="类型"></a>

## 类型

```tsx
(callback: (res: TaroGeneral.IBeaconError) => void) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `(res: TaroGeneral.IBeaconError) => void` | iBeacon 服务状态变化事件的回调函数 |
