# Taro.getExtConfigSync()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/ext/getExtConfigSync)

Taro.getExtConfig 的同步版本。

**Tips**

1. 本接口暂时无法通过 Taro.canIUse 判断是否兼容，开发者需要自行判断 Taro.getExtConfigSync 是否存在来兼容

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ext/wx.getExtConfigSync.html)

<a id="类型"></a>

## 类型

```tsx
() => TaroGeneral.IAnyObject
```

<a id="参数"></a>

## 参数

<a id="extinfo"></a>

### ExtInfo

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| extConfig | `TaroGeneral.IAnyObject` | 第三方平台自定义的数据 |

<a id="示例代码"></a>

## 示例代码

```tsx
let extConfig = Taro.getExtConfigSync? Taro.getExtConfigSync(): {}

console.log(extConfig)
```
