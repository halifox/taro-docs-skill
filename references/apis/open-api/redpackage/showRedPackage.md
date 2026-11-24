# Taro.showRedPackage(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/open-api/redpackage/showRedPackage)

拉取h5领取红包封面页。获取参考红包封面地址参考 [微信红包封面开发平台](https://cover.weixin.qq.com/cgi-bin/mmcover-bin/readtemplate?t=page/index#/doc?page=introduce)。

支持情况：微信小程序 H5 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/redpackage/wx.showRedPackage.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => Promise<TaroGeneral.CallbackResult>
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
| url | `string` | 是 | 封面地址 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |
