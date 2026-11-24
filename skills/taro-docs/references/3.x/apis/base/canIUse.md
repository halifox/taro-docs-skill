# Taro.canIUse(schema)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/base/canIUse)

判断小程序的 API，回调，参数，组件等是否在当前版本可用。

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/wx.canIUse.html)

<a id="类型"></a>

## 类型

```tsx
(schema: string) => boolean
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| schema | `string` | 使用 `${API}.${method}.${param}.${option}` 或者 `${component}.${attribute}.${option}` 方式来调用<br><br>**参数说明**<br><br>- `${API}` 代表 API 名字<br>- `${method}` 代表调用方式，有效值为return, success, object, callback<br>- `${param}` 代表参数或者返回值<br>- `${option}` 代表参数的可选值或者返回值的属性<br>- `${component}` 代表组件名字<br>- `${attribute}` 代表组件属性<br>- `${option}` 代表组件属性的可选值 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.canIUse('openBluetoothAdapter')
Taro.canIUse('getSystemInfoSync.return.screenWidth')
Taro.canIUse('getSystemInfo.success.screenWidth')
Taro.canIUse('showToast.object.image')
Taro.canIUse('onCompassChange.callback.direction')
Taro.canIUse('request.object.method.GET')
Taro.canIUse('live-player')
Taro.canIUse('text.selectable')
Taro.canIUse('button.open-type.contact')
```
