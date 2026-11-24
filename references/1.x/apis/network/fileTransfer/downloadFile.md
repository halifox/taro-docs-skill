# Taro.downloadFile(param)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/network/fileTransfer/downloadFile)

下载文件资源到本地。客户端直接发起一个 HTTPS GET 请求，返回文件的本地临时路径。使用前请注意阅读相关说明。

注意：请在服务端响应的 header 中指定合理的 Content-Type 字段，以保证客户端正确处理文件类型。

使用方式同 [`wx.downloadFile`](https://developers.weixin.qq.com/miniprogram/dev/api/wx.downloadFile.html)，支持 `Promise` 化使用。

<a id="参数"></a>

## 参数

<a id="object-param"></a>

### object param

| Property | Type | Description |
| --- | --- | --- |
| url | `string` | 下载资源的 url |
| [header] | `object` | HTTP 请求的 Header，Header 中不能设置 Referer |
| [filePath] | `string` | 指定文件下载后存储的路径(h5端该参数无效) |
| [success()] | `function` | 接口调用成功的回调函数 |
| [fail()] | `function` | 接口调用失败的回调函数 |
| [complete()] | `function` | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="返回值"></a>

## 返回值

<a id="promiseobject-res-promise"></a>

### Promise<object res> promise

| Name | Type | Description |
| --- | --- | --- |
| promise.headersReceive(callback) | `function` | 绑定接收到http header的回调 |
| promise.progress(callback) | `function` | 绑定请求进度更新的回调 |
| promise.abort() | `function` | 中断请求 |
| res.statusCode | `number` | 请求的返回状态码 |
| res.tempFilePath | `string` | 下载文件的临时路径 |

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.downloadFile(params).then(...)
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native | 支付宝小程序 | 百度小程序 |
| --- | --- | --- | --- | --- | --- |
| Taro.downloadFile | ✔️ | ✔️ | ️ | ✔️ | ✔️ |
