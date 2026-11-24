# Taro.createVideoContext(id, component)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/media/video/createVideoContext)

创建 video 上下文 VideoContext 对象。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/wx.createVideoContext.html)

<a id="类型"></a>

## 类型

```tsx
(id: string, component?: TaroGeneral.IAnyObject) => VideoContext
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| id | `string` | video 组件的 id |
| component | `TaroGeneral.IAnyObject` | 在自定义组件下，当前组件实例的this，以操作组件内 video 组件 |

<a id="示例代码"></a>

## 示例代码

```tsx
videoContext = Taro.createVideoContext('myVideo')
```
