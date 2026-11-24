# Taro.onLocationChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/location/onLocationChange)

监听实时地理位置变化事件，需结合 Taro.startLocationUpdateBackground、Taro.startLocationUpdate 使用。

支持情况：微信小程序 百度小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/location/wx.onLocationChange.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 实时地理位置变化事件的回调函数 |

<a id="callback"></a>

### Callback

实时地理位置变化事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="callbackresult"></a>

### CallbackResult

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| accuracy | `number` | 是 | 位置的精确度 |
| altitude | `number` | 是 | 高度，单位 m |
| horizontalAccuracy | `number` | 是 | 水平精度，单位 m |
| latitude | `number` | 是 | 纬度，范围为 -90~90，负数表示南纬 |
| longitude | `number` | 是 | 经度，范围为 -180~180，负数表示西经 |
| speed | `number` | 是 | 速度，单位 m/s |
| verticalAccuracy | `number` | 是 | 垂直精度，单位 m（Android 无法获取，返回 0） |
| street | `string` | 否 | 街道名称<br>API 支持度: swan |
| cityCode | `string` | 否 | 城市编码<br>API 支持度: swan |
| city | `string` | 否 | 城市名称<br>API 支持度: swan, tt<br>tt: iOS 不支持 |
| country | `string` | 否 | 国家<br>API 支持度: swan |
| countryCode | `string` | 否 | 国家代码<br>API 支持度: swan |
| province | `string` | 否 | 省份<br>API 支持度: swan |
| streetNumber | `string` | 否 | 街道号码<br>API 支持度: swan |
| district | `string` | 否 | 区<br>API 支持度: swan |
| isFullAccuracy | `boolean` | 否 | 是不是精确定位信息<br>API 支持度: swan |

<a id="示例代码"></a>

## 示例代码

```tsx
const _locationChangeFn = function (res) {
 console.log('location change', res)
}
Taro.onLocationChange(_locationChangeFn)
Taro.offLocationChange(_locationChangeFn)
```
