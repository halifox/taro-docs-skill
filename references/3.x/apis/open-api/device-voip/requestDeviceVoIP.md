# Taro.requestDeviceVoIP(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/open-api/device-voip/requestDeviceVoIP)

请求用户授权与设备（组）间进行音视频通话

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/device-voip/wx.requestDeviceVoIP.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<TaroGeneral.CallbackResult>
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
| sn | `string` | 是 | 设备唯一序列号。由厂商分配，长度不能超过128字节。字符只接受数字，大小写字母，下划线（\_）和连字符（-） |
| snTicket | `string` | 是 | 设备票据，5分钟内有效 |
| modelId | `string` | 是 | 设备型号 id。通过微信公众平台注册设备获得。 |
| deviceName | `string` | 是 | 设备名称，将显示在授权弹窗内（长度不超过13）。授权框中「设备名字」= 「deviceName」 + 「modelId 对应设备型号」 |
| isGroup | `boolean` | 否 | 是否为授权设备组，默认 false |
| groupId | `string` | 是 | 设备组的唯一标识 id 。isGroup 为 true 时只需要传该参数，isGroup 为 false 时不需要传该参数，但需要传 sn、snTicket、modelId、deviceName 。 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
// 授权单台设备
Taro.requestDeviceVoIP({
  sn: 'xxxx',
  snTicket: 'xxxxx',
  modelId: 'xxx',
  deviceName: 'xxx',
  success(res) {
    console.log(res)
  },
  fail(res) {
    console.log(res)
  }
})

// 批量授权（授权设备组）
Taro.requestDeviceVoIP({
  isGroup: true,
  groupId: '设备组 ID',
  success(res) {
    console.log(res)
  },
  fail(res) {
    console.log(res)
  }
})
```
