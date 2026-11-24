# Taro.connectWifi(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/device/wifi/connectWifi)

连接 Wi-Fi。若已知 Wi-Fi 信息，可以直接利用该接口连接。仅 Android 与 iOS 11 以上版本支持。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/wifi/wx.connectWifi.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<WifiError>
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| SSID | `string` | 是 | Wi-Fi 设备 SSID |
| password | `string` | 是 | Wi-Fi 设备密码 |
| BSSID | `string` | 否 | Wi-Fi 设备 BSSID |
| complete | `(res: WifiError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: WifiError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: WifiError) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.connectWifi({
  SSID: '',
  BSSID: '',
  success: function (res) {
    console.log(res.errMsg)
  }
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.connectWifi | ✔️ |  |  |
