# View

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/components/viewContainer/view)

视图容器

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/view.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<ViewProps>
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
        <Text>flex-direction: row 横向布局</Text>
        <View className='flex-wrp' style='flex-direction:row;'>
          <View className='flex-item demo-text-1'/>
          <View className='flex-item demo-text-2'/>
          <View className='flex-item demo-text-3'/>
        </View>
        <Text>flex-direction: column 纵向布局</Text>
        <View className='flex-wrp' style='flex-direction:column;'>
          <View className='flex-item flex-item-V demo-text-1'/>
          <View className='flex-item flex-item-V demo-text-2'/>
          <View className='flex-item flex-item-V demo-text-3'/>
        </View>
      </View>
    )
  }
}
```

<a id="viewprops"></a>

## ViewProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| hoverClass | `string` | `none` | 否 | 指定按下去的样式类。当 `hover-class="none"` 时，没有点击态效果 |
| hoverStyle | `string` | `none` | 否 | 由于 RN 不支持 Class，故 RN 端的 View 组件实现了 `hoverStyle`属性，写法和 style 类似，只不过 `hoverStyle` 的样式是指定按下去的样式。 |
| hoverStopPropagation | `boolean` | `fasle` | 否 | 指定是否阻止本节点的祖先节点出现点击态 |
| hoverStartTime | `number` | `50` | 否 | 按住后多久出现点击态，单位毫秒 |
| hoverStayTime | `number` | `400` | 否 | 手指松开后点击态保留时间，单位毫秒 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | H5 | React Native |
| --- | --- | --- | --- | --- | --- | --- |
| ViewProps.hoverClass | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | (由于 RN 不支持 Class，故 RN 端的 View 组件实现了 `hoverStyle`属性，写法和 style 类似，只不过 `hoverStyle` 的样式是指定按下去的样式。) |
| ViewProps.hoverStyle |  |  |  |  |  | ✔️ |
| ViewProps.hoverStopPropagation | ✔️ | ✔️ | ✔️ | ✔️ |  |  |
| ViewProps.hoverStartTime | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| ViewProps.hoverStayTime | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |

<a id="api-支持度-1"></a>

## API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | H5 | React Native |
| --- | --- | --- | --- | --- | --- | --- |
| View | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
