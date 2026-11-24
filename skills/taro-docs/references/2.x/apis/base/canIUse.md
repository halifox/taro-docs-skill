# Taro.canIUse(schema)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/base/canIUse)

判断小程序的 API，回调，参数，组件等是否在当前版本可用。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/wx.canIUse.html)

<a id="类型"></a>

## 类型

```tsx
(schema: string) => boolean
```

<a id="参数"></a>

## 参数

使用 `${API}.${method}.${param}.${option}` 或者 `${component}.${attribute}.${option}` 方式来调用

**参数说明**

- `${API}` 代表 API 名字  
- `${method}` 代表调用方式，有效值为return, success, object, callback  
- `${param}` 代表参数或者返回值  
- `${option}` 代表参数的可选值或者返回值的属性  
- `${component}` 代表组件名字  
- `${attribute}` 代表组件属性  
- `${option}` 代表组件属性的可选值

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

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.canIUse | ✔️ |  |  |
