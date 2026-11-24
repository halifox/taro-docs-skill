# 渐进式入门教程

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/guide)

<a id="在我们开始之前"></a>

## 在我们开始之前

我们将在这个教程开发一个简单的 V2EX 论坛客户端，你将在本节教程学到 Taro 的基础知识、概念和部分优化技巧。学习这些知识并不需要事先了解 Taro、小程序开发或多端开发。当你掌握这些知识之后，你应该可以快速高效地开发多端应用。

> **提示**
>
> 这篇教程适合对喜欢边学边做或小程序开发完全没有了解的开发者，如果你倾向于按部就班地学习，请把 [文档](index.md) 的内容全部过一遍。当你看完 [文档](index.md) 就可以发现：本篇教程就是文档的渐近式索引。

这篇教程将分为四个章节：

- [环境准备](#%E7%8E%AF%E5%A2%83%E5%87%86%E5%A4%87)：当我们使用 Taro 需要安装什么东西；
- [基础教程](#%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B)：Taro 的基础概念和开发指南；
- [项目进阶与优化](#%E9%A1%B9%E7%9B%AE%E8%BF%9B%E9%98%B6%E4%B8%8E%E4%BC%98%E5%8C%96)：当项目变大变慢时，应该如何保持或提高应用的可维护性和性能；
- [多端开发](#%E5%A4%9A%E7%AB%AF%E5%BC%80%E5%8F%91)：已经使用 Taro 开发了一端的应用，如何快速拓展到多端应用。

（如果你在大屏幕浏览时）在本篇教程右边的标题目录包含了所有章节的子目录，你可以查看或导航到你感兴趣的章节。

<a id="前置知识"></a>

### 前置知识

在本篇教程中我们假定你已经对 Web 前端开发和 JavaScript 有一定的了解。我们将使用 React 和 Vue 两个框架分别实现我们的应用，在代码实例中点击 React 或 Vue 按钮就可以切换不同的实现。如果你对两个框架都不太熟悉，可以通过 [React 文档](https://zh-hans.reactjs.org/)或 [Vue 文档](https://cn.vuejs.org/)对照代码实现。

在我们的代码实现中还会使用部分 ES6 语法，你可以通过 [ES6 入门教程](https://es6.ruanyifeng.com/) 查看或学习 ES6 语法。

<a id="环境准备"></a>

## 环境准备

目前 Taro 仅提供一种开发方式：安装 Taro 命令行工具（Taro CLI）进行开发。

Taro CLI 依赖于 Node.js 环境，所以在你的机器上必须安装 Node.js 环境。安装 Node.js 环境有很多种方法，如果你完全不了解 Node.js 可以访问 [Node.js 官网](https://nodejs.org/en/) 下载一个可执行程序进行安装。请确保已具备较新的 node 环境（>=16.20.0）。

当你的机器已经存在了 Node.js 环境，可以通过在终端输入命令 `npm i -g @tarojs/cli` 安装 Taro CLI。安装完毕之后，在终端输入命令 `taro`，如果出现类似内容就说明安装成功了：

```bash
👽 Taro v3.0.0-beta.6

Usage: taro <command> [options]

Options:
  -V, --version       output the version number
  -h, --help          output usage information

Commands:
  init [projectName]  Init a project with default templete
  config <cmd>        Taro config
  create              Create page for project
  build               Build a project with options
  update              Update packages of taro
  info                Diagnostics Taro env info
  doctor              Diagnose taro project
  help [cmd]          display help for [cmd]
```

<a id="编辑器"></a>

### 编辑器

我们推荐使用 [VSCode](https://code.visualstudio.com/) 或 [WebStorm](https://www.jetbrains.com/webstorm/)（或其它支持 Web 开发的 Jetbrains IDE）。

当你使用 VSCode 时，推荐安装 [ESLint 插件](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)，如果你使用 TypeScript，别忘了配置 `eslint.probe` 参数。如果使用 Vue，推荐安装 [Vetur](https://marketplace.visualstudio.com/items?itemName=octref.vetur) 插件。

如果你愿意花钱又懒得折腾可以选择 [WebStorm](https://www.jetbrains.com/webstorm/)（或其它支持 Web 开发的 Jetbrains IDE），基本不需要配置。

不管使用 VSCode 还是 WebStrom，安装了上述插件之后使用 Taro 都实现自动补全和代码实时检查（linting）的功能。

<a id="终端"></a>

### 终端

<a id="macoslinux"></a>

#### macOS/Linux

在 \*nix 系统中终端模拟器使用什么工具（Terminal/iTerm2/Konsole/Hyper/etc..）并不重要，但运行 Taro CLI 的 shell 我们推荐使用 `bash` 或 `zsh`。

<a id="windows"></a>

#### Windows

在 Windows 中我们推荐使用内置的 `cmd` 或 `PowerShell`。如果有条件推荐安装 [WSL](https://docs.microsoft.com/zh-cn/windows/wsl/install-win10) 并使用 Linux 分发版的终端运行 Taro CLI。由于 Taro 的开发团队和 CI 都只运行或测试 \*nix 系统，部分 Windows 极端情况或许没能考虑到，导致出现 Bug。

<a id="寻求帮助"></a>

### 寻求帮助

当你在开发过程中遇到问题时，你可以扫码加入 微信开发者群![](https://camo.githubusercontent.com/10834a234b99a5880b5dff7c0ca7235e2a0772e7/687474703a2f2f696d6732302e333630627579696d672e636f6d2f7562612f6a66732f7432303139372f3238332f313638373136383837342f3133363034322f32623464383131662f35623330613635634e39643166303366312e706e67) 提问，或者去 [Taro 社区](https://taro-club.jd.com/) 提问。当你确信是 Taro 有 Bug 时，请随时向 [Taro GitHub Issue](https://github.com/NervJS/taro/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc) 提出你的问题。

<a id="基础教程"></a>

## 基础教程

安装好 Taro CLI 之后可以通过 `taro init` 命令创建一个全新的项目，你可以根据你的项目需求填写各个选项，一个最小版本的 Taro 项目会包括以下文件：

```bash
├── babel.config.js             # Babel 配置
├── .eslintrc.js                # ESLint 配置
├── config                      # 编译配置目录
│   ├── dev.js                  # 开发模式配置
│   ├── index.js                # 默认配置
│   └── prod.js                 # 生产模式配置
├── package.json                # Node.js manifest
├── dist                        # 打包目录
├── project.config.json         # 小程序项目配置
├── src # 源码目录
│   ├── app.config.js           # 全局配置
│   ├── app.css                 # 全局 CSS
│   ├── app.js                  # 入口组件
│   ├── index.html              # H5 入口 HTML
│   └── pages                   # 页面组件
│       └── index
│           ├── index.config.js # 页面配置
│           ├── index.css       # 页面 CSS
│           └── index.jsx       # 页面组件，如果是 Vue 项目，此文件为 index.vue
```

我们以后将会讲解每一个文件的作用，但现在，我们先把注意力聚焦在 `src` 文件夹，也就是源码目录：

<a id="入口组件"></a>

### 入口组件

每一个 Taro 项目都有一个入口组件和一个入口配置，我们可以在入口组件中设置全局状态/全局生命周期，一个最小化的入口组件会是这样：

**React**

src/app.js

```jsx
import React, { Component } from 'react'
import './app.css'

class App extends Component {
  render() {
    // this.props.children 是将要会渲染的页面
    return this.props.children
  }
}

// 每一个入口组件都必须导出一个 React 组件
export default App
```

**Vue**

src/app.js

```js
import Vue from 'vue'
import './app.css'

const App = {
  render(h) {
    // this.$slots.default 是将要会渲染的页面
    return h('block', this.$slots.default)
  },
}

export default App
```

每一个入口组件（例如 `app.js`）总是伴随一个全局配置文件（例如 `app.config.js`），我们可以在全局配置文件中设置页面组件的路径、全局窗口、路由等信息，一个最简单的全局配置如下：

**React**

src/app.config.js

```js
export default {
  pages: ['pages/index/index'],
}
```

**Vue**

src/app.config.js

```js
export default {
  pages: ['pages/index/index'],
}
```

你可能会注意到，不管是 React 还是 Vue，两者的全局配置是一样的。这是因为在配置文件中，Taro 并不关心框架的区别，Taro CLI 会直接在编译时在 Node.js 环境直接执行全局配置的代码，并把 `export default` 导出的对象序列化为一个 JSON 文件。接下来我们要讲到 [页面配置](#%E9%A1%B5%E9%9D%A2%E7%BB%84%E4%BB%B6) 也是同样的执行逻辑。

因此，我们必须保证配置文件是在 Node.js 环境中是可以执行的，不能使用一些在 H5 环境或小程序环境才能运行的包或者代码，否则编译将会失败。

> **了解更多**
>
> Taro 的入口组件和全局配置规范是基于微信小程序而制定的，并对全平台进行统一。
> 你可以通过访问 [React 入口组件](react-entry.md) 和 [Vue 入口组件](vue-entry.md)，以及 [全局配置](app-config.md) 了解入口组件和全局配置的详情。

<a id="页面组件"></a>

### 页面组件

页面组件是每一项路由将会渲染的页面，Taro 的页面默认放在 `src/pages` 中，每一个 Taro 项目至少有一个页面组件。在我们生成的项目中有一个页面组件：`src/pages/index/index`，细心的朋友可以发现，这个路径恰巧对应的就是我们[全局配置](app-config.md)的 `pages` 字段当中的值。一个简单的页面组件如下：

**React**

src/pages/index/index.jsx

```jsx
import { View } from '@tarojs/components'
class Index extends Component {
  state = {
    msg: 'Hello World!',
  }

  onReady() {
    console.log('onReady')
  }

  render() {
    return <View>{this.state.msg}</View>
  }
}

export default Index
```

**Vue**

src/pages/index/index.vue

```html
<template>
  <view> {{ msg }} </view>
</template>

<script>
  export default {
    data() {
      return {
        msg: 'Hello World!',
      }
    },
    onReady() {
      console.log('onReady')
    },
  }
</script>
```

这不正是我们熟悉的 React 和 Vue 组件吗！但还是有两点细微的差别：

1. `onReady` 生命周期函数。这是来源于微信小程序规范的生命周期，表示组件首次渲染完毕，准备好与视图交互。Taro 在运行时将大部分小程序规范页面生命周期注入到了页面组件中，同时 React 或 Vue 自带的生命周期也是完全可以正常使用的。
2. `View` 组件。这是来源于 `@tarojs/components` 的跨平台组件。相对于我们熟悉的 `div`、`span` 元素而言，在 Taro 中我们要全部使用这样的跨平台组件进行开发。

和入口组件一样，每一个页面组件（例如 `index.vue`）也会有一个页面配置（例如 `index.config.js`），我们可以在页面配置文件中设置页面的导航栏、背景颜色等参数，一个最简单的页面配置如下：

src/pages/index/index.config.js

```jsx
export default {
  navigationBarTitleText: '首页',
}
```

> **了解更多**
>
> Taro 的页面钩子函数和页面配置规范是基于微信小程序而制定的，并对全平台进行统一。
> 你可以通过访问 [React 页面组件](react-page.md) 和 [Vue 页面组件](vue-page.md) 了解全部页面钩子函数和页面配置规范。

<a id="自定义组件"></a>

### 自定义组件

如果你看到这里，那不得不恭喜你，你已经理解了 Taro 中最复杂的概念：入口组件和页面组件，并了解了它们是如何（通过配置文件）交互的。接下来的内容，如果你已经熟悉了 React 或 Vue 以及 Web 开发的话，那就太简单了：

我们先把首页写好，首页的逻辑很简单：把论坛最新的帖子展示出来。

**React**

src/pages/index/index.jsx

```jsx
import Taro from '@tarojs/taro'
import React from 'react'
import { View } from '@tarojs/components'
import { ThreadList } from '../../components/thread_list'
import api from '../../utils/api'

import './index.css'

class Index extends React.Component {
  config = {
    navigationBarTitleText: '首页',
  }

  state = {
    loading: true,
    threads: [],
  }

  async componentDidMount() {
    try {
      const res = await Taro.request({
        url: api.getLatestTopic(),
      })
      this.setState({
        threads: res.data,
        loading: false,
      })
    } catch (error) {
      Taro.showToast({
        title: '载入远程数据错误',
      })
    }
  }

  render() {
    const { loading, threads } = this.state
    return (
      <View className="index">
        <ThreadList threads={threads} loading={loading} />
      </View>
    )
  }
}

export default Index
```

**Vue**

src/pages/index/index.vue

```html
<template>
  <view class="index">
    <thread-list :threads="threads" :loading="loading" />
  </view>
</template>

<script>
  import Vue from 'vue'
  import Taro from '@tarojs/taro'
  import api from '../../utils/api'
  import ThreadList from '../../components/thread_list.vue'
  export default {
    components: {
      'thread-list': ThreadList,
    },
    data() {
      return {
        loading: true,
        threads: [],
      }
    },
    async created() {
      try {
        const res = await Taro.request({
          url: api.getLatestTopic(),
        })
        this.loading = false
        this.threads = res.data
      } catch (error) {
        Taro.showToast({
          title: '载入远程数据错误',
        })
      }
    },
  }
</script>
```

> **了解更多**
>
> 可能你会注意到在一个 Taro 应用中发送请求是 `Taro.request()` 完成的。
> 和页面配置、全局配置一样，Taro 的 API 规范也是基于微信小程序而制定的，并对全平台进行统一。
> 你可以通过在 [API 文档](apis/about/desc.md) 找到所有 API。

在我们的首页组件里，还引用了一个 `ThreadList` 组件，我们现在来实现它：

**React**

src/components/thread\_list.jsx

```jsx
import React from 'react'
import { View, Text } from '@tarojs/components'
import { Thread } from './thread'
import { Loading } from './loading'

import './thread.css'

class ThreadList extends React.Component {
  static defaultProps = {
    threads: [],
    loading: true,
  }

  render() {
    const { loading, threads } = this.props

    if (loading) {
      return <Loading />
    }

    const element = threads.map((thread, index) => {
      return (
        <Thread
          key={thread.id}
          node={thread.node}
          title={thread.title}
          last_modified={thread.last_modified}
          replies={thread.replies}
          tid={thread.id}
          member={thread.member}
        />
      )
    })

    return <View className="thread-list">{element}</View>
  }
}

export { ThreadList }
```

src/components/thread.jsx

```jsx
import Taro, { eventCenter } from '@tarojs/taro'
import React from 'react'
import { View, Text, Navigator, Image } from '@tarojs/components'

import api from '../utils/api'
import { timeagoInst, Thread_DETAIL_NAVIGATE } from '../utils'

class Thread extends React.Component {
  handleNavigate = () => {
    const { tid, not_navi } = this.props
    if (not_navi) {
      return
    }
    eventCenter.trigger(Thread_DETAIL_NAVIGATE, this.props)
    // 跳转到帖子详情
    Taro.navigateTo({
      url: '/pages/thread_detail/thread_detail',
    })
  }

  render() {
    const { title, member, last_modified, replies, node, not_navi } = this.props
    const time = timeagoInst.format(last_modified * 1000, 'zh')
    const usernameCls = `author ${not_navi ? 'bold' : ''}`

    return (
      <View className="thread" onClick={this.handleNavigate}>
        <View className="info">
          <View>
            <Image src={member.avatar_large} className="avatar" />
          </View>
          <View className="middle">
            <View className={usernameCls}>{member.username}</View>
            <View className="replies">
              <Text className="mr10">{time}</Text>
              <Text>评论 {replies}</Text>
            </View>
          </View>
          <View className="node">
            <Text className="tag">{node.title}</Text>
          </View>
        </View>
        <Text className="title">{title}</Text>
      </View>
    )
  }
}

export { Thread }
```

**Vue**

src/components/thread\_list.vue

```html
<template>
  <view className="thread-list">
    <loading v-if="loading" />
    <thread
      v-else
      v-for="t in threads"
      :key="t.id"
      :node="t.node"
      :title="t.title"
      :last_modified="t.last_modified"
      :replies="t.replies"
      :tid="t.id"
      :member="t.member"
    />
  </view>
</template>

<script>
  import Vue from 'vue'
  import Loading from './loading.vue'
  import Thread from './thread.vue'
  export default {
    components: {
      loading: Loading,
      thread: Thread,
    },
    props: {
      threads: {
        type: Array,
        default: [],
      },
      loading: {
        type: Boolean,
        default: true,
      },
    },
  }
</script>
```

src/components/thread.vue

```html
<template>
  <view class="thread" @tap="handleNavigate">
    <view class="info">
      <view>
        <image :src="member.avatar_large | url" class="avatar" />
      </view>
      <view class="middle">
        <view :class="usernameCls"> {{member.username}} </view>
        <view class="replies">
          <text class="mr10">{{time}}</text>
          <text>评论 {{replies}}</text>
        </view>
      </view>
      <view class="node">
        <text class="tag">{{node.title}}</text>
      </view>
    </view>
    <text class="title">{{title}}</text>
  </view>
</template>

<script>
  import Vue from 'vue'
  import { eventCenter } from '@tarojs/taro'
  import Taro from '@tarojs/taro'
  import { timeagoInst, Thread_DETAIL_NAVIGATE } from '../utils'
  import './thread.css'
  export default {
    props: ['title', 'member', 'last_modified', 'replies', 'node', 'not_navi', 'tid'],
    computed: {
      time() {
        return timeagoInst.format(this.last_modified * 1000, 'zh')
      },
      usernameCls() {
        return `author ${this.not_navi ? 'bold' : ''}`
      },
    },
    filters: {
      url(val) {
        return 'https:' + val
      },
    },
    methods: {
      handleNavigate() {
        const { tid, not_navi } = this.$props
        if (not_navi) {
          return
        }
        eventCenter.trigger(Thread_DETAIL_NAVIGATE, this.$props)
        // 跳转到帖子详情
        Taro.navigateTo({
          url: '/pages/thread_detail/thread_detail',
        })
      },
    },
  }
</script>
```

这里可以发现我们把论坛帖子渲染逻辑拆成了两个组件，并放在 `src/components` 文件中，因为这些组件是会在其它页面中多次用到。
拆分组件的力度是完全由开发者决定的，Taro 并没有规定组件一定要放在 `components` 文件夹，也没有规定页面一定要放在 `pages` 文件夹。

另外一个值得注意的点是：我们并没有使用 `div`/`span` 这样的 HTML 组件，而是使用了 `View`/`Text` 这样的跨平台组件。

> **了解更多**
>
> Taro 文档的[跨平台组件库](components-desc.md) 包含了所有组件参数和用法。但目前组件库文档中的参数和组件名都是针对 React 的（除了 React 的点击事件是 `onClick` 之外）。
> 对于 Vue 而言，组件名和组件参数都采用短横线风格（kebab-case）的命名方式，例如：`<picker-view indicator-class="myclass" />`

<a id="路由与-tabbar"></a>

### 路由与 Tabbar

在 `src/components/thread` 组件中，我们通过

```js
Taro.navigateTo({ url: '/pages/thread_detail/thread_detail' })
```

跳转到帖子详情，但这个页面仍未实现，现在我们去入口文件配置一个新的页面：

src/app.config.js

```js
export default {
  pages: ['pages/index/index', 'pages/thread_detail/thread_detail'],
}
```

然后在路径 `src/pages/thread_detail/thread_detail` 实现帖子详情页面，路由就可以跳转，我们整个流程就跑起来了：

**React**

src/pages/thread\_detail/thread\_detail

```jsx
import Taro from '@tarojs/taro'
import React from 'react'
import { View, RichText, Image } from '@tarojs/components'
import { Thread } from '../../components/thread'
import { Loading } from '../../components/loading'
import api from '../../utils/api'
import { timeagoInst, GlobalState } from '../../utils'

import './index.css'

function prettyHTML (str) {
  const lines = ['p', 'h1', 'h2', 'h3', 'h4', 'h5', 'h6']

  lines.forEach(line => {
    const regex = new RegExp(`<${line}`, 'gi')

    str = str.replace(regex, `<${line} class="line"`)
  })

  return str.replace(/<img/gi, '<img class="img"')
}

class ThreadDetail extends React.Component {
  state = {
    loading: true,
    replies: [],
    content: '',
    thread: {}
  } as IState

  config = {
    navigationBarTitleText: '话题'
  }

  componentWillMount () {
    this.setState({
      thread: GlobalState.thread
    })
  }

  async componentDidMount () {
    try {
      const id = GlobalState.thread.tid
      const [{ data }, { data: [ { content_rendered } ] } ] = await Promise.all([
        Taro.request({
          url: api.getReplies({
            'topic_id': id
          })
        }),
        Taro.request({
          url: api.getTopics({
            id
          })
        })
      ])
      this.setState({
        loading: false,
        replies: data,
        content: prettyHTML(content_rendered)
      })
    } catch (error) {
      Taro.showToast({
        title: '载入远程数据错误'
      })
    }
  }

  render () {
    const { loading, replies, thread, content } = this.state

    const replieEl = replies.map((reply, index) => {
      const time = timeagoInst.format(reply.last_modified * 1000, 'zh')
      return (
        <View className='reply' key={reply.id}>
          <Image src={reply.member.avatar_large} className='avatar' />
          <View className='main'>
            <View className='author'>
              {reply.member.username}
            </View>
            <View className='time'>
              {time}
            </View>
            <RichText nodes={reply.content} className='content' />
            <View className='floor'>
              {index + 1} 楼
            </View>
          </View>
        </View>
      )
    })

    const contentEl = loading
      ? <Loading />
      : (
        <View>
          <View className='main-content'>
          <RichText nodes={content} />
          </View>
          <View className='replies'>
            {replieEl}
          </View>
        </View>
      )

    return (
      <View className='detail'>
        <Thread
          node={thread.node}
          title={thread.title}
          last_modified={thread.last_modified}
          replies={thread.replies}
          tid={thread.id}
          member={thread.member}
          not_navi={true}
        />
        {contentEl}
      </View>
    )
  }
}

export default ThreadDetail
```

**Vue**

src/pages/thread\_detail/thread\_detail.vue

```html
<template>
  <view class="detail">
    <thread
      :node="topic.node"
      :title="topic.title"
      :last_modified="topic.last_modified"
      :replies="topic.replies"
      :tid="topic.id"
      :member="topic.member"
      :not_navi="true"
    />
    <loading v-if="loading" />
    <view v-else>
      <view class="main-content">
        <rich-text :nodes="content | html" />
      </view>
      <view class="replies">
        <view v-for="(reply, index) in replies" class="reply" :key="reply.id">
          <image :src="reply.member.avatar_large" class="avatar" />
          <view class="main">
            <view class="author"> {{reply.member.username}} </view>
            <view class="time"> {{reply.last_modified | time}} </view>
            <rich-text :nodes="reply.content_rendered | html" class="content" />
            <view class="floor"> {{index + 1}} 楼 </view>
          </view>
        </view>
      </view>
    </view>
  </view>
</template>

<script>
  import Vue from 'vue'
  import Taro from '@tarojs/taro'
  import api from '../../utils/api'
  import { timeagoInst, GlobalState, IThreadProps, prettyHTML } from '../../utils'
  import Thread from '../../components/thread.vue'
  import Loading from '../../components/loading.vue'
  import './index.css'
  export default {
    components: {
      loading: Loading,
      thread: Thread,
    },
    data() {
      return {
        topic: GlobalState.thread,
        loading: true,
        replies: [],
        content: '',
      }
    },
    async created() {
      try {
        const id = GlobalState.thread.tid
        const [
          { data },
          {
            data: [{ content_rendered }],
          },
        ] = await Promise.all([
          Taro.request({
            url: api.getReplies({
              topic_id: id,
            }),
          }),
          Taro.request({
            url: api.getTopics({
              id,
            }),
          }),
        ])
        this.loading = false
        this.replies = data
        this.content = content_rendered
      } catch (error) {
        Taro.showToast({
          title: '载入远程数据错误',
        })
      }
    },
    filters: {
      time(val) {
        return timeagoInst.format(val * 1000)
      },
      html(val) {
        return prettyHTML(val)
      },
    },
  }
</script>
```

到目前为止，我们已经实现了这个应用的所有逻辑，除去「节点列表」页面（在进阶指南我们会讨论这个页面组件）之外，剩下的页面都可以通过我们已经讲解过的组件或页面快速抽象完成。按照我们的计划，这个应用会有五个页面，分别是：

1. 首页，展示最新帖子（已完成）
2. 节点列表
3. 热门帖子（可通过组件复用）
4. 节点帖子 （可通过组件复用）
5. 帖子详情 （已完成）

其中前三个页面我们可以把它们规划在 `tabBar` 里，`tabBar` 是 Taro 内置的导航栏，可以在 `app.config.js` 配置，配置完成之后处于的 `tabBar` 位置的页面会显示一个导航栏。最终我们的 `app.config.js` 会是这样：

app.config.js

```jsx
export default {
  pages: [
    'pages/index/index',
    'pages/nodes/nodes',
    'pages/hot/hot',
    'pages/node_detail/node_detail',
    'pages/thread_detail/thread_detail',
  ],
  tabBar: {
    list: [
      {
        iconPath: 'resource/latest.png',
        selectedIconPath: 'resource/lastest_on.png',
        pagePath: 'pages/index/index',
        text: '最新',
      },
      {
        iconPath: 'resource/hotest.png',
        selectedIconPath: 'resource/hotest_on.png',
        pagePath: 'pages/hot/hot',
        text: '热门',
      },
      {
        iconPath: 'resource/node.png',
        selectedIconPath: 'resource/node_on.png',
        pagePath: 'pages/nodes/nodes',
        text: '节点',
      },
    ],
    color: '#000',
    selectedColor: '#56abe4',
    backgroundColor: '#fff',
    borderStyle: 'white',
  },
  window: {
    backgroundTextStyle: 'light',
    navigationBarBackgroundColor: '#fff',
    navigationBarTitleText: 'V2EX',
    navigationBarTextStyle: 'black',
  },
}
```

<a id="项目进阶与优化"></a>

## 项目进阶与优化

<a id="状态管理"></a>

### 状态管理

在我们实现帖子组件（`src/components/thread`）时，通过 Taro 内置的 `eventCenter` 发起了一个事件，把当前帖子的数据注入到一个全局的 `GlobalState` 中，然后在帖子详情页面再从 `GlobalState` 取出当前帖子的数据——这种简单的发布/订阅模式在处理简单逻辑时非常有效且清晰。

一旦我们的业务逻辑变得复杂，一个简单的发布订阅机制绑定到一个全局的 `state` 可能就会导致我们的数据流变得难以追踪。好在这个问题不管是在 React 还是 Vue 社区中都有很好的解决方案。我们会使用这两个社区最热门的状态管理工具：`Redux` 和 `Vuex` 来解决这个问题。

**Redux**

首先安装 `redux` 和 `react-redux`:

```bash
npm i redux react-redux
```

在入口文件使用 `react-redux` 的 `Provider` 注入 `context` 到我们的应用：

src/app.js

```js
import React, { Component } from 'react'
import { Provider } from 'react-redux'
import { createStore, combineReducers } from 'redux'
import './app.css'

const reducers = combineReducers({
  thread: (state = {}, action) => {
    if (action.type === 'SET_CURRENT_THREAD') {
      return {
        ...state,
        ...action.thread,
      }
    }
    return state
  },
})

const store = createStore(reducers)

class App extends Component {
  render() {
    // this.props.children 是将要会渲染的页面
    return <Provider store={store}>{this.props.children}</Provider>
  }
}

export default App
```

然后在帖子组件中我们就可以通过 `connect` 一个 `dispatch` 设置当前的帖子：

src/components/thread.jsx

```diff
- eventCenter.trigger(Thread_DETAIL_NAVIGATE, this.props)
+ this.props.setThread(this.props)
- export default Thread
+ const mapDispatchToProps = dispatch => {
+   return {
+     setThread: thread => dispatch({ type: 'SET_CURRENT_THREAD', thread })
+   }
+ }
+ export default connect(null, mapDispatchToProps)(Thread)
```

在帖子详情组件中通过 `connect` 一个 `mapStateToProps` 获取当前帖子的数据：

src/components/thread\_detail.jsx

```diff
- const id = GlobalState.thread.tid
+ const id = this.props.thread.tid
- export default ThreadDetail
+ function mapStateToProps(state) {
+  return { thread: state.thread }
+ }
+ export default connect(mapStateToProps)(ThreadDetail)
```

> **请注意**
>
> 此教程演示的是 `Redux` 极简用法，而非最佳实践。详情请访问 [Redux 文档](https://www.redux.org.cn/) 和 [react-redux 文档](https://react-redux.js.org/introduction/quick-start)。

**Vuex**

首先安装 `vuex`:

```bash
npm i vuex
```

在入口文件中注入 Vuex 的 `store`：

src/app.js

```js
import Vue from 'vue'
import Vuex from 'vuex'
import './app.css'

const store = new Vuex.Store({
  state: {
    thread: {},
  },
  mutations: {
    setThread: (state, thread) => {
      state.thread = { ...thread }
    },
  },
})

const App = {
  store,
  render(h) {
    // this.$slots.default 是将要会渲染的页面
    return h('block', this.$slots.default)
  },
}

export default App
```

然后在帖子组件中我们就可以通过 `this.$store.setThread()` 设置当前的帖子：

src/components/thread.vue

```diff
- eventCenter.trigger(Thread_DETAIL_NAVIGATE, this.props)
+ this.$store.setThread(this.$props)
```

在帖子详情组件中通过 `computed` 获取当前帖子的数据：

src/components/thread\_detail.vue

```diff
{
  data () {
    return {
-     topic: GlobalState.thread,
      loading: true,
      replies: [],
      content: ''
    }
  },
+ computed: {
+  topic() {
+    return this.$store.state.thread
+  }
+ }
}
```

> **请注意**
>
> 此教程演示的是 `Vuex` 极简用法，而非最佳实践。详情请访问 [Vuex 文档](https://vuex.vuejs.org/zh/guide/)。

<a id="其它状态管理工具"></a>

#### 其它状态管理工具

原理上来说，Taro 可以支持任何兼容 React 或 Vue 的状态管理工具，使用这类工具通常都会要求在入口组件注入 `context`，而在 Taro 中入口文件是不能渲染 UI 的。只要注意这点即可。

在 Vue 生态圈我们推荐使用 `Vuex`。React 生态圈状态管理工具百花齐放，考虑到使用 Taro 的开发者很多应用会编译到小程序，我们推荐几个在性能或体积上有优势的状态管理工具：

- [`mobx-react`](https://cn.mobx.js.org/): 和 Vuex 一样响应式的状态管理工具
- [unstaged](https://github.com/jamiebuilds/unstated-next): 基于 React Hooks 的极简状态管理工具，压缩体积只有 200 字节
- [Recoil](https://recoiljs.org/): Facebook 推出的基于 React Hooks 的状态管理工具

<a id="css-工具"></a>

### CSS 工具

在 Taro 中，我们可以自由地使用 CSS 预处理器和后处理器，使用的方法也非常简单，只要在编译配置添加相关的插件即可：

config/index.js

```js
const config = {
  projectName: 'v2ex',
  date: '2018-8-3',
  designWidth: 750,
  sourceRoot: 'src',
  outputRoot: 'dist',
  plugins: [
    '@tarojs/plugin-sass', // 使用 Sass
    // '@tarojs/plugin-less', // 使用 Less
    // '@tarojs/plugin-stylus', // 使用 Stylus
  ],
  defineConstants: {},
  mini: {},
  h5: {
    publicPath: '/',
    staticDirectory: 'static',
    module: {
      postcss: {
        autoprefixer: {
          enable: true,
        },
      },
    },
  },
}

module.exports = function (merge) {
  if (process.env.NODE_ENV === 'development') {
    return merge({}, config, require('./dev'))
  }
  return merge({}, config, require('./prod'))
}
```

> **了解更多**
>
> 除了 CSS 预处理器之外，Taro 还支持 [CSS Modules](css-modules.md) 和 [CSS-in-JS](css-in-js.md)。
> 原理上还支持更多 CSS 工具，我们将在 [自定义编译](#%E8%87%AA%E5%AE%9A%E4%B9%89%E7%BC%96%E8%AF%91) 继续讨论这个问题。

<a id="渲染-html"></a>

### 渲染 HTML

在帖子详情组件（`ThreadDetail`）中，我们使用了内置组件 `RichText` 来渲染 HTML，但这个组件的兼容性不好，无法在所有端都正常使用，某些特定的 HTML 元素也无法渲染。

幸运的是，Taro 内置了 HTML 渲染，使用方法也和 React/Vue 在 Web 开发中没什么区别：

**React**

src/pages/thread\_detail/thread\_detail.jsx

```diff
- <RichText nodes={reply.content} className='content' />
+ <View dangerouslySetInnerHTML={{ __html: reply.content }} className='content'></View>
```

**Vue**

src/pages/thread\_detail/thread\_detail.vue

```diff
- <rich-text :nodes="reply.content_rendered | html" class='content' />
+ <view v-html="reply.content_rendered | html" class='content' />
```

> **了解更多**
>
> Taro 内置的 HTML 渲染功能不仅可以按 Web 开发的方式去使用，也支持自定义样式、自定义渲染、自定义事件这样的高级功能。
> 你可以访问 [HTML 渲染文档](html.md) 了解更多。

<a id="性能优化"></a>

### 性能优化

<a id="虚拟列表"></a>

#### 虚拟列表

在帖子列表组件（`ThreadList`）中，我们直接渲染从远程得来的数据。这样做没有什么问题，但如果我们的数据非常庞大，或者列表渲染的 DOM 结构异常复杂，这就可能会产生性能问题。

为了解决这一问题，Taro 内置了虚拟列表（`VirtualList`）功能，比起全量渲染所有列表数据，我们只需要渲染当前可视区域(visable viewport)的视图：

**React**

src/pages/thread\_detail/thread\_list.jsx

```jsx
import React from 'react'
import { View, Text } from '@tarojs/components'
import { Thread } from './thread'
import { Loading } from './loading'
import VirtualList from '@tarojs/components-advanced/dist/components/virtual-list'

import './thread.css'

const Row = React.memo(({ thread }) => {
  return (
    <Thread
      key={thread.id}
      id={thread.id}
      node={thread.node}
      title={thread.title}
      last_modified={thread.last_modified}
      replies={thread.replies}
      tid={thread.id}
      member={thread.member}
    />
  )
})

class ThreadList extends React.Component {
  static defaultProps = {
    threads: [],
    loading: true,
  }

  render() {
    const { loading, threads } = this.props

    if (loading) {
      return <Loading />
    }

    const element = (
      <VirtualList
        height={800} /* 列表的高度 */
        width="100%" /* 列表的宽度 */
        item={Row} /* 列表单项组件，这里只能传入一个组件 */
        itemData={threads} /* 渲染列表的数据 */
        itemCount={threads.length} /* 渲染列表的长度 */
        itemSize={100} /* 列表单项的高度  */
      />
    )

    return <View className="thread-list">{element}</View>
  }
}

export { ThreadList }
```

**Vue**

app.js

```js
// 在入口文件新增使用插件
import VirtualList from '@tarojs/components-advanced/dist/components/virtual-list'
Vue.use(VirtualList)
```

src/components/row.vue

```html
<template>
  <thread
    :id="id"
    :key="thread.id"
    :node="thread.node"
    :title="thread.title"
    :last_modified="thread.last_modified"
    :replies="thread.replies"
    :tid="thread.id"
    :member="thread.member"
  />
</template>

<script>
  import Thread from './thread.vue'
  export default {
    components: {
      thread: Thread,
    },
    props: ['id', 'index', 'data'],
    computed: {
      thread() {
        return this.data[this.index]
      },
    },
  }
</script>
```

src/components/thread\_list.vue

```html
<template>
  <view className="thread-list">
    <loading v-if="loading" />
    <virtual-list
      v-else
      :height="500"
      :item-data="threads"
      :item-count="threads.length"
      :item-size="100"
      :item="Row"
      width="100%"
    />
  </view>
</template>

<script>
  import Vue from 'vue'
  import Loading from './loading.vue'
  import Thread from './thread.vue'
  import Row from './row.vue'
  export default {
    components: {
      loading: Loading,
      thread: Thread,
    },
    props: {
      threads: {
        type: Array,
        default: [],
      },
      loading: {
        type: Boolean,
        default: true,
      },
    },
  }
</script>
```

> **了解更多**
>
> 在文档[虚拟列表](virtual-list.md) 你可以找到虚拟列表的一些高级用法，例如：无限滚动、滚动偏移、滚动事件等。

<a id="预渲染"></a>

#### 预渲染

现在我们来实现最后一个页面：节点列表页面。这个页面本质说就是渲染一个存在本地的巨大列表：

**React**

src/pages/nodes/nodes.jsx

```jsx
import React from 'react'
import { View, Text, Navigator } from '@tarojs/components'
import allNodes from './all_node'
import api from '../../utils/api'

import './nodes.css'

function Nodes() {
  const element = allNodes.map((item) => {
    return (
      <View key={item.title} className="container">
        <View className="title">
          <Text style="margin-left: 5px">{item.title}</Text>
        </View>
        <View className="nodes">
          {item.nodes.map((node) => {
            return (
              <Navigator
                className="tag"
                url={`/pages/node_detail/node_detail${api.queryString(node)}`}
                key={node.full_name}
              >
                <Text>{node.full_name}</Text>
              </Navigator>
            )
          })}
        </View>
      </View>
    )
  })
  return <View className="node-container">{element}</View>
}

export default Nodes
```

**Vue**

src/pages/nodes/nodes.vue

```html
<template>
  <view class="node-container">
    <view v-for="item in allNodes" :key="item.title" class="container">
      <view class="title">
        <text style="margin-left: 5px">{{item.title}}</text>
      </view>
      <view class="nodes">
        <navigator v-for="node in item.nodes" :key="node.full_name" class="tag" :url="node | url">
          <text>{{node.full_name}}</text>
        </navigator>
      </view>
    </view>
  </view>
</template>

<script>
  import Vue from 'vue'
  import allNodes from './all_node'
  import api from '../../utils/api'
  import './nodes.css'

  function getURL(node) {
    return `/pages/node_detail/node_detail${api.queryString(node)}`
  }

  export default {
    data() {
      return {
        allNodes,
      }
    },
    filters: {
      url(node) {
        return getURL(node)
      },
    },
  }
</script>
```

这个时候我们整个应用就完成了。但如果你把这个应用放在真机小程序中，尤其是一些性能不高的真机中，切换到此页面的时间可能会比较长，会有一段白屏时间。

这是由于 Taro 的渲染机制导致的：在页面初始化时，原生小程序可以从本地直接取数据渲染，但 Taro 会把初始数据通过 React/Vue 渲染成一颗 DOM 树，然后将这颗 DOM 树序列化之后交给小程序渲染。也就是说，比起原生小程序 Taro 会在页面初始化时多一次调用 `setData` 函数的支出——而大部分小程序的性能问题是 `setData` 数据过大导致的。

为了解决这个问题，Taro 引入了一种名为预渲染（Prerender）的技术，和服务端渲染一样，在 Taro CLI 直接将要渲染的页面转换为 `wxml` 字符串，这样就获得了与原生小程序一致甚至更快的速度。

使用预渲染也非常简单，我们只要进行简单的配置即可：

config/prod.js

```js
const config = {
  ...
  mini: {
    prerender: {
      include: ['pages/nodes/nodes'], // `pages/nodes/nodes` 也会参与 prerender
    }
  }
};

// 我们这里在编译生产模式时才开启预渲染
// 如果需要开发时也开启，那就把配置放在 `config/index` 或 `config/dev`
module.exports = config
```

> **了解更多**
>
> 预渲染的配置支持条件渲染页面、条件渲染逻辑、自定义渲染函数等功能，详情可以访问[预渲染文档](prerender.md)。

<a id="打包体积"></a>

### 打包体积

默认而言使用生产模式打包，Taro 就会给你优化打包体积。但值得注意，Taro 默认的打包配置是为了让多数项目和需求都可以运行，而不是针对任何项目的最优选择。因此你可以在 Taro 配置的基础之上再针对自己的项目进行优化。

<a id="javascript"></a>

#### JavaScript

在 Taro 应用中，所有 Java(Type)Script 都是通过 `babel.config.js` 配置的，具体来说是使用 [`babel-prest-taro`](https://www.npmjs.com/package/babel-preset-taro) 这个 Babel 插件编译的。

默认而言 Taro 会兼容所有 [`@babel/preset-env`](https://www.npmjs.com/package/@babel/preset-env) 支持的语法，并兼容到 `iOS 9` 和 `Android 5`，如果你不需要那么高的兼容性，或者不需要某些 ES2015+ 语法支持，可以自行配置 `babel.config.js` 达到缩小打包体积效果。

例如我们可以把兼容性提升到 `iOS 12`：

babel.config.js

```js
// babel.config.js
module.exports = {
  presets: [
    [
      'taro',
      {
        targets: {
          ios: '12',
        },
      },
    ],
  ],
}
```

你可以访问 [Babel 文档](https://babeljs.io/) 了解更多自定义配置的信息。

<a id="打包体积分析"></a>

#### 打包体积分析

Taro 使用 [Webpack](https://www.webpackjs.com/) 作为内部的打包系统，有时候当我们的业务代码使用了 `require` 语法或者 `import default` 语法，Webpack 并不能给我们提供 `tree-shaking` 的效果。在这样的情况下我们通过 [`webpack-bundle-analyzer`](https://www.npmjs.com/package/webpack-bundle-analyzer) 来分析我们依赖打包体积，这个插件会在浏览器打开一个可视化的图表页面告诉我们引用各个包的体积。

首先安装 `webpack-bundle-analyzer` 依赖:

```bash
npm install webpack-bundle-analyzer -D
```

然后在 [mini.webpackChain](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/config-detail/#miniwebpackchain-1) 中添加如下配置：

config/index

```js
const config = {
  ...
  mini: {
    webpackChain (chain, webpack) {
      chain.plugin('analyzer')
        .use(require('webpack-bundle-analyzer').BundleAnalyzerPlugin, [])
    }
  }
}
```

运行编译命令完成之后就可以看到各文件依赖关系及体积。

你可以访问 [webpack-bundle-analyzer](https://www.npmjs.com/package/webpack-bundle-analyzer) 文档了解详细的用法。

<a id="分包"></a>

#### 分包

在一些情况，我们希望我们的页面只有当用到时才按需进行加载。这种情况在 Taro 应用被称为分包，分包的使用也非常简单，只需要通过配置入口文件 `app.config.js` 即可。

假设我们需要把刚刚实现预渲染的所有节点页面进行分包：

src/app.config.js

```js
export default {
  pages: [
    'pages/index/index',
    // 'pages/nodes/nodes', 把要分包的页面从 `pages` 字段中删除
    'pages/hot/hot',
    'pages/node_detail/node_detail',
    'pages/thread_detail/thread_detail'
  ],
  // 在 `subpackages` 字段添加分包，如果目标是支付宝小程序，还需要加一个字段 `subPackages` 值和 `subpackages` 一致
  // 不能在 `pages` 根目录也不能在 pages 目录外，需要在 `pages` 根目录另外新建文件夹做分包
  "subpackages": [
    {
      "root": "pages",
      "pages": [
        "nodes/nodes"
      ]
    }
  ]
  tabBar: {
    list: [{
      'iconPath': 'resource/latest.png',
      'selectedIconPath': 'resource/lastest_on.png',
      pagePath: 'pages/index/index',
      text: '最新'
    }, {
      'iconPath': 'resource/hotest.png',
      'selectedIconPath': 'resource/hotest_on.png',
      pagePath: 'pages/hot/hot',
      text: '热门'
    }, {
      // 如果是分包的子页面，就不能在 `tabBar` 中使用
      'iconPath': 'resource/node.png',
      'selectedIconPath': 'resource/node_on.png',
      pagePath: 'pages/nodes/nodes',
      text: '节点'
    }],
    'color': '#000',
    'selectedColor': '#56abe4',
    'backgroundColor': '#fff',
    'borderStyle': 'white'
  },
  window: {
    backgroundTextStyle: 'light',
    navigationBarBackgroundColor: '#fff',
    navigationBarTitleText: 'V2EX',
    navigationBarTextStyle: 'black'
  }
}
```

<a id="自定义编译"></a>

### 自定义编译

在特定的情况下，Taro 自带的编译系统没有办法满足我们的编译需求，这时 Taro 提供了两种拓展编译的方案：

<a id="使用-webpack-进行拓展"></a>

#### 使用 Webpack 进行拓展

在[打包体积分析](#%E6%89%93%E5%8C%85%E4%BD%93%E7%A7%AF%E5%88%86%E6%9E%90) 中我们在 [mini.webpackChain](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/config-detail/#miniwebpackchain-1) 添加了一个 Webpack 插件，达到了打包体积/依赖分析的效果。

事实上通过 `mini.webpackChain` 这个配置我们可以几乎使用任何 Webpack 生态的插件和 `loader`，例如我们想使用 `CoffeeScript` 来进行开发：

config/index

```js
const config = {
  ...
  mini: {
    webpackChain (chain, webpack) {
      // webpack-chain 详细语法请参考文档：https://github.com/neutrinojs/webpack-chain
      chain.merge({
        module: {
          rule: {
            coffeeScript: {
              test: /\.coffee$/,
              use: {
                coffeeLoader: {
                  loader: 'coffee-loader'
                }
              }
            }
          }
        }
      })
    }
  }
}
```

同样，之前我们提到过的 `CSS Modules` 也可以通过 Webpack 的形式进行拓展支持。详情可以访问 [webpack-chain](https://github.com/neutrinojs/webpack-chain) 文档了解详细的用法。

<a id="使用插件化系统进行拓展"></a>

#### 使用插件化系统进行拓展

在 [CSS 工具](#css-%E5%B7%A5%E5%85%B7) 我们已经使用了名为 `@tarojs/plugin-sass` 的插件来实现对 `Sass` 的支持。比起使用 Webpack 拓展编译，Taro 的插件功能不用在每个端都对 Webpack 进行配置，只用使用插件即可。

除此之外，Taro 的插件化功能还可以拓展 Taro CLI 编译命令，拓展编译流程，拓展编译平台，你可以访问 [插件功能文档](plugin.md) 了解更多自定义配置的信息。

> **了解更多**
>
> 除了以上两种方式外，Taro 还提供大量的编译相关选项，你可以访问 [编译配置详情](config-detail.md) 文档了解更多。

<a id="多端开发"></a>

## 多端开发

<a id="跨平台开发"></a>

### 跨平台开发

在某些情况下，不同平台的表现或业务逻辑有质的不同。在这样的情况下我们是没有办法做到「一套代码走天下」的。

例如我们正在实现 V2EX 论坛应用，当前的 API 没有办法在浏览器中跨域调用，因此我们需要在 H5 端使用另一份 API。我们可以通过内置环境变量来解决：

```diff
- import api from '../../utils/api'
// 我们可以根据不同的平台，引入不同的 API
+ let api
+ if (process.env.TARO_ENV === 'weapp') {
+  api = require('../../utils/api-weapp')
+ } else if (process.env.TARO_ENV === 'h5') {
+  api = require('../../utils/api-h5')
+ }
```

Taro 还提供了[统一接口的多端文件](envs.md#%E7%BB%9F%E4%B8%80%E6%8E%A5%E5%8F%A3%E7%9A%84%E5%A4%9A%E7%AB%AF%E6%96%87%E4%BB%B6)，通过不同的命名方式寻找依赖，在这类情况下，我们可以保留：

```js
import api from '../../utils/api'
```

语句原封不动，修改我们的文件结构，在文件名和后缀名之间加上平台的名字：

```bash
.
└── utils
    ├── api.h5.js
    ├── api.weapp.js
    └── index.js
```

> **了解更多**
>
> 除了「内置环境变量」和「统一接口的多端文件」之外，Taro 还提供了别的跨平台开发解决方案，你可以访问文档 [跨平台开发](envs.md) 了解更多。

<a id="同步调试"></a>

### 同步调试

默认情况下，Taro 会把各端打包后的文件都放在 `dist` 目录。如果你想要多端同步调试的话先编译后的文件就会被后编译好的文件覆盖。

但我们可以通过修改编译配置的 `outputRoot` 达到多端同步调试的目的：

config/index.js

```js
const config = {
  outputRoot: `dist/${process.env.TARO_ENV}`,
}
```

在这样的配置下，微信小程序编译后的目录就会是 `dist/weapp`，H5 编译后目录就会是 `dist/h5`。

<a id="使用原生小程序组件"></a>

### 使用原生小程序组件

某些情况下我们需要复用小程序既有生态，而小程序的组件/库通常是针对特定小程序写的，并不能直接在 Taro 上使用，需要一些额外的操作。

例如我们的论坛应用，在帖子详情可能服务端返回的是 MarkDown 格式，我们就需要 `towxml` 来渲染的我们的帖子：

首先我们需要在帖子详情页面的配置文件中引用 `towxml`:

```js
export default {
  usingComponents: {
    towxml: '../../towxml/towxml',
  },
}
```

然后使用 `towxml` 组件，这里必须记住的是不管是 React 还是 Vue，原生小程序组件声明需要是小写的

**React**

src/pages/thread\_detail/thread\_detail.jsx

```diff
- <View dangerouslySetInnerHTML={{ __html: reply.content }} className='content'></View>
+ <towxml nodes="{{reply.content}}" />
```

**Vue**

src/pages/thread\_detail/thread\_detail.vue

```diff
- <view v-html="reply.content_rendered | html" class='content' />
+ <towxml :nodes="reply.content_rendered | html" />
```

最后按照 [towxml](https://github.com/sbfkcel/towxml/wiki/3.0-%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8) 文档调用即可。

> **请注意**
>
> 一旦使用了原生小程序组件，Taro 应用就失去了跨端的能力。

> **了解更多**
>
> Taro 还支持使用小程序插件，详情可以访问文档[使用小程序原生第三方组件和插件](taro-in-miniapp.md)。
