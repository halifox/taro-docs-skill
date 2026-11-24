# Taro.getBeacons(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/device/ibeacon/getBeacons)

获取所有已搜索到的 iBeacon 设备

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/ibeacon/wx.getBeacons.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => Promise<CallbackResult>
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: IBeaconError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: IBeaconError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="callbackresult"></a>

### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| beacons | `IBeaconInfo[]` | iBeacon 设备列表 |
| errMsg | `string` | 调用结果 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.getBeacons | ✔️ |  |  |
