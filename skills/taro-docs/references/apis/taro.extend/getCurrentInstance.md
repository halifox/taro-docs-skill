# Taro.getCurrentInstance()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/taro.extend/getCurrentInstance)

获取当前页面实例

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native 快应用 Harmony Harmony hybrid

<a id="类型"></a>

## 类型

```tsx
() => Current
```

<a id="参数"></a>

## 参数

<a id="current"></a>

### Current

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| app | `any` | 是 |  |
| router | `any` | 是 |  |
| page | `any` | 是 |  |
| onReady | `string` | 是 |  |
| onHide | `string` | 是 |  |
| onShow | `string` | 是 |  |
| preloadData | `Record<any, any>` | 否 |  |
| rnNavigationRef | `React.RefObject<any>` | 否 | RN 私有对象navigationRef，用于使用底层接口控制路由 |
