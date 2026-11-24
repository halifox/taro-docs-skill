# Taro.getStorageSync(key)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/storage/getStorageSync)

Taro.getStorage 的同步版本

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/storage/wx.getStorageSync.html)

<a id="类型"></a>

## 类型

```tsx
(key: string) => any
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| key | `string` | 本地缓存中指定的 key |

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
| Taro.getStorageSync | ✔️ | ✔️ |  |
