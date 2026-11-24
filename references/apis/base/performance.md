# Performance

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/base/performance/)

Performance 对象，用于获取性能数据及创建性能监听器

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/Performance.html)

<a id="方法"></a>

## 方法

<a id="createobserver"></a>

### createObserver

创建全局性能事件监听器

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/Performance.createObserver.html)

```tsx
(callback: TaroGeneral.TFunc) => PerformanceObserver
```

| 参数 | 类型 |
| --- | --- |
| callback | `TaroGeneral.TFunc` |

<a id="getentries"></a>

### getEntries

该方法返回当前缓冲区中的所有性能数据

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/Performance.getEntries.html)

```tsx
() => PerformanceEntry[]
```

<a id="getentriesbyname"></a>

### getEntriesByName

获取当前缓冲区中所有名称为 [name] 且类型为 [entryType] 的性能数据

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/Performance.getEntriesByName.html)

```tsx
(name: string, entryType: string) => PerformanceEntry[]
```

| 参数 | 类型 |
| --- | --- |
| name | `string` |
| entryType | `string` |

<a id="getentriesbytype"></a>

### getEntriesByType

获取当前缓冲区中所有类型为 [entryType] 的性能数据

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/Performance.getEntriesByType.html)

```tsx
(entryType: string) => PerformanceEntry[]
```

| 参数 | 类型 |
| --- | --- |
| entryType | `string` |

<a id="setbuffersize"></a>

### setBufferSize

设置缓冲区大小，默认缓冲 30 条性能数据

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/Performance.setBufferSize.html)

```tsx
(size: number) => void
```

| 参数 | 类型 |
| --- | --- |
| size | `number` |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | 抖音小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| Performance | ✔️ | ✔️ |  |  |  |  |
| Performance.createObserver | ✔️ |  |  |  |  |  |
| Performance.getEntries | ✔️ | ✔️ |  |  |  |  |
| Performance.getEntriesByName | ✔️ | ✔️ |  |  |  |  |
| Performance.getEntriesByType | ✔️ | ✔️ |  |  |  |  |
| Performance.setBufferSize | ✔️ |  |  |  |  |  |
