# Taro.useSaveExitState(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/taro.hooks/useSaveExitState)

页面销毁前保留状态回调

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

<a id="类型"></a>

## 类型

```tsx
(callback: () => { data: Record<any, any>; expireTimeStamp?: number; }) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| callback | `() => { data: Record<any, any>; expireTimeStamp?: number; }` |
