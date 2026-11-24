# Taro.createLivePlayerContext(id, component)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/live/createLivePlayerContext)

创建 [live-player](https://developers.weixin.qq.com/miniprogram/dev/component/live-player.html) 上下文 [LivePlayerContext](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/LivePlayerContext.html) 对象。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/live/wx.createLivePlayerContext.html)

<a id="类型"></a>

## 类型

```tsx
(id: string, component?: Record<string, any>) => LivePlayerContext
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| id | `string` | [live-player](https://developers.weixin.qq.com/miniprogram/dev/component/live-player.html) 组件的 id |
| component | `Record<string, any>` | 在自定义组件下，当前组件实例的this，以操作组件内 [live-player](https://developers.weixin.qq.com/miniprogram/dev/component/live-player.html) 组件 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.createLivePlayerContext | ✔️ |  |  |
