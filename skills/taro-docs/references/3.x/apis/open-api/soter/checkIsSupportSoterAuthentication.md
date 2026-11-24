# Taro.checkIsSupportSoterAuthentication(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/open-api/soter/checkIsSupportSoterAuthentication)

获取本机支持的 SOTER 生物认证方式

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/soter/wx.checkIsSupportSoterAuthentication.html)

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
| supportMode | `(keyof requestAuthModes)[]` | 该设备支持的可被SOTER识别的生物识别方式 |
| errMsg | `string` | 调用信息 |

<a id="requestauthmodes"></a>

### requestAuthModes

| 参数 | 说明 |
| --- | --- |
| fingerPrint | 指纹识别 |
| facial | 人脸识别 |
| speech | 声纹识别<br>API 支持度: 暂未支持 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.checkIsSupportSoterAuthentication({
  success: function (res) {
    // res.supportMode = [] 不具备任何被SOTER支持的生物识别方式
    // res.supportMode = ['fingerPrint'] 只支持指纹识别
    // res.supportMode = ['fingerPrint', 'facial'] 支持指纹识别和人脸识别
  }
})
```
