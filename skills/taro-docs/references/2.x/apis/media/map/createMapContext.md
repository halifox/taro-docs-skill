# Taro.createMapContext(mapId, component)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/map/createMapContext)

创建 [map](https://developers.weixin.qq.com/miniprogram/dev/component/map.html) 上下文 [MapContext](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.html) 对象。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/wx.createMapContext.html)

<a id="类型"></a>

## 类型

```tsx
(mapId: string, component?: Record<string, any>) => MapContext
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| mapId | `string` | Map 组件的 id |
| component | `Record<string, any>` | 在自定义组件下，当前组件实例的this，以操作组件内 Map 组件 |

<a id="示例代码"></a>

## 示例代码

```tsx
const mapCtx = Taro.createMapContext('myMap')
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.createMapContext | ✔️ |  |  |
