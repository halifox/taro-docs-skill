# Taro.getScreenBrightness(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/device/screen/getScreenBrightness)

获取屏幕亮度。

**说明**

- 若安卓系统设置中开启了自动调节亮度功能，则屏幕亮度会根据光线自动调整，该接口仅能获取自动调节亮度之前的值，而非实时的亮度值。

支持情况：微信小程序 百度小程序 支付宝小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/screen/wx.getScreenBrightness.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => Promise<SuccessCallbackOption>
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
| success | `(option: SuccessCallbackOption) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackoption"></a>

### SuccessCallbackOption

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| value | `number` | 屏幕亮度值，范围 0 ~ 1，0 最暗，1 最亮 |
