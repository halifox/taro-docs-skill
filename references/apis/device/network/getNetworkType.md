# Taro.getNetworkType(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/network/getNetworkType)

获取网络类型。

支持情况：微信小程序 百度小程序 抖音小程序 QQ 小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/network/wx.getNetworkType.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => Promise<SuccessCallbackResult>
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

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| networkType | `keyof NetworkType` | 是 | 网络类型 |
| signalStrength | `number` | 否 | 信号强弱，单位 dbm |
| hasSystemProxy | `boolean` | 否 | 设备是否使用了网络代理 |
| errMsg | `string` | 是 | 调用结果 |

<a id="networktype"></a>

### NetworkType

网络类型

| 参数 | 说明 |
| --- | --- |
| wifi | wifi 网络 |
| 2g | 2g 网络 |
| 3g | 3g 网络 |
| 4g | 4g 网络 |
| 5g | 5g 网络 |
| unknown | Android 下不常见的网络类型 |
| none | 无网络 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getNetworkType({
  success: function (res) {
    // 返回网络类型, 有效值：
    // wifi/2g/3g/4g/unknown(Android下不常见的网络类型)/none(无网络)
    var networkType = res.networkType
  }
})
```
