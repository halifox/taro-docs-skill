# Taro.setBackgroundColor(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/ui/background/setBackgroundColor)

动态设置窗口的背景色

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> React Native: 仅 Android

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/background/wx.setBackgroundColor.html)

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
| backgroundColor | `string` | 否 | 窗口的背景色，必须为十六进制颜色值 |
| backgroundColorBottom | `string` | 否 | 底部窗口的背景色，必须为十六进制颜色值，仅 iOS 支持 |
| backgroundColorTop | `string` | 否 | 顶部窗口的背景色，必须为十六进制颜色值，仅 iOS 支持 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.setBackgroundColor({
  backgroundColor: '#ffffff', // 窗口的背景色为白色
})
Taro.setBackgroundColor({
  backgroundColorTop: '#ffffff', // 顶部窗口的背景色为白色
  backgroundColorBottom: '#ffffff', // 底部窗口的背景色为白色
})
```
