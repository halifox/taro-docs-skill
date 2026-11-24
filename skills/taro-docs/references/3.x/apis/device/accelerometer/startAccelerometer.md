# Taro.startAccelerometer(res)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/device/accelerometer/startAccelerometer)

开始监听加速度数据。

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/accelerometer/wx.startAccelerometer.html)

<a id="类型"></a>

## 类型

```tsx
(res?: Option) => Promise<TaroGeneral.CallbackResult>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| res | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| interval | `keyof Interval` | `"normal"` | 否 | 监听加速度数据回调函数的执行频率 |
| complete | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="interval"></a>

### Interval

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| game | `"game"` | 适用于更新游戏的回调频率，在 20ms/次 左右 |
| ui | `"ui"` | 适用于更新 UI 的回调频率，在 60ms/次 左右 |
| normal | `"normal"` | 普通的回调频率，在 200ms/次 左右 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.startAccelerometer({ interval: 'game' })
```
