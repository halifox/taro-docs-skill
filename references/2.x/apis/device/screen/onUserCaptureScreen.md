# Taro.onUserCaptureScreen(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/device/screen/onUserCaptureScreen)

监听用户主动截屏事件，用户使用系统截屏按键截屏时触发此事件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/screen/wx.onUserCaptureScreen.html)

<a id="类型"></a>

## 类型

```tsx
(callback: (res: CallbackResult) => void) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `(res: CallbackResult) => void` | 用户主动截屏事件的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.onUserCaptureScreen(function (res) {
    console.log('用户截屏了')
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.onUserCaptureScreen | ✔️ |  |  |
