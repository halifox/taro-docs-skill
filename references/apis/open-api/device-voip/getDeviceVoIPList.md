# Taro.getDeviceVoIPList(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/open-api/device-voip/getDeviceVoIPList)

查询当前用户授权的音视频通话设备（组）信息

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/device-voip/wx.getDeviceVoIPList.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<SuccessCallbackResult>
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
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 |
| --- | --- |
| list | `DeviceVoIP[]` |

<a id="devicevoip"></a>

### DeviceVoIP

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| sn | `string` | 设备唯一序列号。（仅单台设备时） |
| model\_id | `string` | 设备型号 id。通过微信公众平台注册设备获得。（仅单台设备时） |
| group\_id | `string` | 设备组的唯一标识 id（仅设备组时） |
| status | `number` | 设备（组）授权状态。0：未授权；1：已授权 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getDeviceVoIPList({
  success(res) {
    console.log(res)
  },
  fail(res) {
    console.log(res)
  }
})
```
