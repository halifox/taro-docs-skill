# Taro.getStorage(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/storage/getStorage)

从本地缓存中异步获取指定 key 的内容

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/storage/wx.getStorage.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<SuccessCallbackResult>
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| key | `string` | 是 | 本地缓存中指定的 key |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | `any` | key对应的内容 |
| errMsg | `string` | 调用结果 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getStorage({
  key: 'key',
  success: function (res) {
    console.log(res.data)
  }
})
```

```tsx
try {
  var value = Taro.getStorageSync('key')
  if (value) {
    // Do something with return value
  }
} catch (e) {
  // Do something when catch error
}
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.getStorage | ✔️ | ✔️ | ✔️ |
