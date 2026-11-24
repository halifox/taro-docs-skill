# WebView

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/open/web-view)

web-view 组件是一个可以用来承载网页的容器，会自动铺满整个小程序页面。个人类型与海外类型的小程序暂不支持使用。

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/web-view.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<WebViewProps>
```

<a id="示例代码"></a>

## 示例代码

**React**

```tsx
class App extends Component {
  handleMessage () {}

  render () {
    return (
      <WebView src='https://mp.weixin.qq.com/' onMessage={this.handleMessage} />
    )
  }
}
```

**Vue**

```html
<template>
  <web-view src='https://mp.weixin.qq.com/' @message="handleMessage" />
</template>
```

<a id="webviewprops"></a>

## WebViewProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| src | `string` |  | 是 | webview 指向网页的链接。可打开关联的公众号的文章，其它网页需登录小程序管理后台配置业务域名。 |
| progressbarColor | `string` |  | 否 | webview 的进度条颜色 |
| type | `string` | `default` | 否 | 若使用web-view组件引入第三方客服，必须填写type="im" |
| onMessage | `CommonEventFunction<onMessageEventDetail>` |  | 否 | 网页向小程序 postMessage 时，会在特定时机（小程序后退、组件销毁、分享）触发并收到消息。e.detail = { data } |
| onLoad | `CommonEventFunction<onLoadEventDetail>` |  | 否 | 网页加载成功时候触发此事件。e.detail = { src } |
| onError | `CommonEventFunction<onErrorEventDetail>` |  | 否 | 网页加载失败的时候触发此事件。e.detail = { src } |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | 京东小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| WebViewProps.src | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| WebViewProps.progressbarColor |  |  |  | ✔️ |  |  |  |  |  |  |  |
| WebViewProps.type |  |  |  | ✔️ |  |  |  |  |  |  |  |
| WebViewProps.onMessage | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  |  |  |  | ✔️ |
| WebViewProps.onLoad | ✔️ |  | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |  | ✔️ | ✔️ |
| WebViewProps.onError | ✔️ |  | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |  | ✔️ | ✔️ |

<a id="onmessageeventdetail"></a>

### onMessageEventDetail

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | `any[]` | 消息数据，是多次 postMessage 的参数组成的数组 |

<a id="onloadeventdetail"></a>

### onLoadEventDetail

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| src | `string` | 网页链接 |

<a id="onerroreventdetail"></a>

### onErrorEventDetail

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| src | `string` | 网页链接 |
