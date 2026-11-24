# Taro.onScreenRecordingStateChanged(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/device/screen/onScreenRecordingStateChanged)

监听用户录屏事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/screen/wx.onScreenRecordingStateChanged.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 用户录屏事件的监听函数 |

<a id="screenrecordingstate"></a>

### ScreenRecordingState

| 参数 | 说明 |
| --- | --- |
| start | 开始录屏 |
| stop | 结束录屏 |

<a id="callback"></a>

### Callback

用户录屏事件的监听函数

```tsx
(state: keyof ScreenRecordingState) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| state | `keyof ScreenRecordingState` | 录屏状态 |

<a id="示例代码"></a>

## 示例代码

```tsx
// 监听用户录屏事件
const handler = function (res) {
    console.log(res.state)
}
Taro.onScreenRecordingStateChanged(handler)
```
