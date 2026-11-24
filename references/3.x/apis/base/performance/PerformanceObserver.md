# PerformanceObserver

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/base/performance/PerformanceObserver)

PerformanceObserver 对象，用于监听性能相关事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/PerformanceObserver.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| supportedEntryTypes | `PerformanceEntry[]` | 获取当前支持的所有性能指标类型 |

<a id="disconnect"></a>

### disconnect

停止监听

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/PerformanceObserver.disconnect.html)

```tsx
() => void
```

<a id="observe"></a>

### observe

开始监听

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/PerformanceObserver.observe.html)

```tsx
(option: Option) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="参数"></a>

## 参数

<a id="observe-1"></a>

### observe

<a id="option"></a>

#### Option

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| type | `keyof EntryType` | 指标类型。不能和 entryTypes 同时使用 |
| entryTypes | `(keyof EntryType)[]` | 指标类型列表。不能和 type 同时使用。 |

<a id="entrytype"></a>

#### EntryType

| 参数 | 说明 |
| --- | --- |
| navigation | 路由 |
| render | 渲染 |
| script | 脚本 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| PerformanceObserver | ✔️ |  |  |  |  |
| PerformanceObserver.disconnect | ✔️ |  |  |  |  |
| PerformanceObserver.observe | ✔️ |  |  |  |  |
