# Taro.startFacialRecognitionVerifyAndUploadVideo(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/open-api/facial/startFacialRecognitionVerifyAndUploadVideo)

开始人脸识别认证并上传认证视频

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => Promise<CallbackResult>
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
| name | `string` | 是 | 身份证名称 |
| idCardNumber | `string` | 是 | 身份证名称 |
| checkAliveType | `number` | 否 | 交互方式 |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="callbackresult"></a>

### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errMsg | `string` | 错误信息 |
| errCode | `number` | 错误码 |
| verifyResult | `string` | 认证结果 |
