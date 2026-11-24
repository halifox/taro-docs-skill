# Taro.openDocument(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/files/openDocument)

新开页面打开文档，支持格式

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/file/wx.openDocument.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<TaroGeneral.CallbackResult>
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
| filePath | `string` | 是 | 文件路径，可通过 downloadFile 获得 |
| showMenu | `boolean` | 否 | 是否显示右上角菜单 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| fileType | `keyof FileType` | 否 | 文件类型，指定文件类型打开文件 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="filetype"></a>

### FileType

文件类型

| 参数 | 说明 |
| --- | --- |
| doc | doc 格式 |
| docx | docx 格式 |
| xls | xls 格式 |
| xlsx | xlsx 格式 |
| ppt | ppt 格式 |
| pptx | pptx 格式 |
| pdf | pdf 格式 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.downloadFile({
  url: 'https://example.com/somefile.pdf',
  success: function (res) {
    var filePath = res.tempFilePath
    Taro.openDocument({
      filePath: filePath,
      success: function (res) {
        console.log('打开文档成功')
      }
    })
  }
})
```
