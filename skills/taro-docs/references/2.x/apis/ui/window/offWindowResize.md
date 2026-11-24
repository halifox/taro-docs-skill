# Taro.offWindowResize(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/ui/window/offWindowResize)

取消监听窗口尺寸变化事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/window/wx.offWindowResize.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

<a id="callback"></a>

### Callback

窗口尺寸变化事件的回调函数

```tsx
(res: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `CallbackResult` |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.offWindowResize | ✔️ | ✔️ |  |
