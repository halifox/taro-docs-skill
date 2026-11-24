# Taro.onCopyUrl(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/share/onCopyUrl)

监听用户点击右上角菜单的「复制链接」按钮时触发的事件

> 本接口为 Beta 版本，暂只在 Android 平台支持。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/share/wx.onCopyUrl.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 用户点击右上角菜单的「复制链接」按钮时触发的事件的回调函数 |

<a id="callback"></a>

### Callback

用户点击右上角菜单的「复制链接」按钮时触发的事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="callbackresult"></a>

### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| query | `string` | 用短链打开小程序时当前页面携带的查询字符串。小程序中使用时，应在进入页面时调用 `Taro.onCopyUrl` 自定义 `query`，退出页面时调用 `Taro.offCopyUrl`，防止影响其它页面。 |
