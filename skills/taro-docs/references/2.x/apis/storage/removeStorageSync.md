# Taro.removeStorageSync(key)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/storage/removeStorageSync)

从本地缓存中同步移除指定 key 。
Taro.removeStorage 的同步版本

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/storage/wx.removeStorageSync.html)

<a id="类型"></a>

## 类型

```tsx
{ (key: string): void; (key: string): void; }
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| key | `string` | 本地缓存中指定的 key |

<a id="示例代码"></a>

## 示例代码

<a id="示例-1"></a>

### 示例 1

```tsx
try {
  Taro.removeStorageSync('key')
} catch (e) {
  // Do something when catch error
}
```

<a id="示例-2"></a>

### 示例 2

```tsx
Taro.removeStorage({
  key: 'key',
  success: function (res) {
    console.log(res)
  }
})
```

```tsx
try {
  Taro.removeStorageSync('key')
} catch (e) {
  // Do something when catch error
}
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.removeStorageSync | ✔️ | ✔️ |  |
