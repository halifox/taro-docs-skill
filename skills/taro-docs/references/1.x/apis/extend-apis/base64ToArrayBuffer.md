# base64ToArrayBuffer

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/extend-apis/base64ToArrayBuffer)

将 Base64 字符串转成 ArrayBuffer 数据。(小程序端基础库 1.1.0 开始支持，低版本需做兼容处理)

**示例代码：**

```jsx
import Taro from '@tarojs/taro'

const base64 = 'CxYh'
const arrayBuffer = Taro.base64ToArrayBuffer(base64)
```

> API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.arrayBufferToBase64 | ✔️ | ✔️ |  |
| Taro.base64ToArrayBuffer | ✔️ | ✔️ |  |
