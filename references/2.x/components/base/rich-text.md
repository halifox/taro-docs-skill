# RichText

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/components/base/rich-text)

富文本

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/rich-text.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<RichTextProps>
```

<a id="示例代码"></a>

## 示例代码

```tsx
class App extends Components {
  state = {
    nodes: [{
      name: 'div',
      attrs: {
        class: 'div_class',
        style: 'line-height: 60px; color: red;'
      },
      children: [{
        type: 'text',
        text: 'Hello World!'
      }]
    }]
  }
  render () {
    return (
      <RichText nodes={this.state.nodes} />
    )
  }
}
```

<a id="richtextprops"></a>

## RichTextProps

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| nodes | `Nodes` | 否 | 节点列表/ HTML String |
| space | `"ensp" \| "emsp" \| "nbsp"` | 否 | 显示连续空格 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RichTextProps.space | ✔️ |  |  |

<a id="tspace"></a>

### TSpace

space 的合法值

| 参数 | 说明 |
| --- | --- |
| ensp | 中文字符空格一半大小 |
| emsp | 中文字符空格大小 |
| nbsp | 根据字体设置的空格大小 |

<a id="text"></a>

### Text

文本节点

| 参数 | 类型 | 默认值 | 说明 | 备注 |
| --- | --- | --- | --- | --- |
| type | `"text"` |  | 文本类型 |  |
| text | `string` | `""` | 文本字符串 | `支持 entities` |

<a id="htmlelement"></a>

### HTMLElement

元素节点，默认为元素节点
全局支持class和style属性，不支持 id 属性。

| 参数 | 类型 | 必填 | 说明 | 备注 |
| --- | --- | --- | --- | --- |
| type | `"node"` | 否 | HTML 类型 |  |
| name | `string` | 是 | 标签名 | `支持部分受信任的 HTML 节点` |
| attrs | `Object` | 否 | 属性 | `支持部分受信任的属性，遵循 Pascal 命名法` |
| children | `Nodes` | 否 | 子节点列表 | `结构和 nodes 一致` |

<a id="nodes"></a>

## Nodes

节点类型

> 现支持两种节点，通过type来区分，分别是元素节点和文本节点，默认是元素节点，在富文本区域里显示的HTML节点 元素节点：type = node\*

<a id="类型-1"></a>

### 类型

```tsx
(Text | HTMLElement)[] | string
```

<a id="api-支持度-1"></a>

## API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | H5 | React Native |
| --- | --- | --- | --- | --- | --- | --- |
| RichText | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
