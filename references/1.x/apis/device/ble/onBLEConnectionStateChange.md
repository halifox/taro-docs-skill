# Taro.onBLEConnectionStateChange(CALLBACK)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/device/ble/onBLEConnectionStateChange)

使用方式同 [`wx.onBLEConnectionStateChange`](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth/wx.onBLEConnectionStateChange.html)。

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.onBLEConnectionStateChange(res => {
  // 该方法回调中可以用于处理连接意外断开等异常情况
  console.log(`device ${res.deviceId} state has changed, connected: ${res.connected}`)
})
```
