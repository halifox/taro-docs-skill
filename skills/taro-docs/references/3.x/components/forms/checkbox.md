# Checkbox

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/forms/checkbox)

多选项目

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/checkbox.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<CheckboxProps>
```

<a id="示例代码"></a>

## 示例代码

**React**

```tsx
export default class PageCheckbox extends Component {
  state = {
    list: [
      {
        value: '美国',
        text: '美国',
        checked: false
      },
      {
        value: '中国',
        text: '中国',
        checked: true
      },
      {
        value: '巴西',
        text: '巴西',
        checked: false
      },
      {
        value: '日本',
        text: '日本',
        checked: false
      },
      {
        value: '英国',
        text: '英国',
        checked: false
      },
      {
        value: '法国',
        text: '法国',
        checked: false
      }
    ]
  }
  render () {
    return (
      <View className='page-body'>
        <View className='page-section'>
          <Text>默认样式</Text>
          <Checkbox value='选中' checked>选中</Checkbox>
          <Checkbox style='margin-left: 20rpx' value='未选中'>未选中</Checkbox>
        </View>
        <View className='page-section'>
          <Text>推荐展示样式</Text>
          {this.state.list.map((item, i) => {
            return (
              <Label className='checkbox-list__label' for={i} key={i}>
                <Checkbox className='checkbox-list__checkbox' value={item.value} checked={item.checked}>{item.text}</Checkbox>
              </Label>
            )
          })}
        </View>
      </View>
    )
  }
}
```

**Vue**

```html
<template>
  <view class="container">
    <view class="page-section">
      <text>默认样式</text>
      <checkbox value="选中" :checked="true">选中</checkbox>
      <checkbox style="margin-left: 20rpx;" value="未选中">未选中</checkbox>
    </view>
    <view class="page-section">
      <text>推荐展示样式(Taro 团队成员):</text>
      <label v-for="item in list" class="checkbox-list__label">
        <checkbox class="checkbox-list__checkbox" :value="item.value" :checked="item.checked">{{ item.text }}</checkbox>
      </label>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      list: [
        {
          value: '美国',
          text: '美国',
          checked: false
        },
        {
          value: '中国',
          text: '中国',
          checked: true
        },
        {
          value: '巴西',
          text: '巴西',
          checked: false
        },
        {
          value: '日本',
          text: '日本',
          checked: false
        },
        {
          value: '英国',
          text: '英国',
          checked: false
        },
        {
          value: '法国',
          text: '法国',
          checked: false
        }
      ]
    }
  }
}
</script>
```

<a id="checkboxprops"></a>

## CheckboxProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| value | `string` |  | 是 | `<Checkbox/>`标识，选中时触发`<CheckboxGroup/>`的 change 事件，并携带 `<Checkbox/>` 的 value |
| disabled | `boolean` | `false` | 否 | 是否禁用 |
| checked | `boolean` | `false` | 否 | 当前是否选中，可用来设置默认选中 |
| color | `string` |  | 否 | checkbox的颜色，同 css 的 color |
| name | `string` |  | 否 | Checkbox 的名字 |
| nativeProps | `Record<string, unknown>` |  | 否 | 用于透传 `WebComponents` 上的属性到内部 H5 标签上 |
| ariaLabel | `string` |  | 否 | 无障碍访问，（属性）元素的额外描述 |
| onChange | `CommonEventFunction<{ value: string[]; }>` |  | 否 | 选中项发生变化时触发 change 事件，小程序无此 API |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | 京东小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| CheckboxProps.value | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| CheckboxProps.disabled | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| CheckboxProps.checked | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| CheckboxProps.color | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| CheckboxProps.name |  |  |  |  |  |  | ✔️ |  | ✔️ | ✔️ |  |
| CheckboxProps.nativeProps |  |  |  |  |  |  | ✔️ |  |  | ✔️ |  |
| CheckboxProps.ariaLabel |  |  |  |  | ✔️ |  |  |  |  |  |  |
| CheckboxProps.onChange |  |  | ✔️ |  |  |  | ✔️ | ✔️ |  | ✔️ |  |
