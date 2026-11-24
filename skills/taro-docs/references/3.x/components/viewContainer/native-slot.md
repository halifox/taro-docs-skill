# NativeSlot

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/viewContainer/native-slot)

编译的原生组件支持使用 slot 插槽

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://github.com/NervJS/taro/pull/12627)

<a id="类型"></a>

## 类型

```tsx
ComponentType<NativeSlotProps>
```

<a id="示例代码"></a>

## 示例代码

```tsx
import { NativeSlot, View } from '@tarojs/components'

export default function () {
  render () {
    return (
      <View>
        <NativeSlot />
      </View>
    )
  }
}
```

<a id="nativeslotprops"></a>

## NativeSlotProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| name | `string` | `none` | 否 | 指定插入的 slot 位置 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | 京东小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| NativeSlotProps.name | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  |  |  |
