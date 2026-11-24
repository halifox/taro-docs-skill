# Icon

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/base/icon)

图标。组件属性的长度单位默认为 px

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/icon.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<IconProps>
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

**Vue**

<a id="iconprops"></a>

## IconProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| type | `keyof TIconType` |  | 是 | icon 的类型 |
| size | `number` | `23` | 否 | icon 的大小，单位px |
| color | `string` |  | 否 | icon 的颜色，同 css 的 color |
| ariaLabel | `string` |  | 否 | 无障碍访问，（属性）元素的额外描述 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | 京东小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| IconProps.type | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| IconProps.size | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| IconProps.color | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| IconProps.ariaLabel |  |  |  |  | ✔️ |  |  |  |  |  |  |

<a id="ticontype"></a>

### TIconType

icon 的类型

| 参数 | 说明 |
| --- | --- |
| success | 成功图标 |
| success\_no\_circle | 成功图标（不带外圈） |
| info | 信息图标 |
| warn | 警告图标 |
| waiting | 等待图标 |
| cancel | 取消图标 |
| download | 下载图标 |
| search | 搜索图标 |
| clear | 清除图标 |
| circle | 圆环图标(多选控件图标未选择)「微信文档未标注属性」 |
| info\_circle | 带圆环的信息图标「微信文档未标注属性」 |
