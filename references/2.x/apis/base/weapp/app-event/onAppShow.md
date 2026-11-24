# Taro.onAppShow(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/base/weapp/app-event/onAppShow)

监听小程序切前台事件。该事件与 [`App.onShow`](https://developers.weixin.qq.com/miniprogram/dev/reference/api/App.html#onshowobject-object) 的回调参数一致。

**返回有效 referrerInfo 的场景**

| 场景值 | 场景 | appId含义 |
| --- | --- | --- |
| 1020 | 公众号 profile 页相关小程序列表 | 来源公众号 |
| 1035 | 公众号自定义菜单 | 来源公众号 |
| 1036 | App 分享消息卡片 | 来源App |
| 1037 | 小程序打开小程序 | 来源小程序 |
| 1038 | 从另一个小程序返回 | 来源小程序 |
| 1043 | 公众号模板消息 | 来源公众号 |

**注意**

部分版本在无`referrerInfo`的时候会返回 `undefined`，建议使用 `options.referrerInfo && options.referrerInfo.appId` 进行判断。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/app/app-event/wx.onAppShow.html)

<a id="类型"></a>

## 类型

```tsx
(callback: (result: CallbackResult) => void) => void
```

<a id="参数"></a>

## 参数

<a id="callbackresult"></a>

### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| path | `string` | 小程序切前台的路径 |
| query | `Record<string, any>` | 小程序切前台的 query 参数 |
| referrerInfo | `ResultReferrerInfo` | 来源信息。从另一个小程序、公众号或 App 进入小程序时返回。否则返回 {}。(参见后文注意) |
| scene | `number` | 小程序切前台的[场景值](https://developers.weixin.qq.com/miniprogram/dev/framework/app-service/scene.html) |
| shareTicket | `string` | shareTicket，详见[获取更多转发信息](https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/share.html) |

<a id="resultreferrerinfo"></a>

### ResultReferrerInfo

来源信息。从另一个小程序、公众号或 App 进入小程序时返回。否则返回 `{}`。(参见后文注意)

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| appId | `string` | 来源小程序、公众号或 App 的 appId |
| extraData | `Record<string, any>` | 来源小程序传过来的数据，scene=1037或1038时支持 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.onAppShow | ✔️ |  |  |
