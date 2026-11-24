# Taro.chooseImage(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/media/image/chooseImage)

从本地相册选择图片或使用相机拍照。

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/image/wx.chooseImage.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<SuccessCallbackResult>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| count | `number` | `9` | 否 | 最多可以选择的图片张数<br>API 支持度: weapp, alipay, swan, tt, h5, rn |
| sizeType | `(keyof sizeType)[]` | `['original', 'compressed']` | 否 | 所选的图片的尺寸<br>API 支持度: weapp, alipay, swan, tt, rn |
| sourceType | `(keyof sourceType)[]` | `['album', 'camera']` | 否 | 选择图片的来源<br>API 支持度: weapp, alipay, swan, tt, h5, rn |
| complete | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |
| imageId | `string` |  | 否 | 用来上传的input元素ID（仅h5端<br>API 支持度: h5 |

<a id="sizetype"></a>

### sizeType

图片的尺寸

| 参数 | 说明 |
| --- | --- |
| original | 原图 |
| compressed | compressed |

<a id="sourcetype"></a>

### sourceType

图片的来源

| 参数 | 说明 |
| --- | --- |
| album | 从相册选图 |
| camera | 使用相机 |
| user | 使用前置摄像头(仅H5纯浏览器使用) |
| environment | 使用后置摄像头(仅H5纯浏览器) |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| tempFilePaths | `string[]` | 图片的本地临时文件路径列表 |
| tempFiles | `ImageFile[]` | 图片的本地临时文件列表 |
| errMsg | `string` | 调用结果 |

<a id="imagefile"></a>

### ImageFile

图片的本地临时文件列表

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| path | `string` | 是 | 本地临时文件路径 |
| size | `number` | 是 | 本地临时文件大小，单位 B |
| type | `string` | 否 | 文件的 MIME 类型<br>API 支持度: h5 |
| originalFileObj | `File` | 否 | 原始的浏览器 File 对象<br>API 支持度: h5 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.chooseImage({
  count: 1, // 默认9
  sizeType: ['original', 'compressed'], // 可以指定是原图还是压缩图，默认二者都有
  sourceType: ['album', 'camera'], // 可以指定来源是相册还是相机，默认二者都有，在H5浏览器端支持使用 `user` 和 `environment`分别指定为前后摄像头
  success: function (res) {
    // 返回选定照片的本地文件路径列表，tempFilePath可以作为img标签的src属性显示图片
    var tempFilePaths = res.tempFilePaths
  }
})
```
