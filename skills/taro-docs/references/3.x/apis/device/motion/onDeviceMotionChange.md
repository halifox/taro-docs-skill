# Taro.onDeviceMotionChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/device/motion/onDeviceMotionChange)

监听设备方向变化事件。频率根据 Taro.startDeviceMotionListening() 的 interval 参数。可以使用 Taro.stopDeviceMotionListening() 停止监听。

支持情况：微信小程序 百度小程序 支付宝小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/motion/wx.onDeviceMotionChange.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| callback | `Callback` |

<a id="callback"></a>

### Callback

设备方向变化事件的回调函数

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
| alpha | `number` | 当 手机坐标 X/Y 和 地球 X/Y 重合时，绕着 Z 轴转动的夹角为 alpha，范围值为 [0, 2\*PI)。逆时针转动为正。 |
| beta | `number` | 当手机坐标 Y/Z 和地球 Y/Z 重合时，绕着 X 轴转动的夹角为 beta。范围值为 [-1\*PI, PI) 。顶部朝着地球表面转动为正。也有可能朝着用户为正。 |
| gamma | `number` | 当手机 X/Z 和地球 X/Z 重合时，绕着 Y 轴转动的夹角为 gamma。范围值为 [-1\*PI/2, PI/2)。右边朝着地球表面转动为正。 |
