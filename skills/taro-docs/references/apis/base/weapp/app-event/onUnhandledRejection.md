# Taro.onUnhandledRejection(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/base/weapp/app-event/onUnhandledRejection)

监听未处理的 Promise 拒绝事件。该事件与 [`App.onUnhandledRejection`](https://developers.weixin.qq.com/miniprogram/dev/reference/api/App.html#onUnhandledRejection-Object-object) 的回调时机与参数一致。

**注意**

- 所有的 unhandledRejection 都可以被这一监听捕获，但只有 Error 类型的才会在小程序后台触发报警。

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/app/app-event/wx.onUnhandledRejection.html)

<a id="类型"></a>

## 类型

```tsx
<T = any>(callback: Callback<T>) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| callback | `T` |

<a id="callback"></a>

### Callback

```tsx
(res: Result<T>) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `Result<T>` |

<a id="result"></a>

### Result

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| reason | string or Error | 拒绝原因，一般是一个 Error 对象 |
| promise | `Promise<T>` | 被拒绝的 Promise 对象 |
