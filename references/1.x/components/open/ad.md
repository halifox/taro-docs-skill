# Ad

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/components/open/ad)

<a id="banner-广告"></a>

## Banner 广告

> 组件 支持度

| 微信小程序 |
| --- |
| ✔ |

> 具体用法请看小程序官方文档

[微信小程序 Ad](https://developers.weixin.qq.com/miniprogram/dev/component/ad.html)。

```jsx
import Taro, { Component } from '@tarojs/taro'
// 引入 Ad 组件
import { Ad } from '@tarojs/components'

class App extends Component {
  render () {
    return (
      <Ad
        unit-id=''
        ad-intervals={60}
        onLoad={() => console.log('ad onLoad')}
        onError={() => console.log('ad onError')}
        onClose={() => console.log('ad onClose')}
      />
    )
  }
}
```
