# Taro.vibrateShort(param)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/device/vibrate/vibrateShort)

使手机发生较短时间的振动（15 ms）。仅在 iPhone 7 / 7 Plus 以上及 Android 机型生效

使用方式同 [`wx.vibrateShort`](https://developers.weixin.qq.com/miniprogram/dev/api/wx.vibrateShort.html)，支持 `Promise` 化使用。

<a id="参数"></a>

## 参数

<a id="object-param"></a>

### object param

| Property | Type | Default | Description |
| --- | --- | --- | --- |
| [success] | `function` |  | 接口调用成功的回调函数 |
| [fail] | `function` |  | 接口调用失败的回调函数 |
| [complete] | `function` |  | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.vibrateShort(params).then(...)
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.vibrateShort | ✔️ | ✔️ | ✔️ |
