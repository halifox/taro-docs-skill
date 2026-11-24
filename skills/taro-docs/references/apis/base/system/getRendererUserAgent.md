# Taro.getRendererUserAgent(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/base/system/getRendererUserAgent)

获取 Webview 小程序的 UserAgent
基础库 2.26.3 开始支持

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/system/wx.getRendererUserAgent.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => Promise<Result>
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
| success | `(res: Result) => void` | 否 | 接口调用成功的回调函数 |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| complete | `(res: any) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="result"></a>

### Result

| 参数 | 类型 |
| --- | --- |
| userAgent | `string` |
