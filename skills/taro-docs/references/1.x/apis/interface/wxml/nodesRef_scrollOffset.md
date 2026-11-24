# nodesRef.scrollOffset([callback])

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/interface/wxml/nodesRef_scrollOffset)

添加节点的滚动位置查询请求，以像素为单位。节点必须是 scroll-view 或者 viewport。返回值是 nodesRef 对应的 selectorQuery。

返回的节点信息中，每个节点的滚动位置用 scrollLeft、scrollTop 字段描述。如果提供了 callback 回调函数，在执行 selectQuery 的 exec 方法后，节点信息会在 callback 中返回。

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.createSelectorQuery()
  .selectViewport()
  .scrollOffset(rect => {
    rect.id      // 节点的 ID
    rect.dataset // 节点的 dataset
    res.scrollLeft // 节点的水平滚动位置
    res.scrollTop  // 节点的竖直滚动位置
  })
  .exec()
})
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| selectorQuery.in | ✔️ | ✔️ |  |
| selectorQuery.select | ✔️ | ✔️ |  |
| selectorQuery.selectAll | ✔️ | ✔️ |  |
| selectorQuery.selectViewport | ✔️ | ✔️ |  |
| nodesRef.boundingClientRect | ✔️ | ✔️ |  |
| nodesRef.scrollOffset | ✔️ | ✔️ |  |
| nodesRef.fields | ✔️ | ✔️ |  |
| selectorQuery.exec | ✔️ | ✔️ |  |
