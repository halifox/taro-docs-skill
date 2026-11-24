# requirePlugin

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/taro.extend/requirePlugin)

小程序引用插件 JS 接口

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native 快应用 Harmony

<a id="类型"></a>

## 类型

```tsx
{ (pluginName: string): any; (pluginName: string, success?: (mod: any) => any, error?: (e: { mod: any; errMsg: string; }) => any): any; async?: (pluginName: string) => Promise<any>; }
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| pluginName | `string` |
