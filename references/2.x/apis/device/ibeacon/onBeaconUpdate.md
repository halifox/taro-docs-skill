# Taro.onBeaconUpdate(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/device/ibeacon/onBeaconUpdate)

监听 iBeacon 设备更新事件，仅能注册一个监听

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/ibeacon/wx.onBeaconUpdate.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

<a id="callback"></a>

### Callback

iBeacon 设备更新事件的回调函数

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
| beacons | `IBeaconInfo[]` | 当前搜寻到的所有 iBeacon 设备列表 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.onBeaconUpdate | ✔️ |  |  |
