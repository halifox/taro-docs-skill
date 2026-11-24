# RealtimeTagLogManager

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/base/debug/RealtimeTagLogManager)

给定标签的实时日志管理器实例，可以通过 给定标签的实时日志管理器实例，可以通过 [RealtimeLogManager.tag](RealtimeLogManager.md#tag) 接口获取，目前只支持在插件使用。 接口获取，目前只支持在插件使用。

**使用说明**
RealtimeTagLogManager 功能和 [RealtimeLogManager](RealtimeLogManager.md) 相似，但是为了让输出的实时日志更易于分析，其具有更严格的格式要求。
RealtimeTagLogManager 使用时需要传入标签，调用该实例所输出的日志均会被汇集到对应标签下，同时该实例的日志只支持 key-value 格式进行输出。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/RealtimeTagLogManager.html)

<a id="方法"></a>

## 方法

<a id="addfiltermsg"></a>

### addFilterMsg

添加过滤关键字

支持情况：微信小程序 H5 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/RealtimeTagLogManager.addFilterMsg.html)

```tsx
(msg: string) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| msg | `string` | 是 setFilterMsg 的添加接口。用于设置多个过滤关键字。 |

<a id="error"></a>

### error

写 error 日志

支持情况：微信小程序 H5 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/RealtimeTagLogManager.error.html)

```tsx
(key: string, value: string | number | Object | any[]) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| key | `string` | 日志的 key |
| value | string or number or Object or any[] | 日志的 key |

<a id="info"></a>

### info

写 info 日志

支持情况：微信小程序 H5 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/RealtimeTagLogManager.info.html)

```tsx
(key: string, value: string | number | Object | any[]) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| key | `string` | 日志的 key |
| value | string or number or Object or any[] | 日志的 key |

<a id="setfiltermsg"></a>

### setFilterMsg

设置过滤关键字

支持情况：微信小程序 H5 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/RealtimeTagLogManager.setFilterMsg.html)

```tsx
(msg: string) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| msg | `string` | 过滤关键字，最多不超过1Kb，可以在小程序管理后台根据设置的内容搜索得到对应的日志。 |

<a id="warn"></a>

### warn

写 warn 日志

支持情况：微信小程序 H5 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/RealtimeTagLogManager.warn.html)

```tsx
(key: string, value: string | number | Object | any[]) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| key | `string` | 日志的 key |
| value | string or number or Object or any[] | 日志的 key |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- |
| RealtimeTagLogManager | ✔️ |  |  |  |
| RealtimeTagLogManager.addFilterMsg | ✔️ |  |  |  |
| RealtimeTagLogManager.error | ✔️ |  |  |  |
| RealtimeTagLogManager.info | ✔️ |  |  |  |
| RealtimeTagLogManager.setFilterMsg | ✔️ |  |  |  |
| RealtimeTagLogManager.warn | ✔️ |  |  |  |
