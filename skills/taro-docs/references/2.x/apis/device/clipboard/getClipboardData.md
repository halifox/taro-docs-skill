# Taro.getClipboardData(res)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/device/clipboard/getClipboardData)

获取系统剪贴板内容

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/clipboard/wx.getClipboardData.html)

<a id="类型"></a>

## 类型

```tsx
(res?: Option) => Promise<Promised>
```

<a id="参数"></a>

## 参数

<a id="promised"></a>

### Promised

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errMsg | `string` | 调用信息 |
| data | `string` | 剪贴板的内容 |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: SuccessCallbackOption) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackoption"></a>

### SuccessCallbackOption

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | `string` | 剪贴板的内容 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getClipboardData({
  success: function (res){
    console.log(res.data)
  }
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.getClipboardData | ✔️ | ✔️(部分实现) | ✔️ |
