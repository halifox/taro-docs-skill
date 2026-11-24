# Taro.chooseImage(OBJECT)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/multimedia/images/chooseImage)

使用方式同 [`wx.chooseImage`](https://developers.weixin.qq.com/miniprogram/dev/api/wx.chooseImage.html) ，支持 `Promise` 化使用。

注：RN 端该 API 不支持 `count` 属性；不支持相机与相册同时选择，只会取 `sourceType` 数组里的第一个值。默认从相册选取图片。

<a id="参数"></a>

## 参数

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| object | `Object` |  | 参数 |
| [object.sourceType] | `Array.<string>` | `['album', 'camera']` | 选择图片的来源（h5端未实现） |
| [object.sizeType] | `Array.<string>` | `['original', 'compressed']` | 所选的图片的尺寸（h5端未实现） |
| [object.count] | `number` | `9` | 最多可以选择的图片张数 |
| [object.success] | `function` |  | 接口调用成功的回调函数 |
| [object.fail] | `function` |  | 接口调用失败的回调函数 |
| [object.complete] | `function` |  | 接口调用结束的回调函数（调用成功、失败都会执行） |
| [object.imageId] | `string` |  | 用来上传的input元素ID（仅h5端） |

<a id="返回值"></a>

## 返回值

<a id="promise-object-res"></a>

### Promise <object res>

| Name | Type | Description |
| --- | --- | --- |
| res.tempFilePaths | `Array.<string>` | 图片的本地临时文件路径列表 |
| res.tempFiles | `Array.<Object>` | 图片的本地临时文件列表 |

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.chooseImage(params).then(...)
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native | 支付宝小程序 | 百度小程序 |
| --- | --- | --- | --- | --- | --- |
| Taro.chooseImage | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
