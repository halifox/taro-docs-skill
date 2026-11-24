# Taro.onLocationChangeError(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/location/onLocationChangeError)

监听持续定位接口返回失败时触发

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/location/wx.onLocationChangeError.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 监听持续定位接口返回失败时触发的回调函数 |

<a id="callback"></a>

### Callback

监听持续定位接口返回失败时触发的回调函数

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
| errCode | `number` | 是 | 错误码 |
| errMsg | `string` | 否 | 错误信息<br>API 支持度: tt<br>tt: 最低支持版本 2.48.0 |
