# setGlobalDataPlugin

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/taro.extend/setGlobalDataPlugin)

Vue3 插件，用于设置 `getApp()` 中的全局变量

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native 快应用 Harmony Harmony hybrid

<a id="类型"></a>

## 类型

```tsx
Plugin
```

<a id="参数"></a>

## 参数

<a id="plugin"></a>

### Plugin

Vue3 插件，用于设置 `getApp()` 中的全局变量

<a id="install"></a>

#### install

```tsx
(app: any, data: any) => void
```

<a id="示例代码"></a>

## 示例代码

```js
// 使用插件
const App = createApp(...)
App.use(setGlobalDataPlugin, {
  xxx: 999
})
// 获取全局变量
Taro.getApp().xxx
```
