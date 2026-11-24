# Taro.createSelectorQuery()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/wxml/createSelectorQuery)

返回一个 SelectorQuery 对象实例。在自定义组件或包含自定义组件的页面中，应使用 `this.createSelectorQuery()` 来代替。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/wxml/wx.createSelectorQuery.html)

<a id="类型"></a>

## 类型

```tsx
() => SelectorQuery
```

<a id="参数"></a>

## 参数

<a id="示例代码"></a>

## 示例代码

```tsx
const query = Taro.createSelectorQuery()
query.select('#the-id').boundingClientRect()
query.selectViewport().scrollOffset()
query.exec(function(res){
  res[0].top       // #the-id节点的上边界坐标
  res[1].scrollTop // 显示区域的竖直滚动位置
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.createSelectorQuery | ✔️ | ✔️ |  |
