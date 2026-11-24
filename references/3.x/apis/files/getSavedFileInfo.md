# Taro.getSavedFileInfo(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/files/getSavedFileInfo)

获取本地文件的文件信息。此接口只能用于获取已保存到本地的文件，若需要获取临时文件信息，请使用 [Taro.getFileInfo](../../../apis/files/getFileInfo.md) 接口。

支持情况：微信小程序 百度小程序 支付宝小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/file/wx.getSavedFileInfo.html)

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
| filePath | `string` | 是 | 文件路径 |
| apFilePath | `string` | 否 | 文件路径<br>API 支持度: alipay |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| createTime | `number` | 文件保存时的时间戳，从1970/01/01 08:00:00 到该时刻的秒数 |
| size | `number` | 文件大小，单位 B |
| errMsg | `string` | 调用结果 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getSavedFileInfo({
  filePath: 'wxfile://somefile', //仅做示例用，非真正的文件路径
  success: function (res) {
    console.log(res.size)
    console.log(res.createTime)
  }
})
```
