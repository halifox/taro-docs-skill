# Taro.onAccelerometerChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/accelerometer/onAccelerometerChange)

监听加速度数据，频率：5次/秒，接口调用后会自动开始监听，可使用 `Taro.stopAccelerometer` 停止监听。

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/accelerometer/wx.onAccelerometerChange.html)

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

```tsx
(res: Result) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `Result` |

<a id="result"></a>

### Result

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| x | `number` | X 轴 |
| y | `number` | Y 轴 |
| z | `number` | Z 轴 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.onAccelerometerChange(res => {
  console.log(res.x)
  console.log(res.y)
  console.log(res.z)
})
```
