# Taro.preload(options)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/base/preload)

跳转预加载 API

<a id="类型"></a>

## 类型

```tsx
{ (options: Record<string, any>): any; (key: string, value: any): any; }
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| options | `Record<string, any>` | 预加载的数据<br>param: options 预加载的数据 |

<a id="示例代码"></a>

## 示例代码

<a id="示例-1"></a>

### 示例 1

```tsx
Taro.preload({ key: 'value' })
```

<a id="示例-2"></a>

### 示例 2

```tsx
Taro.preload('key', 'value')
```
