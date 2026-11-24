# Taro.addPhoneCalendar(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/calendar/addPhoneCalendar)

向系统日历添加事件

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/calendar/wx.addPhoneCalendar.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<TaroGeneral.CallbackResult>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| title | `string` |  | 是 | 日历事件标题 |
| startTime | `number` |  | 是 | 开始时间的 unix 时间戳 (1970年1月1日开始所经过的秒数) |
| allDay | `boolean` | `false` | 否 | 是否全天事件 |
| description | `string` |  | 否 | 事件说明 |
| location | `string` |  | 否 | 事件位置 |
| endTime | `string` |  | 否 | 结束时间的 unix 时间戳，默认与开始时间相同 |
| alarm | `boolean` | `true` | 否 | 是否提醒 |
| alarmOffset | `number` | `0` | 否 | 提醒提前量，单位秒，默认 0 表示开始时提醒 |
| complete | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |
