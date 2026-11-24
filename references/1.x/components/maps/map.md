# Map

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/components/maps/map)

<a id="地图"></a>

## 地图

`<Map />` 组件的 H5 与 RN 版本尚未实现。

> 小程序端参数支持详见各小程序官网

[微信小程序 Map](https://developers.weixin.qq.com/miniprogram/dev/component/map.html)。

[百度小程序 Map](https://smartprogram.baidu.com/docs/develop/component/map/#map)。

[支付宝小程序 Map](https://docs.alipay.com/mini/component/map)。

```jsx
import Taro, { Component } from '@tarojs/taro'
// 引入 map 组件
import { Map } from '@tarojs/components'

class App extends Component {
  onTap () {}
  render () {
    return (
      <Map onClick={this.onTap} />
    )
  }
}
```
