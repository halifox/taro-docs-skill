# Taro.onKeyboardHeightChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/ui/keyboard/onKeyboardHeightChange)

监听键盘高度变化

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/keyboard/wx.onKeyboardHeightChange.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

<a id="callback"></a>

### Callback

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
| height | `number` | 键盘高度 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.onKeyboardHeightChange(res => {
  console.log(res.height)
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.onKeyboardHeightChange | ✔️ |  |  |
