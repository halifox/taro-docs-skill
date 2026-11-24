# MediaQueryObserver

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/wxml/MediaQueryObserver)

`MediaQueryObserver` 对象，用于监听页面 media query 状态的变化，如界面的长宽是不是在某个指定的范围内。

<a id="方法"></a>

## 方法

<a id="observe"></a>

### observe

开始监听页面 media query 变化情况

```tsx
(descriptor: descriptor, callback: observeCallback) => void
```

| 参数 | 类型 |
| --- | --- |
| descriptor | `descriptor` |
| callback | `observeCallback` |

<a id="disconnect"></a>

### disconnect

停止监听。回调函数将不再触发

```tsx
() => void
```

<a id="参数"></a>

## 参数

<a id="descriptor"></a>

### descriptor

media query 描述符

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| minWidth | `number` | 页面最小宽度 (单位: px) |
| maxWidth | `number` | 页面最大宽度 (单位: px) |
| width | `number` | 页面宽度 (单位: px) |
| minHeight | `number` | 页面最小高度 (单位: px) |
| maxHeight | `number` | 页面最大高度（px 为单位） |
| height | `number` | 页面高度（px 为单位） |
| orientation | "landscape" or "portrait" | 屏幕方向 |

<a id="observecallback"></a>

### observeCallback

监听 media query 状态变化的回调函数

```tsx
(res: { matches: boolean; }) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `{ matches: boolean; }` |
