# Taro.getApp(opts)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/framework/getApp)

获取到小程序全局唯一的 App 实例。

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native 快应用 Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/reference/api/getApp.html)

<a id="类型"></a>

## 类型

```tsx
<T = TaroGeneral.IAnyObject>(opts?: Option) => Instance<T>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| opts | `T` |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| allowDefault | `boolean` | 否 | 在 `App` 未定义时返回默认实现。当App被调用时，默认实现中定义的属性会被覆盖合并到App中。一般用于独立分包 |

<a id="instance"></a>

### Instance

```tsx
Option | T
```
