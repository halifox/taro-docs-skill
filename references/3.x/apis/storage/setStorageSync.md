# Taro.setStorageSync(key, data)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/storage/setStorageSync)

Taro.setStorage 的同步版本

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/storage/wx.setStorageSync.html)

<a id="类型"></a>

## 类型

```tsx
(key: string, data: any) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| key | `string` | 本地缓存中指定的 key |
| data | `any` | 需要存储的内容。只支持原生类型、Date、及能够通过`JSON.stringify`序列化的对象。 |

<a id="示例代码"></a>

## 示例代码

<a id="示例-1"></a>

### 示例 1

```tsx
Taro.setStorage({
  key:"key",
  data:"value"
})
```

<a id="示例-2"></a>

### 示例 2

```tsx
try {
  Taro.setStorageSync('key', 'value')
} catch (e) { }
```
