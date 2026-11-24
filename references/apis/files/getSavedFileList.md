# Taro.getSavedFileList(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/files/getSavedFileList)

获取本地已保存的文件列表

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/file/wx.getSavedFileList.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => Promise<SuccessCallbackResult>
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
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| fileList | `FileItem[]` | 文件数组 |
| errMsg | `string` | 调用结果 |

<a id="fileitem"></a>

### FileItem

文件数组

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| createTime | `number` | 是 | 文件保存时的时间戳，从1970/01/01 08:00:00 到当前时间的秒数 |
| filePath | `string` | 是 | 本地路径 |
| apFilePath | `string` | 否 | 文件路径<br>API 支持度: alipay |
| size | `number` | 是 | 本地文件大小，以字节为单位 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getSavedFileList({
  success: function (res) {
    console.log(res.fileList)
  }
})
```
