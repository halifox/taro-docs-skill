# Taro.batchSetStorageSync(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/storage/batchSetStorageSync)

将数据批量存储在本地缓存中指定的 key 中。
会覆盖掉原来该 key 对应的内容。除非用户主动删除或因存储空间原因被系统清理，否则数据都一直可用。
单个 key 允许存储的最大数据长度为 1MB，所有数据存储上限为 10MB。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/storage/wx.batchGetStorageSync.html)

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

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| kvList | `kv[]` | [{ key, value }] |

<a id="kv"></a>

### kv

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| key | `string` | key 本地缓存中指定的 key |
| value | `any` | data 需要存储的内容。只支持原生类型、Date、及能够通过JSON.stringify序列化的对象。 |

<a id="示例代码"></a>

## 示例代码

```tsx
try {
  Taro.batchSetStorageSync([{key: 'key', value: 'value'}])
} catch (e) { }
```
