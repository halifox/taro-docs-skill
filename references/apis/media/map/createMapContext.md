# Taro.createMapContext(mapId, component)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/media/map/createMapContext)

创建 [map](../../../components/maps/map.md) 上下文 [MapContext](MapContext.md) 对象。

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/wx.createMapContext.html)

<a id="类型"></a>

## 类型

```tsx
(mapId: string, component?: TaroGeneral.IAnyObject) => MapContext
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| mapId | `string` | Map 组件的 id |
| component | `TaroGeneral.IAnyObject` | 在自定义组件下，当前组件实例的this，以操作组件内 Map 组件 |

<a id="示例代码"></a>

## 示例代码

```tsx
const mapCtx = Taro.createMapContext('myMap')
```
