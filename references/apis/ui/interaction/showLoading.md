# Taro.showLoading(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/ui/interaction/showLoading)

显示 loading 提示框。需主动调用 Taro.hideLoading 才能关闭提示框

**注意**

- Taro.showLoading 和 Taro.showToast 同时只能显示一个
- Taro.showLoading 应与 Taro.hideLoading 配对使用

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/interaction/wx.showLoading.html)

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
| title | `string` | 是 | 提示的内容 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| mask | `boolean` | 否 | 是否显示透明蒙层，防止触摸穿透 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.showLoading({
  title: '加载中',
})
setTimeout(function () {
  Taro.hideLoading()
}, 2000)
```
