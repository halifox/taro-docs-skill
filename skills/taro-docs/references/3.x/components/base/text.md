# Text

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/base/text)

文本

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/text.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<TextProps>
```

<a id="示例代码"></a>

## 示例代码

**React**

```tsx
export default class PageView extends Component {
  state = {
    contents: [],
    contentsLen: 0
  }

  add = () => {
    this.setState(prev => {
      const cot = prev.contents.slice()
      cot.push({ text: 'hello world' })
      return {
        contents: cot,
        contentsLen: cot.length
      }
    })
  }

  remove = () => {
    this.setState(prev => {
      const cot = prev.contents.slice()
      cot.pop()
      return {
        contents: cot,
        contentsLen: cot.length
      }
    })
  }

  render () {
    return (
      <View className='container'>
        {this.state.contents.map((item, index) => (
          <Text key={index}>{item.text}</Text>
        ))}
        <Button className='btn-max-w button_style' plain type='default' onClick={this.add}>add line</Button>
        <Button className='btn-max-w button_style' plain type='default' disabled={this.state.contentsLen ? false : true} onClick={this.remove}>remove line</Button>
      </View>
    )
  }
}
```

**Vue**

```html
<template>
  <view class="container">
    <view v-for="(item, index) in contents">
      <text>{{item.text}} line {{index + 1}}</text>
    </view>
    <button class="btn-max-w button_style" :plain="true" type="default" @tap="add">add line</button>
    <button class="btn-max-w button_style" :plain="true" type="default" :disabled="contentsLen ? false : true" @tap="remove">remove line</button>
</template>

<script>
export default {
  data() {
    return {
      contents: [],
      contentsLen: 0
    }
  },
  methods: {
    add () {
      const cot = this.contents.slice()
      cot.push({ text: 'hello world' })
      this.contents = cot
      this.contentsLen = cot.length
    },

    remove () {
      const cot = this.contents.slice()
      cot.pop()
      this.contents = cot
      this.contentsLen = cot.length
    }
  }
}
</script>
```

<a id="textprops"></a>

## TextProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| selectable | `boolean` | `false` | 否 | 文本是否可选 |
| userSelect | `boolean` | `false` | 否 | 文本是否可选，该属性会使文本节点显示为 inline-block |
| space | `keyof TSpace` |  | 否 | 显示连续空格 |
| decode | `boolean` | `false` | 否 | 是否解码 |
| numberOfLines | `number` |  | 否 | 多行省略，值须大于等于 1，表现同 css 的 -webkit-line-clamp 属性一致。 |
| overflow | `keyof Overflow` | `'visible'` | 否 | 文本溢出处理 |
| maxLines | `number` |  | 否 | 限制文本最大行数 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | 京东小程序 | H5 | React Native | Harmony | Harmony hybrid |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| TextProps.selectable | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ |
| TextProps.userSelect | ✔️ |  |  |  |  |  | ✔️ |  |  | ✔️ |
| TextProps.space | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  |  | ✔️ |
| TextProps.decode | ✔️ |  | ✔️ | ✔️ | ✔️ | ✔️ | (默认解码，不支持设置) |  |  |  |
| TextProps.numberOfLines |  |  | ✔️ |  |  |  |  |  |  |  |
| TextProps.overflow |  |  |  |  |  |  |  |  |  |  |
| TextProps.maxLines | ✔️ |  |  |  |  |  |  |  |  |  |

<a id="tspace"></a>

### TSpace

space 的合法值

| 参数 | 说明 |
| --- | --- |
| ensp | 中文字符空格一半大小 |
| emsp | 中文字符空格大小 |
| nbsp | 根据字体设置的空格大小 |

<a id="overflow"></a>

### Overflow

| 参数 | 说明 |
| --- | --- |
| clip | 修剪文本 |
| fade | 淡出 |
| ellipsis | 显示省略号 |
| visible | 文本不截断 |
