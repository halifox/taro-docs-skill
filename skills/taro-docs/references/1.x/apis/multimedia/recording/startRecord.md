# Taro.startRecord(OBJECT)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/multimedia/recording/startRecord)

使用方式同 [`wx.startRecord`](https://developers.weixin.qq.com/miniprogram/dev/api/wx.startRecord.html)，支持 `Promise` 化使用。

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.startRecord(params).then(...)
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native | 支付宝小程序 | 百度小程序 |
| --- | --- | --- | --- | --- | --- |
| Taro.startRecord | ✔️ |  |  |  |  |

## 录音管理

使用方式同 [`wx.getRecorderManager`](https://developers.weixin.qq.com/miniprogram/dev/api/wx.getRecorderManager.html)。

**示例代码：**

> API 支持度

| API | 微信小程序 | H5 | React Native | 支付宝小程序 | 百度小程序 |
| --- | --- | --- | --- | --- | --- |
