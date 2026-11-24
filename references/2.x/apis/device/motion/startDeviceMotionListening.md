# Taro.startDeviceMotionListening(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/device/motion/startDeviceMotionListening)

开始监听设备方向的变化。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/motion/wx.startDeviceMotionListening.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => void
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| interval | `"game" \| "ui" \| "normal"` | `"normal"` | 否 | 监听设备方向的变化回调函数的执行频率 |
| success | `(res: CallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="interval"></a>

### interval

| 参数 | 说明 |
| --- | --- |
| game | 适用于更新游戏的回调频率，在 20ms/次 左右 |
| ui | 适用于更新 UI 的回调频率，在 60ms/次 左右 |
| normal | 普通的回调频率，在 200ms/次 左右 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.startDeviceMotionListening | ✔️ | ✔️ | ✔️ |
