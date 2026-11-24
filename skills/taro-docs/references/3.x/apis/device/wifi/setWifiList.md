# Taro.setWifiList(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/device/wifi/setWifiList)

设置 `wifiList` 中 AP 的相关信息。在 `onGetWifiList` 回调后调用，**iOS特有接口**。

**注意**

- 该接口只能在 `onGetWifiList` 回调之后才能调用。
- 此时客户端会挂起，等待小程序设置 Wi-Fi 信息，请务必尽快调用该接口，若无数据请传入一个空数组。
- 有可能随着周边 Wi-Fi 列表的刷新，单个流程内收到多次带有存在重复的 Wi-Fi 列表的回调。

支持情况：微信小程序 百度小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/wifi/wx.setWifiList.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<TaroGeneral.WifiError>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| wifiList | `WifiData[]` | 是 | 提供预设的 Wi-Fi 信息列表 |
| complete | `(res: TaroGeneral.WifiError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.WifiError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.WifiError) => void` | 否 | 接口调用成功的回调函数 |

<a id="wifidata"></a>

### WifiData

提供预设的 Wi-Fi 信息列表

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| BSSID | `string` | 否 | Wi-Fi 的 BSSID |
| SSID | `string` | 否 | Wi-Fi 的 SSID |
| password | `string` | 否 | Wi-Fi 设备密码 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.onGetWifiList(function (res) {
  if (res.wifiList.length) {
    Taro.setWifiList({
      wifiList: [{
        SSID: res.wifiList[0].SSID,
        BSSID: res.wifiList[0].BSSID,
        password: '123456'
      }]
    })
  } else {
    Taro.setWifiList({
      wifiList: []
    })
  }
})
Taro.getWifiList()
```
