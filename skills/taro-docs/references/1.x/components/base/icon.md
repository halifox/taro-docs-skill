# Icon

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/components/base/icon)

<a id="图标"></a>

## 图标

> 属性

| 属性名 | 类型 | 默认值 | 说明 |
| --- | --- | --- | --- |
| type | String |  | icon 的类型，有效值：success, success\_no\_circle, info, warn, waiting, cancel, download, search, clear |
| size | Number | 23 | icon 的大小，单位 px |
| color | Color |  | icon 的颜色，同 css 的 color |

> 各端支持度

| 属性 | 微信小程序 | H5 | ReactNative | 百度小程序 | 支付宝小程序 | 抖音小程序 |
| --- | --- | --- | --- | --- | --- | --- |
| type | ✔ | ✔ | ✔ | ✔ | ✔ | ✔ |
| size | ✔ | ✔ | ✔ | ✔ | ✔ | ✔ |
| color | ✔ | ✔ | ✔ | ✔ | ✔ | ✔ |

<a id="示例"></a>

### 示例：

```jsx
import Taro, { Component } from '@tarojs/taro'
import { View, Icon } from '@tarojs/components'

export default class PageView extends Component {
  constructor() {
    super(...arguments)
  }

  render() {
    return (
      <View className='components-page'>
        <Icon size='60' type='success' />
        <Icon size='60' type='info' />
        <Icon size='60' type='warn' color='#ccc' />
        <Icon size='60' type='warn' />
        <Icon size='60' type='waiting' />
        <Icon size='20' type='success_no_circle' />
        <Icon size='20' type='warn' />
        <Icon size='20' type='success' />
        <Icon size='20' type='download' />
        <Icon size='20' type='clear' color='red' />
        <Icon size='20' type='search' />
      </View>
    )
  }
}
```
