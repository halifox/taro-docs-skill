# Switch

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/forms/switch)

开关选择器

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/switch.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<SwitchProps>
```

<a id="示例代码"></a>

## 示例代码

**React**

```tsx
export default class PageView extends Component {
  constructor() {
    super(...arguments)
  }

  render() {
    return (
      <View className='components-page'>
        <Text>默认样式</Text>
        <Switch checked/>
        <Switch/>
        <Text>推荐展示样式</Text>
        <Switch checked/>
        <Switch/>
      </View>
    )
  }
}
```

**Vue**

```html
<template>
  <view class='components-page'>
    <text>默认样式</text>
    <switch :checked="true" />
    <switch />
    <text>推荐展示样式</text>
    <switch :checked="true" />
    <switch />
  </view>
</template>
```

<a id="switchprops"></a>

## SwitchProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| checked | `boolean` | `false` | 否 | 是否选中 |
| defaultChecked | `boolean` |  | 否 | 设置在 React 非受控状态下，当前是否选中 |
| disabled | `boolean` | `false` | 否 | 是否禁用 |
| type | "switch" or "checkbox" | `"switch"` | 否 | 样式，有效值：switch, checkbox |
| color | `string` | `"#04BE02"` | 否 | switch 的颜色，同 css 的 color |
| nativeProps | `Record<string, unknown>` |  | 否 | 用于透传 `WebComponents` 上的属性到内部 H5 标签上 |
| name | `string` |  | 否 | 组件名字，用于表单提交获取数据。 |
| controlled | `string` | `false` | 否 | 是否为受控组件，为 true 时，checked 会完全受 setData 控制。 |
| ariaLabel | `string` |  | 否 | 无障碍访问，（属性）元素的额外描述 |
| onChange | `CommonEventFunction<onChangeEventDetail>` |  | 否 | checked 改变时触发 change 事件 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | 京东小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| SwitchProps.checked | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| SwitchProps.defaultChecked | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| SwitchProps.disabled | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| SwitchProps.type | ✔️ | ✔️ |  | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| SwitchProps.color | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| SwitchProps.nativeProps |  |  |  |  |  |  | ✔️ |  |  | ✔️ |  |
| SwitchProps.name |  |  | ✔️ |  |  |  |  |  |  |  |  |
| SwitchProps.controlled |  |  | ✔️ |  |  |  |  |  |  |  |  |
| SwitchProps.ariaLabel |  |  |  |  | ✔️ |  |  |  |  |  |  |
| SwitchProps.onChange | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |

<a id="onchangeeventdetail"></a>

### onChangeEventDetail

| 参数 | 类型 |
| --- | --- |
| value | `boolean` |
