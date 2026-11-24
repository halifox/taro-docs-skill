# Taro.getStorageInfoSync()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/storage/getStorageInfoSync)

Taro.getStorageInfo 的同步版本

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/storage/wx.getStorageInfoSync.html)

<a id="类型"></a>

## 类型

```tsx
() => Option
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| currentSize | `number` | 是 | 当前占用的空间大小, 单位 KB |
| keys | `string[]` | 是 | 当前 storage 中所有的 key |
| limitSize | `number` | 是 | 限制的空间大小，单位 KB |
| success | `boolean` | 否 | 是否执行成功<br>API 支持度: alipay |

<a id="示例代码"></a>

## 示例代码

```tsx
try {
  const res = Taro.getStorageInfoSync()
  console.log(res.keys)
  console.log(res.currentSize)
  console.log(res.limitSize)
} catch (e) {
  // Do something when catch error
}
```
