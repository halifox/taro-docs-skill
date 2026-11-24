# Taro.onThemeChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/base/weapp/app-event/onThemeChange)

监听系统主题改变事件。该事件与 [`App.onThemeChange`](https://developers.weixin.qq.com/miniprogram/dev/reference/api/App.html#onThemeChange-Object-object) 的回调时机一致。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/app/app-event/wx.onThemeChange.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| callback | `Callback` |

<a id="callback"></a>

### Callback

系统主题改变事件的回调函数

```tsx
(res: Result) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `Result` |

<a id="result"></a>

### Result

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| theme | `keyof ITheme` | 系统当前的主题，取值为`light`或`dark` |

<a id="itheme"></a>

### ITheme

| 参数 | 说明 |
| --- | --- |
| light | 浅色主题 |
| dark | 深色主题 |
