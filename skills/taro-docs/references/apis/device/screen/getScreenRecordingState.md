# Taro.getScreenRecordingState(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/screen/getScreenRecordingState)

查询用户是否在录屏

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/screen/wx.getScreenRecordingState.html)

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
| success | `(option: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="screenrecordingstate"></a>

### ScreenRecordingState

| 参数 | 说明 |
| --- | --- |
| on | 开启 |
| off | 关闭 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| state | `keyof ScreenRecordingState` | 录屏状态 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getScreenRecordingState({
    success: function (res) {
        console.log(res.state)
    },
})
```
