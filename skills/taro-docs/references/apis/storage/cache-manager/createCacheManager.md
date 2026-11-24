# Taro.createCacheManager(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/storage/cache-manager/createCacheManager)

创建缓存管理器

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/storage/cachemanager/wx.createCacheManager.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => CacheManager
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="mode"></a>

### Mode

| 参数 | 说明 |
| --- | --- |
| weakNetwork | 弱网/离线使用缓存返回 |
| always | 总是使用缓存返回 |
| none | 不开启，后续可手动开启/停止使用缓存返回 |

<a id="extra"></a>

### Extra

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| apiList | `string[]` | 否 | 需要缓存的 wx api 接口，不传则表示支持缓存的接口全都做缓存处理。返回的如果是缓存数据，开发者可通过 fromCache 标记区分 |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| origin | `string` | 否 | 全局 origin |
| mode | `keyof Mode` | 否 | 缓存模式 |
| maxAge | `number` | 否 | 全局缓存有效时间，单位为毫秒，默认为 7 天，最长不超过 30 天 |
| extra | `Extra` | 否 | 额外的缓存处理 |
