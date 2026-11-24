# Taro.usePageNotFound(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/taro.hooks/usePageNotFound)

小程序要打开的页面不存在时触发的回调。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> H5: 多页面模式不支持该方法

<a id="类型"></a>

## 类型

```tsx
(callback: (res: { [key: string]: any; path: string; query: Record<any, any>; isEntryPage: boolean; }) => void) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| callback | `(res: { [key: string]: any; path: string; query: Record<any, any>; isEntryPage: boolean; }) => void` |
