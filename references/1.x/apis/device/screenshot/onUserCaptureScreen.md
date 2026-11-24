# Taro.onUserCaptureScreen(CALLBACK)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/device/screenshot/onUserCaptureScreen)

监听用户主动截屏事件，用户使用系统截屏按键截屏时触发此事件。

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.onUserCaptureScreen(() => {
    console.log('用户截屏了')
})
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.onUserCaptureScreen | ✔️ |  |  |
