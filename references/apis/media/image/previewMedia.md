# Taro.previewMedia(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/media/image/previewMedia)

预览图片和视频。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/image/wx.previewMedia.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<TaroGeneral.CallbackResult>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="sources"></a>

### Sources

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| url | `string` | 是 | 图片或视频的地址 |
| type | "image" or "video" | 否 | 资源的类型（图片或视频），默认值：image |
| poster | `string` | 否 | 视频的封面图片 |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| sources | `Sources[]` | 是 | 需要预览的资源列表 |
| current | `number` | 否 | 当前显示的资源序号，默认值：0 |
| showmenu | `boolean` | 否 | 是否显示长按菜单 2.13.0，默认值：true |
| referrerPolicy | `string` | 否 | origin: 发送完整的referrer; no-referrer: 不发送。格式固定为 [https://servicewechat.com/{appid}/{version}/page-frame.html，其中](https://servicewechat.com/%7Bappid%7D/%7Bversion%7D/page-frame.html%EF%BC%8C%E5%85%B6%E4%B8%AD) {appid} 为小程序的 appid，{version} 为小程序的版本号，版本号为 0 表示为开发版、体验版以及审核版本，版本号为 devtools 表示为开发者工具，其余为正式版本；默认值：no-referrer |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.previewMedia({
  sources: []
})
```
