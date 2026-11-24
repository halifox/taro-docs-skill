# Taro.clearStorageSync()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/storage/clearStorageSync)

Taro.clearStorage 的同步版本

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/storage/wx.clearStorageSync.html)

<a id="类型"></a>

## 类型

```tsx
() => void
```

<a id="参数"></a>

## 参数

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.clearStorage()
```

```tsx
try {
  Taro.clearStorageSync()
} catch(e) {
// Do something when catch error
}
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.clearStorageSync | ✔️ | ✔️ |  |
