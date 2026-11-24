# Taro.createMediaQueryObserver()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/wxml/createMediaQueryObserver)

创建并返回一个 MediaQueryObserver 对象实例。在自定义组件或包含自定义组件的页面中，应使用 `this.createMediaQueryObserver()` 来代替。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/framework/view/resizable.html#Media%20Query)

<a id="类型"></a>

## 类型

```tsx
() => MediaQueryObserver
```

<a id="示例代码"></a>

## 示例代码

```tsx
let createMediaQueryObserver
if (process.env.TARO_ENV === 'weapp') {
   // 小程序没有组件实例，只能获取Page级组件实例
   createMediaQueryObserver = Taro.getCurrentInstance().page.createMediaQueryObserver
} else if (process.env.TARO_ENV === 'h5') {
   createMediaQueryObserver= Taro.createMediaQueryObserver
}
const mediaQueryObserver = createMediaQueryObserver()
```
