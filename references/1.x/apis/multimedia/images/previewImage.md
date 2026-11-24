# Taro.previewImage(param)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/multimedia/images/previewImage)

在新页面中全屏预览图片。预览的过程中用户可以进行保存图片、发送给朋友等操作。

使用方式同 [`wx.previewImage`](https://developers.weixin.qq.com/miniprogram/dev/api/wx.previewImage.html)，支持 `Promise` 化使用。

<a id="参数"></a>

## 参数

<a id="object-param"></a>

### object param

| Property | Type | Default | Description |
| --- | --- | --- | --- |
| urls | `Array.<string>` |  | 需要预览的图片链接列表。 |
| [current] | `string` | `"urls[0]"` | urls的第一张 当前显示图片的链接 |
| [success] | `function` |  | 接口调用成功的回调函数 |
| [fail] | `function` |  | 接口调用失败的回调函数 |
| [complete] | `function` |  | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.previewImage(params).then(...)
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native | 支付宝小程序 | 百度小程序 |
| --- | --- | --- | --- | --- | --- |
| Taro.previewImage | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
