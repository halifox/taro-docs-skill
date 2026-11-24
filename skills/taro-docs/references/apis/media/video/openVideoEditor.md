# Taro.openVideoEditor(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/media/video/openVideoEditor)

打开视频编辑器

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/wx.openVideoEditor.html)

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

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| filePath | `string` | 是 | 视频源的路径，只支持本地路径 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| duration | `number` | 剪辑后生成的视频文件的时长，单位毫秒（ms） |
| size | `number` | 剪辑后生成的视频文件大小，单位字节数（byte） |
| tempFilePath | `string` | 编辑后生成的视频文件的临时路径 |
| tempThumbPath | `string` | 编辑后生成的缩略图文件的临时路径 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.openVideoEditor({
 filePath: ''
})
```
