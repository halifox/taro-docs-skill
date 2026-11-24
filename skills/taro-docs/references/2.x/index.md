# Taro 介绍

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/)

> 这是 Taro 2.x 版本的文档，若要查看 1.x 版本的文档，请[点击这里选择版本](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/versions)。

<a id="简介"></a>

## 简介

**Taro** 是一套遵循 [React](https://reactjs.org/) 语法规范的 **多端开发** 解决方案。

现如今市面上端的形态多种多样，Web、React-Native、微信小程序等各种端大行其道，当业务要求同时在不同的端都要求有所表现的时候，针对不同的端去编写多套代码的成本显然非常高，这时候只编写一套代码就能够适配到多端的能力就显得极为需要。

使用 **Taro**，我们可以只书写一套代码，再通过 **Taro** 的编译工具，将源代码分别编译出可以在不同端（[微信](https://mp.weixin.qq.com/) / [京东](https://mp.jd.com/?entrance=taro) / [百度](https://smartprogram.baidu.com/) / [支付宝](https://mini.open.alipay.com/) / [字节跳动](https://developer.open-douyin.com/) 小程序、[快应用](https://www.quickapp.cn/)、H5、React-Native 等）运行的代码。

<a id="特性"></a>

## 特性

<a id="react-语法风格"></a>

### React 语法风格

**Taro** 遵循 [React](https://reactjs.org/) 语法规范，它采用与 React 一致的组件化思想，组件生命周期与 React 保持一致，同时支持使用 [JSX 语法](jsx.md)，让代码具有更丰富的表现力，使用 **Taro** 进行开发可以获得和 React 一致的开发体验。

代码示例

```jsx
import Taro, { Component } from '@tarojs/taro'
import { View, Button } from '@tarojs/components'

export default class Index extends Component {
  constructor() {
    super(...arguments)
    this.state = {
      title: '首页',
      list: [1, 2, 3],
    }
  }

  componentWillMount() {}

  componentDidMount() {}

  componentWillUpdate(nextProps, nextState) {}

  componentDidUpdate(prevProps, prevState) {}

  shouldComponentUpdate(nextProps, nextState) {
    return true
  }

  add = (e) => {
    // dosth
  }

  render() {
    return (
      <View className="index">
        <View className="title">{this.state.title}</View>
        <View className="content">
          {this.state.list.map((item) => {
            return <View className="item">{item}</View>
          })}
          <Button className="add" onClick={this.add}>
            添加
          </Button>
        </View>
      </View>
    )
  }
}
```

> 由于微信小程序端的限制，有极少数 JSX 的优秀用法暂时不能得到很好地支持，同时，为了遵循 React 语法，Taro 在写法上也有一些自己的规范，具体可以参考：[Taro 开发最佳实践](best-practice.md) 。

<a id="快速开发微信小程序"></a>

### 快速开发微信小程序

Taro 立足于微信小程序开发，众所周知小程序的开发体验并不是非常友好，比如小程序中无法使用 npm 来进行第三方库的管理，无法使用一些比较新的 ES 规范等等，针对小程序端的开发弊端，Taro 具有以下的优秀特性

✅ 支持使用 npm/yarn 安装管理第三方依赖

✅ 支持使用 ES7/ES8 甚至更新的 ES 规范，一切都可自行配置

✅ 支持使用 CSS 预编译器，例如 Sass 等

✅ 支持使用 Redux 进行状态管理

✅ 支持使用 MobX 进行状态管理

✅ 小程序 API 优化，异步 API Promise 化等等

<a id="支持多端开发转化"></a>

### 支持多端开发转化

Taro 方案的初心就是为了打造一个多端开发的解决方案。目前 Taro 代码可以支持转换到 **微信/百度/支付宝/字节跳动/QQ/京东小程序** 、**快应用**、 **H5 端** 以及 **移动端（React Native）**。

![](https://storage.360buyimg.com/taro-resource/platforms.min.jpg)

<a id="taro-ui"></a>

## Taro UI

一款基于 `Taro` 框架开发的多端 UI 组件库。

[Taro UI](https://taro-ui.jd.com) 特性：

- 基于 `Taro` 开发 UI 组件
- 一套组件可以在 `微信小程序`，`支付宝小程序`，`百度小程序`，`H5` 多端适配运行（`ReactNative` 端暂不支持）
- 提供友好的 API，可灵活的使用组件

<a id="学习资源"></a>

## 学习资源

<a id="官方文章精选"></a>

### 官方文章精选

- [使用 React Hooks 重构你的小程序](https://aotu.io/notes/2019/07/10/taro-hooks/)
- [Taro 1.3 震撼发布：全面支持 JSX 语法和 HOOKS](https://aotu.io/notes/2019/06/13/taro-1-3/)
- [小程序框架全面测评](https://aotu.io/notes/2019/03/12/mini-program-framework-full-review/)
- [Taro 在京东购物小程序上的实践](https://aotu.io/notes/2018/09/11/taro-in-jd/)
- [用 React 开发小程序的探索之路 （演讲内容整理）| 掘金开发者大会](https://juejin.im/post/5ba346a7f265da0ad13b78bd)
- [为何我们要用 React 来写小程序 - Taro 诞生记](https://aotu.io/notes/2018/06/25/the-birth-of-taro/)
- [多端统一开发框架 - Taro 介绍](https://aotu.io/notes/2018/06/07/Taro/)

<a id="分享交流"></a>

### 分享交流

- [第十三届 D2 前端技术论坛——使用 Taro 快速构建多端应用](https://www.yuque.com/d2forum/content/d213#6a1363f4)
- [WeGeek 直播课：从 0 到 1 快速开发电商小程序](https://link.juejin.im/?target=https%3A%2F%2Fcloud.tencent.com%2Fedu%2Flearning%2Flive-1497)
- [掘金开发者大会——用 React 开发小程序的探索之路](https://www.itdks.com/Course/detail?id=16289)

<a id="其他"></a>

### 其他

更多文章教程、开源项目等，请参考：[awesome-taro](https://github.com/NervJS/awesome-taro)

掘金小册：[Taro 多端开发实现原理与实战](https://juejin.im/book/5b73a131f265da28065fb1cd?referrer=5ba228f16fb9a05d3251492d) (已下架，仅购买用户可阅)
