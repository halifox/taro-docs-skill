# WebView

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/components/open/web-view)

<a id="webview-组件是一个可以用来承载网页的容器会自动铺满整个小程序页面个人类型与海外类型的小程序暂不支持使用"></a>

## WebView 组件是一个可以用来承载网页的容器，会自动铺满整个小程序页面。个人类型与海外类型的小程序暂不支持使用

> 组件 支持度

| H5 | ReactNative |
| --- | --- |
| ✔ | ✔ |

> 其他相关属性请看各小程序官方文档

[微信小程序 WebView](https://developers.weixin.qq.com/miniprogram/dev/component/web-view.html)。

[百度小程序 WebView](https://smartprogram.baidu.com/docs/develop/component/open/#web-view)。

[支付宝小程序 WebView](https://docs.alipay.com/mini/component/web-view)。

[抖音小程序 WebView](https://developer.open-douyin.com/docs/resource/zh-CN/mini-app/develop/component/open-capacity/web-view/)。

```jsx
import Taro, { Component } from '@tarojs/taro'
// 引入 WebView 组件
import { WebView } from '@tarojs/components'

class App extends Component {
  render () {
    return (
      <WebView src='https://mp.weixin.qq.com/'  />
    )
  }
}
```
