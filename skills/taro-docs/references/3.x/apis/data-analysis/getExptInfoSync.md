# Taro.getExptInfoSync(keys)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/data-analysis/getExptInfoSync)

给定实验参数数组，获取对应的实验参数值

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/data-analysis/wx.getExptInfoSync.html)

<a id="类型"></a>

## 类型

```tsx
(keys?: string[]) => TaroGeneral.IAnyObject
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| keys | `string[]` | 实验参数数组，不填则获取所有实验参数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getExptInfoSync(['color'])
```
