# Taro.previewImage(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/image/previewImage)

在新页面中全屏预览图片。预览的过程中用户可以进行保存图片、发送给朋友等操作。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/image/wx.previewImage.html)

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
| urls | `string[]` | 是 | 需要预览的图片链接列表。 |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| current | `string` | 否 | 当前显示图片的链接 |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.previewImage({
  current: '', // 当前显示图片的http链接
  urls: [] // 需要预览的图片http链接列表
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | H5 | React Native |
| --- | --- | --- | --- | --- | --- |
| Taro.previewImage | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
