# Taro.onBackgroundFetchData(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/storage/background-fetch/onBackgroundFetchData)

收到 backgroundFetch 数据时的回调

支持情况：微信小程序 QQ 小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/storage/background-fetch/wx.onBackgroundFetchData.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option | Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | Option or Callback |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

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
| fetchType | `string` | 缓存数据类别，取值为 periodic 或 pre |
| fetchedData | `string` | 缓存数据 |
| timeStamp | `number` | 客户端拿到缓存数据的时间戳 |
| path | `string` | 小程序页面路径 |
| query | `string` | 传给页面的 query 参数 |
| scene | `number` | 进入小程序的场景值 |
