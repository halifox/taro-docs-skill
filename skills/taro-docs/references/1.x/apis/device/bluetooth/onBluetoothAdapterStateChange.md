# Taro.onBluetoothAdapterStateChange(CALLBACK)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/device/bluetooth/onBluetoothAdapterStateChange)

使用方式同 [`wx.onBluetoothAdapterStateChange`](https://developers.weixin.qq.com/miniprogram/dev/api/wx.onBluetoothAdapterStateChange.html)。

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.onBluetoothAdapterStateChange(res => {
  console.log(`adapterState changed, now is`, res)
})
```
