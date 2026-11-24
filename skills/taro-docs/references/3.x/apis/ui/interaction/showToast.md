# Taro.showToast(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/ui/interaction/showToast)

显示消息提示框

**注意**

- Taro.showLoading 和 Taro.showToast 同时只能显示一个
- Taro.showToast 应与 Taro.hideToast 配对使用

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/interaction/wx.showToast.html)

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
| duration | `number` | 否 | 提示的延迟时间 |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| icon | "success" or "error" or "loading" or "none" | 否 | 图标<br><br>可选值：<br>- 'success': 显示成功图标，此时 title 文本最多显示 7 个汉字长度;<br>- 'error': 显示失败图标，此时 title 文本最多显示 7 个汉字长度;<br>- 'loading': 显示加载图标，此时 title 文本最多显示 7 个汉字长度;<br>- 'none': 不显示图标，此时 title 文本最多可显示两行 |
| image | `string` | 否 | 自定义图标的本地路径，image 的优先级高于 icon |
| mask | `boolean` | 否 | 是否显示透明蒙层，防止触摸穿透 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.showToast({
  title: '成功',
  icon: 'success',
  duration: 2000
})
```
