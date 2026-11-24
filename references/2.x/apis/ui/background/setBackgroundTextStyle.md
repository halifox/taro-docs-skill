# Taro.setBackgroundTextStyle(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/ui/background/setBackgroundTextStyle)

动态设置下拉背景字体、loading 图的样式

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/background/wx.setBackgroundTextStyle.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<CallbackResult>
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| textStyle | `"dark" \| "light"` | 是 | 下拉背景字体、loading 图的样式。<br><br>可选值：<br>- 'dark': dark 样式;<br>- 'light': light 样式; |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.setBackgroundTextStyle({
  textStyle: 'dark' // 下拉背景字体、loading 图的样式为dark
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.setBackgroundTextStyle | ✔️ |  |  |
