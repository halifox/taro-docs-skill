# Vue3 Pinia

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/pinia)

Taro Vue3 支持使用 [Pinia](https://pinia.vuejs.org/) 进行状态管理。

<a id="安装"></a>

## 安装

```bash
$ yarn add pinia
# 或者使用 npm
$ npm install pinia
```

> [pinia@2.0.22](mailto:pinia@2.0.22) 已经解决了这个问题（[#967](https://github.com/vuejs/pinia/pull/967)）, 所以你可能不再需要这个插件

<a id="例子"></a>

## 例子

- 运行 `taro init` 命令时选择 Vue3 -> pinia 即可创建 vue3-pinia 模板项目
- [Todo App](https://github.com/NervJS/taro-todos-pinia)

<a id="使用"></a>

## 使用

<a id="创建-pinia-实例"></a>

### 创建 Pinia 实例

src/app.js

```js
import { createApp } from 'vue'
import { createPinia } from 'pinia'

const App = createApp({})

App.use(createPinia())

export default App
```

<a id="创建-store"></a>

### 创建 `store`

在项目中新建 `src/store/index.js` 文件用来配置 `store`：

src/store/index.js

```js
import { defineStore } from 'pinia'

export const useCounterStore = defineStore('counter', {
  state: () => {
    return { count: 0 }
  },
  actions: {
    increment() {
      this.count++
    },
  },
})
```

<a id="使用-store-定义的数据与方法"></a>

### 使用 store 定义的数据与方法

```html
<template>
  <view>
    <text>{{ counter.count }}</text>
    <view @tap="onAdd">ADD</view>
  </view>
</template>

<script>
  import { useCounterStore } from '../stores'

  export default {
    setup() {
      const counter = useCounterStore()

      const onAdd = () => {
        counter.count++
      }

      return {
        counter,
        onAdd,
      }
    },
  }
</script>
```
