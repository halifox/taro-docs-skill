# EntryList

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/base/performance/EntryList)

EntryList 对象

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/EntryList.html)

<a id="方法"></a>

## 方法

<a id="getentries"></a>

### getEntries

该方法返回当前列表中的所有性能数据

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/EntryList.getEntries.html)

```tsx
() => PerformanceEntry[]
```

<a id="getentriesbyname"></a>

### getEntriesByName

获取当前列表中所有名称为 [name] 且类型为 [entryType] 的性能数据

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/EntryList.getEntriesByName.html)

```tsx
(name: string, entryType: string) => PerformanceEntry[]
```

| 参数 | 类型 |
| --- | --- |
| name | `string` |
| entryType | `string` |

<a id="getentriesbytype"></a>

### getEntriesByType

获取当前列表中所有类型为 [entryType] 的性能数据

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/EntryList.getEntriesByType.html)

```tsx
(entryType: string) => PerformanceEntry[]
```

| 参数 | 类型 |
| --- | --- |
| entryType | `string` |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| EntryList | ✔️ |  |  |  |  |
| EntryList.getEntries | ✔️ |  |  |  |  |
| EntryList.getEntriesByName | ✔️ |  |  |  |  |
| EntryList.getEntriesByType | ✔️ |  |  |  |  |
