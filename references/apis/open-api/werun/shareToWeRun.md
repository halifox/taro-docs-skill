# Taro.shareToWeRun(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/open-api/werun/shareToWeRun)

分享数据到微信运动。

支持情况：微信小程序 H5 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/werun/wx.shareToWeRun.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => Promise<TaroGeneral.CallbackResult>
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
| recordList | `record[]` | 是 | 运动数据列表 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="record"></a>

### record

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| typeId | `number` | 运动项目id |
| time | `number` | 运动时长 |
| distance | `number` | 运动距离 |
| calorie | `number` | 消耗卡路里 |
