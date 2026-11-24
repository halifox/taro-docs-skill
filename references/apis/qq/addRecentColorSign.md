# Taro.addRecentColorSign(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/qq/addRecentColorSign)

添加当前小程序页面到最近浏览彩签，需要授权基础库 1.20.0 开始支持。
提示：在手 Q 8.9.0 前的版本，当系统未授予手 Q 悬浮穿权限时，每次调用该接口都会弹出系统授权窗口。自手 Q 8.9.0 起交互调整如下:

1. 系统没有授予手 Q 悬浮窗权限时，接口执行 fail 回调函数并附带 ”No floating window permission“的错误信息，开发者可针对此信息在业务代码里弹窗提示用户手动授予手 Q 悬浮窗权限。
2. 安卓系统部分机型存在获取悬浮窗权限不准确情况。

支持情况：微信小程序 QQ 小程序 H5 React Native Harmony

> [参考文档](https://q.qq.com/wiki/develop/miniprogram/API/open_port/port_addColorSign.html#qq-addrecentcolorsign)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| query | `string` | 否 | 做为点击最近彩签打开的小程序页面的启动参数，如 a=1&b=2<br>默认值：当前页面的查询参数 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.addRecentColorSign({
  query: 'a=1&b=2',
  success(res) {
    console.log('addRecentColorSign success: ', res)
  },
  fail(err) {
    console.log('addRecentColorSign fail: ', err)
  },
  complete(res) {
    console.log('addRecentColorSign complete: ', res)
  }
})
```
