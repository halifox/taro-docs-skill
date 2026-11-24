# Taro.onBluetoothAdapterStateChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/device/bluetooth/onBluetoothAdapterStateChange)

监听蓝牙适配器状态变化事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth/wx.onBluetoothAdapterStateChange.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

<a id="callback"></a>

### Callback

蓝牙适配器状态变化事件的回调函数

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
| available | `boolean` | 蓝牙适配器是否可用 |
| discovering | `boolean` | 蓝牙适配器是否处于搜索状态 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.onBluetoothAdapterStateChange(function (res) {
  console.log('adapterState changed, now is', res)
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.onBluetoothAdapterStateChange | ✔️ |  |  |
