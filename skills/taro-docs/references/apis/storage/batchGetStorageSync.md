# Taro.batchGetStorageSync(keyList)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/storage/batchGetStorageSync)

从本地缓存中同步批量获取指定 key 的内容。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/storage/wx.batchGetStorageSync.html)

<a id="类型"></a>

## 类型

```tsx
<T = any>(keyList: string[]) => T[]
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| keyList | `T` | 本地缓存中指定的 key 数组 |

<a id="示例代码"></a>

## 示例代码

```tsx
try {
  var valueList = Taro.batchGetStorageSync(['key'])
  if (valueList) {
    // Do something with return value
  }
} catch (e) {
  // Do something when catch error
}
```
