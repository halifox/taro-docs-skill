# SelectorQuery

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/wxml/SelectorQuery)

查询节点信息的对象

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/wxml/SelectorQuery.html)

<a id="方法"></a>

## 方法

<a id="exec"></a>

### exec

执行所有的请求。请求结果按请求次序构成数组，在callback的第一个参数中返回。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/wxml/SelectorQuery.exec.html)

```tsx
(callback?: (...args: any[]) => any) => NodesRef
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `(...args: any[]) => any` | 回调函数 |

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| SelectorQuery.exec | ✔️ | ✔️ |  |

<a id="select"></a>

### select

在当前页面下选择第一个匹配选择器 `selector` 的节点。返回一个 `NodesRef` 对象实例，可以用于获取节点信息。

**selector 语法**

selector类似于 CSS 的选择器，但仅支持下列语法。

- ID选择器：#the-id
- class选择器（可以连续指定多个）：.a-class.another-class
- 子元素选择器：.the-parent > .the-child
- 后代选择器：.the-ancestor .the-descendant
- 跨自定义组件的后代选择器：.the-ancestor >>> .the-descendant
- 多选择器的并集：#a-node, .some-other-nodes

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/wxml/SelectorQuery.select.html)

```tsx
(selector: string) => NodesRef
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| selector | `string` | 选择器 |

<a id="示例代码"></a>

#### 示例代码

```tsx
Taro.createSelectorQuery().select('#the-id').fields({
  dataset: true,
  size: true,
  scrollOffset: true,
  properties: ['scrollX', 'scrollY']
}, function (res){
  res.dataset    // 节点的dataset
  res.width      // 节点的宽度
  res.height     // 节点的高度
  res.scrollLeft // 节点的水平滚动位置
  res.scrollTop  // 节点的竖直滚动位置
  res.scrollX    // 节点 scroll-x 属性的当前值
  res.scrollY    // 节点 scroll-x 属性的当前值
}).exec()
```

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| SelectorQuery.select | ✔️ | ✔️ |  |

<a id="selectall"></a>

### selectAll

在当前页面下选择匹配选择器 selector 的所有节点。

**selector 语法**

selector类似于 CSS 的选择器，但仅支持下列语法。

- ID选择器：#the-id
- class选择器（可以连续指定多个）：.a-class.another-class
- 子元素选择器：.the-parent > .the-child
- 后代选择器：.the-ancestor .the-descendant
- 跨自定义组件的后代选择器：.the-ancestor >>> .the-descendant
- 多选择器的并集：#a-node, .some-other-nodes

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/wxml/SelectorQuery.selectAll.html)

```tsx
(selector: string) => NodesRef
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| selector | `string` | 选择器 |

<a id="api-支持度-2"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| SelectorQuery.selectAll | ✔️ | ✔️ |  |

<a id="selectviewport"></a>

### selectViewport

选择显示区域。可用于获取显示区域的尺寸、滚动位置等信息。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/wxml/SelectorQuery.selectViewport.html)

```tsx
() => NodesRef
```

<a id="示例代码-1"></a>

#### 示例代码

```tsx
Taro.createSelectorQuery().selectViewport().scrollOffset(function (res) {
  res.id      // 节点的ID
  res.dataset // 节点的dataset
  res.scrollLeft // 节点的水平滚动位置
  res.scrollTop  // 节点的竖直滚动位置
}).exec()
```

<a id="api-支持度-3"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| SelectorQuery.selectViewport | ✔️ | ✔️ |  |

<a id="in"></a>

### in

将选择器的选取范围更改为自定义组件 `component` 内。（初始时，选择器仅选取页面范围的节点，不会选取任何自定义组件中的节点）。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/wxml/SelectorQuery.in.html)

```tsx
(component: Record<string, any>) => SelectorQuery
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| component | `Record<string, any>` | 自定义组件实例 |

<a id="示例代码-2"></a>

#### 示例代码

```tsx
Component({
  queryMultipleNodes () {
    const query = Taro.createSelectorQuery().in(this)
    query.select('#the-id').boundingClientRect(function(res){
      res.top // 这个组件内 #the-id 节点的上边界坐标
    }).exec()
  }
})
```

<a id="api-支持度-4"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| SelectorQuery.in | ✔️ | ✔️ |  |

<a id="api-支持度-5"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| SelectorQuery.exec | ✔️ | ✔️ |  |
| SelectorQuery.select | ✔️ | ✔️ |  |
| SelectorQuery.selectAll | ✔️ | ✔️ |  |
| SelectorQuery.selectViewport | ✔️ | ✔️ |  |
| SelectorQuery.in | ✔️ | ✔️ |  |
