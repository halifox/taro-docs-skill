# Taro.getSystemInfoSync()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/device/systeminfo/getSystemInfoSync)

获取系统信息同步接口。

**同步返回参数说明：**

| 参数 | 说明 |
| --- | --- |
| brand | 手机品牌 |
| model | 手机型号 |
| system | 操作系统版本 |
| pixelRatio | 设备像素比 |
| screenWidth | 屏幕宽度 |
| screenHeight | 屏幕高度 |
| windowWidth | 可使用窗口宽度 |
| windowHeight | 可使用窗口高度 |
| version | 微信版本号 |
| statusBarHeight | 状态栏的高度 |
| platform | 客户端平台 |
| language | 微信设置的语言 |
| fontSizeSetting | 用户字体大小设置。以“我-设置-通用-字体大小”中的设置为准，单位：px |
| SDKVersion | 客户端基础库版本 |

注意：**H5** 端不支持 version、statusBarHeight、fontSizeSetting、SDKVersion

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

const res = Taro.getSystemInfoSync()
console.log(res.model)
console.log(res.pixelRatio)
console.log(res.windowWidth)
console.log(res.windowHeight)
console.log(res.language)
console.log(res.version)
console.log(res.platform)
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.getSystemInfoSync | ✔️ | ✔️ | ✔️ |
