# Slot

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/viewContainer/slot)

slot 插槽

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

<a id="类型"></a>

## 类型

```tsx
ComponentType<SlotProps>
```

<a id="示例代码"></a>

## 示例代码

```tsx
import { Slot, View, Text } from '@tarojs/components'

export default class SlotView extends Component {
  render () {
    return (
      <View>
        <custom-component>
          <Slot name='title'>
           <Text>Hello, world!</Text>
          </Slot>
        </custom-component>
      </View>
    )
  }
}
```

<a id="slotprops"></a>

## SlotProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| name | `string` | `none` | 否 | 指定插入的 slot 位置 |
| varName | `string` | `none` | 否 | scoped slot 传入数据源 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | 京东小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| SlotProps.name | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  |  |  | ✔️ |
| SlotProps.varName |  | ✔️ |  |  |  |  |  |  |  |  |
