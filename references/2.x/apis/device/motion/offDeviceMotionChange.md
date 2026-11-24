# Taro.offDeviceMotionChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/device/motion/offDeviceMotionChange)

取消监听设备方向变化事件，参数为空，则取消所有的事件监听。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/motion/wx.offDeviceMotionChange.html)

<a id="类型"></a>

## 类型

```tsx
(callback: (...args: any[]) => any) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `(...args: any[]) => any` | 设备方向变化事件的回调函数 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.offDeviceMotionChange | ✔️ |  |  |
