# Taro.stopLocationUpdate(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/location/stopLocationUpdate)

关闭监听实时位置变化，前后台都停止消息接收

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/location/wx.stopLocationUpdate.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => void
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.stopLocationUpdate | ✔️ |  |  |
