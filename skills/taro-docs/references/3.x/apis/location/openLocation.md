# Taro.openLocation(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/location/openLocation)

使用微信内置地图查看位置

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/location/wx.openLocation.html)

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
| latitude | `number` | 是 | 纬度，范围为-90~90，负数表示南纬。使用 gcj02 国测局坐标系 |
| longitude | `number` | 是 | 经度，范围为-180~180，负数表示西经。使用 gcj02 国测局坐标系 |
| scale | `number` | 否 | 缩放比例<br>weapp: 范围 5~18，默认值18<br>alipay: 范围 3~19，默认值15 |
| name | `string` | 否 | 位置名 |
| address | `string` | 否 | 地址的详细说明 |
| ignoredApps | `any[]` | 否 | 定义在拉起的地图 App 面板中需要被屏蔽的地图类 App<br>API 支持度: swan |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getLocation({
 type: 'gcj02', //返回可以用于 Taro.openLocation的经纬度
 success: function (res) {
   const latitude = res.latitude
   const longitude = res.longitude
   Taro.openLocation({
     latitude,
     longitude,
     scale: 18
   })
 }
})
```
