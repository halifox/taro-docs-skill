# Taro.batchSetStorage(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/storage/batchSetStorage)

将数据批量存储在本地缓存中指定的 key 中。会覆盖掉原来该 key 对应的内容。
除非用户主动删除或因存储空间原因被系统清理，否则数据都一直可用。
单个 key 允许存储的最大数据长度为 1MB，所有数据存储上限为 10MB。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/storage/wx.batchGetStorage.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<TaroGeneral.CallbackResult>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| kvList | `kv[]` | 是 | [{ key, value }] |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="kv"></a>

### kv

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| key | `string` | key 本地缓存中指定的 key |
| value | `any` | data 需要存储的内容。只支持原生类型、Date、及能够通过JSON.stringify序列化的对象。 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.batchGetStorage({
  keyList: ['key']
  success(res) {
    console.log(res)
  }
})
```
