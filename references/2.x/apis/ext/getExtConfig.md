# Taro.getExtConfig(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/ext/getExtConfig)

获取[第三方平台](https://developers.weixin.qq.com/miniprogram/dev/devtools/ext.html)自定义的数据字段。

**Tips**

1. 本接口暂时无法通过 Taro.canIUse 判断是否兼容，开发者需要自行判断 Taro.getExtConfig 是否存在来兼容

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ext/wx.getExtConfig.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => Promise<SuccessCallbackResult>
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| extConfig | `Record<string, any>` | 第三方平台自定义的数据 |
| errMsg | `string` | 调用结果 |

<a id="示例代码"></a>

## 示例代码

```tsx
if(Taro.getExtConfig) {
  Taro.getExtConfig({
    success: function (res) {
      console.log(res.extConfig)
    }
  })
}
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.getExtConfig | ✔️ |  |  |
