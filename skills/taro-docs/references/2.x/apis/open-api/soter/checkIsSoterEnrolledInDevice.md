# Taro.checkIsSoterEnrolledInDevice(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/open-api/soter/checkIsSoterEnrolledInDevice)

获取设备内是否录入如指纹等生物信息的接口

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/soter/wx.checkIsSoterEnrolledInDevice.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<SuccessCallbackResult>
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| checkAuthMode | `"fingerPrint" \| "facial" \| "speech"` | 是 | 认证方式 |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="requestauthmodes"></a>

### requestAuthModes

| 参数 | 说明 |
| --- | --- |
| fingerPrint | 指纹识别 |
| facial | 人脸识别 |
| speech | 声纹识别<br>API 支持度: 暂未支持 |

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| requestAuthModes.speech |  |  |  |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errMsg | `string` | 错误信息 |
| isEnrolled | `boolean` | 是否已录入信息 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.checkIsSoterEnrolledInDevice({
  checkAuthMode: 'fingerPrint',
  success: function (res) {
    console.log(res.isEnrolled)
  }
})
```

<a id="api-支持度-1"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.checkIsSoterEnrolledInDevice | ✔️ |  |  |
