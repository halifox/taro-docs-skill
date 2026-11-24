# Taro.reportPerformance(id, value, dimensions)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/base/performance/reportPerformance)

小程序测速上报。使用前，需要在小程序管理后台配置。 详情参见[小程序测速](https://developers.weixin.qq.com/miniprogram/dev/framework/performanceReport/index.html)指南。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/wx.reportPerformance.html)

<a id="类型"></a>

## 类型

```tsx
(id: number, value: number, dimensions?: string | string[]) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| id | `number` | 指标 id |
| value | `number` | 需要上报的数值 |
| dimensions | string or string[] | 自定义维度 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.reportPerformance(1101, 680)
Taro.reportPerformance(1101, 680, 'custom')
```
