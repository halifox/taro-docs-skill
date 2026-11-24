# RichText

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/components/base/rich-text)

<a id="富文本"></a>

## 富文本

> 属性

| 属性名 | 类型 | 默认值 | 说明 |
| --- | --- | --- | --- |
| nodes | Array / String | [] | 节点列表 / HTML String |

> 各端支持度

| 属性 | 微信小程序 | H5 | ReactNative | 百度小程序 | 支付宝小程序 | 抖音小程序 |
| --- | --- | --- | --- | --- | --- | --- |
| nodes | ✔ | ✔ | ✔ | ✔ | ✔ | ✔ |

<a id="示例"></a>

### 示例：

```jsx
import Taro, { Component } from '@tarojs/taro'
// 引入 RichText 组件
import { RichText } from '@tarojs/components'

class App extends Components {
  state = {
    nodes: [{
      name: 'div',
      attrs: {
        class: 'div_class',
        style: 'line-height: 60px; color: red;'
      },
      children: [{
        type: 'text',
        text: 'Hello World!'
      }]
    }]
  }
  render () {
    return (
      <RichText nodes={this.state.nodes} />
    )
  }
}
```
