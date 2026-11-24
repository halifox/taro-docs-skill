# Switch

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/components/forms/switch)

开关选择器

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/switch.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<SwitchProps>
```

<a id="示例代码"></a>

## 示例代码

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

<a id="switchprops"></a>

## SwitchProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| checked | `boolean` | `false` | 否 | 是否选中 |
| disabled | `boolean` | `false` | 否 | 是否禁用 |
| type | `"switch" \| "checkbox"` | `"switch"` | 否 | 样式，有效值：switch, checkbox |
| color | `string` | `"#04BE02"` | 否 | switch 的颜色，同 css 的 color |
| onChange | `BaseEventOrigFunction<onChangeEventDetail>` |  | 否 | checked 改变时触发 change 事件 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | H5 | React Native |
| --- | --- | --- | --- | --- | --- | --- |
| SwitchProps.checked | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| SwitchProps.disabled | ✔️ |  |  |  |  |  |
| SwitchProps.type | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| SwitchProps.color | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| SwitchProps.onChange | ✔️ |  |  |  |  |  |

<a id="onchangeeventdetail"></a>

### onChangeEventDetail

| 参数 | 类型 |
| --- | --- |
| value | `boolean` |

<a id="api-支持度-1"></a>

## API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | H5 | React Native |
| --- | --- | --- | --- | --- | --- | --- |
| Switch | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
