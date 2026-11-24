# Image

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/canvas/Image)

图片对象

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/canvas/Image.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| src | `string` | 图片的 URL |
| height | `number` | 图片的真实高度 |
| width | `number` | 图片的真实宽度 |
| referrerPolicy | `string` | origin: 发送完整的referrer; no-referrer: 不发送。<br><br>格式固定为 [https://servicewechat.com/{appid}/{version}/page-frame.html，其中](https://servicewechat.com/%7Bappid%7D/%7Bversion%7D/page-frame.html%EF%BC%8C%E5%85%B6%E4%B8%AD) {appid} 为小程序的 appid，{version} 为小程序的版本号，版本号为 0 表示为开发版、体验版以及审核版本，版本号为 devtools 表示为开发者工具，其余为正式版本<br>API 支持度: weapp |
| onerror | `(...args: any[]) => any` | 图片加载发生错误后触发的回调函数 |
| onload | `(...args: any[]) => any` | 图片加载完成后触发的回调函数 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- |
| Image | ✔️ |  |  |  |
| Image.referrerPolicy | ✔️ |  |  |  |
