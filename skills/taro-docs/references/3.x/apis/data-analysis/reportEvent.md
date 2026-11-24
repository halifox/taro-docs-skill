# Taro.reportEvent(eventId, data)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/data-analysis/reportEvent)

事件上报

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/data-analysis/wx.reportEvent.html)

<a id="类型"></a>

## 类型

```tsx
(eventId: string, data: TaroGeneral.IAnyObject) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| eventId | `string` | 事件名 |
| data | `TaroGeneral.IAnyObject` | 上报的自定义数据，key 为配置中的字段名，value 为上报的数据。 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.reportEvent('purchase', {
  price: 120,
  color: 'red'
})
```
