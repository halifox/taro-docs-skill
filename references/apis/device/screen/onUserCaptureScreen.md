# Taro.onUserCaptureScreen(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/screen/onUserCaptureScreen)

监听用户主动截屏事件，用户使用系统截屏按键截屏时触发此事件

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/screen/wx.onUserCaptureScreen.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 用户主动截屏事件的回调函数 |

<a id="callback"></a>

### Callback

用户主动截屏事件的回调函数

```tsx
(result: TaroGeneral.CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `TaroGeneral.CallbackResult` |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.onUserCaptureScreen(function (res) {
    console.log('用户截屏了')
})
```
