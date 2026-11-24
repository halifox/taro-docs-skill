# console

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/base/debug/console)

向调试面板中打印日志。console 是一个全局对象，可以直接访问。在微信客户端中，向 vConsole 中输出日志。

**注意**

- 由于 vConsole 功能有限，以及不同客户端对 console 方法的支持情况有差异，建议开发者在小程序中只使用本文档中提供的方法。
- 部分内容展示的限制请参见调试

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/console.html)

<a id="方法"></a>

## 方法

<a id="debug"></a>

### debug

向调试面板中打印 debug 日志

支持情况：微信小程序 H5 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/console.debug.html)

```tsx
(...args: any[]) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| args | `any[]` | 日志内容，可以有任意多个。 |

<a id="error"></a>

### error

向调试面板中打印 error 日志

支持情况：微信小程序 H5 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/console.error.html)

```tsx
(...args: any[]) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| args | `any[]` | 日志内容，可以有任意多个。 |

<a id="group"></a>

### group

在调试面板中创建一个新的分组

**注意**
仅在工具中有效，在 vConsole 中为空函数实现。

支持情况：微信小程序 H5 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/console.group.html)

```tsx
(label?: string) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| label | `string` | 分组标记 |

<a id="groupend"></a>

### groupEnd

结束由 [console.group](#group) 创建的分组

**注意**
仅在工具中有效，在 vConsole 中为空函数实现。

支持情况：微信小程序 H5 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/console.groupEnd.html)

```tsx
() => void
```

<a id="info"></a>

### info

向调试面板中打印 info 日志

支持情况：微信小程序 H5 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/console.info.html)

```tsx
(...args: any[]) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| args | `any[]` | 日志内容，可以有任意多个。 |

<a id="log"></a>

### log

向调试面板中打印 log 日志

支持情况：微信小程序 抖音小程序 H5 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/console.log.html)

```tsx
(...args: any[]) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| args | `any[]` | 日志内容，可以有任意多个。 |

<a id="warn"></a>

### warn

向调试面板中打印 warn 日志

支持情况：微信小程序 H5 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/console.warn.html)

```tsx
(...args: any[]) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| args | `any[]` | 日志内容，可以有任意多个。 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | 抖音小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| console | ✔️ |  |  |  |  | ✔️ | ✔️ |
| console.debug | ✔️ |  |  |  |  | ✔️ | ✔️ |
| console.error | ✔️ |  |  |  |  | ✔️ | ✔️ |
| console.group | ✔️ |  |  |  |  | ✔️ | ✔️ |
| console.groupEnd | ✔️ |  |  |  |  | ✔️ | ✔️ |
| console.info | ✔️ |  |  |  |  | ✔️ | ✔️ |
| console.log | ✔️ | ✔️ |  |  |  | ✔️ | ✔️ |
| console.warn | ✔️ |  |  |  |  | ✔️ | ✔️ |
