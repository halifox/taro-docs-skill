# Reconciler

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/platform-plugin/reconciler)

Taro 的运行时包括 DOM、BOM、React 兼容层、Vue 兼容层等内容，而不同的端平台或开发框架都有可能需要对 Taro 运行时进行侵入定制。

为了解耦，我们参考了 **React Reconciler** 的概念，外部可以通过提供一个自定义的 `hostConfig` 配置对象，对运行时进行定制。

> 遇到 hostConfig 的配置项不满足需求，需要进行扩展时，可以给 Taro 提交 PR ～

<a id="hostconfig-配置"></a>

## hostConfig 配置

<a id="appendchild-parent-child"></a>

### appendChild (parent, child)

`DOMNode` 调用 `appendChild` 方法时触发。

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| parent | DOMNode | 父节点 |
| child | DOMNode / TextElement | 要给父节点追加的节点 |

<a id="removechild-parent-child-oldchild"></a>

### removeChild (parent, child, oldChild)

`DOMNode` 调用 `replaceChild` 方法时触发。

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| parent | DOMNode | 父节点 |
| child | DOMNode / TextElement | 用来替换 oldChild 的新节点 |
| oldChild | DOMNode / TextElement | 被替换掉的原始节点 |

<a id="insertbefore-parent-child-refchild"></a>

### insertBefore (parent, child, refChild)

`DOMNode` 调用 `insertBefore` 方法时触发。

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| parent | DOMNode | 父节点 |
| child | DOMNode / TextElement | 用于插入的节点 |
| refChild | DOMNode / TextElement | 将要插在这个节点之前 |

<a id="removeattribute-element-qualifiedname"></a>

### removeAttribute (element, qualifiedName)

`DOMElement` 调用 `removeAttribute` 方法时触发。

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| element | DOMElement | 当前操作元素 |
| qualifiedName | string | 指定要从元素中移除的属性的名称 |

<a id="setattribute-element-qualifiedname-value"></a>

### setAttribute (element, qualifiedName, value)

`DOMElement` 调用 `setAttribute` 方法时触发。

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| element | DOMElement | 当前操作元素 |
| qualifiedName | string | 表示属性名称的字符串 |
| value |  | 属性的值/新值 |

<a id="prepareupdatedata-data-page"></a>

### prepareUpdateData (data, page)

每次 Taro DOM 树更新，调用小程序 `setData` 前触发。

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | DataTree | 将要 setData 的 Taro DOM 树数据结构 |
| page | TaroRootElement | 页面根元素 |

<a id="appendinitialpage-data-page"></a>

### appendInitialPage (data, page)

Taro DOM 树初始化，第一次调用小程序 `setData` 前触发。在调用 `prepareUpdateData` 后立刻执行。

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | DataTree | 将要 setData 的 Taro DOM 树数据结构 |
| page | TaroRootElement | 页面根元素 |

<a id="getlifecyle-instance-lifecyle"></a>

### getLifecyle (instance, lifecyle)

小程序页面的生命周期被触发时调用。

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| instance | Instance | 用户编写的页面实例 |
| lifecyle | string | 小程序页面被触发的生命周期函数名称 |

需要返回 **function** 或 **function[]**，表示将要执行的函数。

例子：

```js
// 默认值：
// 直接取用户编写的页面实例中，对应的生命周期方法
getLifecyle (instance, lifecyle) {
  return instance[lifecyle]
}

// 在 React 中，
// 小程序触发 onShow，调用用户编写的 componentDidShow
// 小程序触发 onHide，调用用户编写的 componentDidHide
getLifecyle (instance, lifecycle) {
  if (lifecycle === 'onShow') {
    lifecycle = 'componentDidShow'
  } else if (lifecycle === 'onHide') {
    lifecycle = 'componentDidHide'
  }
  return instance[lifecycle]
}
```

<a id="ontaroelementcreate-tagname-nodetype"></a>

### onTaroElementCreate (tagName, nodeType)

`DOMElement` 构造时触发。

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| tagName | string | 当前创建的元素的标签名 |
| nodeType | NodeType | 当前创建的元素的节点类型 |

| nodeType | 说明 |
| --- | --- |
| 1 | ELEMENT\_NODE |
| 2 | ATTRIBUTE\_NODE |
| 3 | TEXT\_NODE |
| 4 | CDATA\_SECTION\_NODE |
| 5 | ENTITY\_REFERENCE\_NODE |
| 6 | COMMENT\_NODE |
| 7 | PROCESSING\_INSTRUCTION\_NODE |
| 9 | DOCUMENT\_NODE |

<a id="getpathindex-indexofnode"></a>

### getPathIndex (indexOfNode)

`DOMNode` 获取 `path` 属性时触发。

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| indexOfNode | number | 当前节点在父节点 children 列表中的下标 |

需要返回一个 **string** 值，代表小程序按路径 `setData` 时的数组下标。

例子：

```js
// 默认值：
getPathIndex (indexOfNode) {
  return `[${indexOfNode}]`
}

// 百度小程序不需要 [] 包裹
getPathIndex (indexOfNode) {
  return indexOfNode
}
```

<a id="geteventcenterevents"></a>

### getEventCenter(Events)

`Taro.eventCenter` 初始化值时触发。

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| Events |  | Taro 事件中心的构造函数 |

需要返回 Taro 事件中心的实例，其将会被赋值给 `Taro.eventCenter`。

例子：

```js
// 默认值：
getEventCenter (Events) {
  return new Events()
}

// 支付宝小程序中，
// 优先从小程序全局对象 my 中取出创建过的事件中心实例，避免分包时出现问题。
getEventCenter (Events) {
  if (!my.taroEventCenter) {
    my.taroEventCenter = new Events()
  }
  return my.taroEventCenter
}
```

<a id="initnativeapi-taro"></a>

### initNativeApi (taro)

引用 `@tarojs/taro` 包时触发。

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| taro |  | Taro 对象 |

例子：

```js
initNativeApi (taro) {
  // 为 Taro 对象增加 getApp 方法
  taro.getApp = getApp
}
```
