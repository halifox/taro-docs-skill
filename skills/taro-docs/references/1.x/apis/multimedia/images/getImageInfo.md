# Taro.getImageInfo(OBJECT)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/multimedia/images/getImageInfo)

获取图片信息。网络图片需先配置download域名才能生效。

使用方式同 [`wx.getImageInfo`](https://developers.weixin.qq.com/miniprogram/dev/api/wx.getImageInfo.html)，支持 `Promise` 化使用。

<a id="参数"></a>

## 参数

| Property | Type | Description |
| --- | --- | --- |
| src | `string` | 图片的路径，可以是相对路径、临时文件路径、存储文件路径、网络图片路径 |
| [success] | `function` | 接口调用成功的回调函数 |
| [fail] | `function` | 接口调用失败的回调函数 |
| [complete] | `function` | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="返回值"></a>

## 返回值

<a id="promise-object-res"></a>

### Promise <object res>

| Name | Type | Description |
| --- | --- | --- |
| res.width | `number` | 图片原始宽度，单位px。不考虑旋转。 |
| res.height | `number` | 图片原始高度，单位px。不考虑旋转。 |
| res.path | `string` | 图片的本地路径 |
| res.orientation | `'up'` / `'up-mirrored'` / `'down'` / `'down-mirrored'` / `'left-mirrored'` / `'right'` / `'right-mirrored'` / `'left'` | 拍照时设备方向（h5平台不支持） |
| res.type | `string` | 图片格式 |

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.getImageInfo(params).then(...)
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native | 支付宝小程序 | 百度小程序 |
| --- | --- | --- | --- | --- | --- |
| Taro.getImageInfo | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
