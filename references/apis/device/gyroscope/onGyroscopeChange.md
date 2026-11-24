# Taro.onGyroscopeChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/gyroscope/onGyroscopeChange)

监听陀螺仪数据变化事件。频率根据 Taro.startGyroscope() 的 interval 参数。可以使用 Taro.stopGyroscope() 停止监听。

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/gyroscope/wx.onGyroscopeChange.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 陀螺仪数据变化事件的回调函数 |

<a id="callback"></a>

### Callback

陀螺仪数据变化事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="callbackresult"></a>

### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| x | `number` | x 轴的角速度 |
| y | `number` | y 轴的角速度 |
| z | `number` | z 轴的角速度 |
