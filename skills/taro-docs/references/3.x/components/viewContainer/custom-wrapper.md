# CustomWrapper

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/viewContainer/custom-wrapper)

custom-wrapper 自定义组件包裹器
当数据更新层级较深时，可用此组件将需要更新的区域包裹起来，这样更新层级将大大减少

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

<a id="类型"></a>

## 类型

```tsx
ComponentType<CustomWrapperProps>
```

<a id="示例代码"></a>

## 示例代码

```tsx
import { Component } from 'react'
import { CustomWrapper, View, Text } from '@tarojs/components'

export default class C extends Component {
  render () {
    return (
      <View>
        <CustomWrapper>
           <Text>Hello, world!</Text>
        </CustomWrapper>
      </View>
    )
  }
}
```

<a id="customwrapperprops"></a>

## CustomWrapperProps
