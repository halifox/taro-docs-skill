# Taro.reportAnalytics(eventName, data)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/open-api/data-analysis/reportAnalytics)

自定义分析数据上报接口。使用前，需要在小程序管理后台自定义分析中新建事件，配置好事件名与字段。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/data-analysis/wx.reportAnalytics.html)

<a id="类型"></a>

## 类型

```tsx
(eventName: string, data: Record<string, any>) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| eventName | `string` | 事件名 |
| data | `Record<string, any>` | 上报的自定义数据，key 为配置中的字段名，value 为上报的数据。 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.reportAnalytics('purchase', {
  price: 120,
  color: 'red'
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.reportAnalytics | ✔️ |  |  |
