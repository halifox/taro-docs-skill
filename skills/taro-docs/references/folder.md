# 目录结构

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/folder)

<a id="项目目录结构"></a>

## 项目目录结构

```text
├── dist                        编译结果目录
|
├── config                      项目编译配置目录
|   ├── index.js                默认配置
|   ├── dev.js                  开发环境配置
|   └── prod.js                 生产环境配置
|
├── src                         源码目录
|   ├── pages                   页面文件目录
|   |   └── index               index 页面目录
|   |       ├── index.js        index 页面逻辑
|   |       ├── index.css       index 页面样式
|   |       └── index.config.js index 页面配置
|   |
|   ├── app.js                  项目入口文件
|   ├── app.css                 项目总通用样式
|   └── app.config.js           项目入口配置
|
├── project.config.json         微信小程序项目配置 project.config.json
├── project.tt.json             抖音小程序项目配置 project.tt.json
├── project.swan.json           百度小程序项目配置 project.swan.json
├── project.qq.json             QQ 小程序项目配置 project.qq.json
├── ascf.config.json            ASCF元服务项目配置 ascf.config.json
|
├── babel.config.js             Babel 配置
├── tsconfig.json               TypeScript 配置
├── .eslintrc                   ESLint 配置
|
└── package.json
```

<a id="编译配置"></a>

## 编译配置

```text
└── config                      项目编译配置目录
    ├── index.js                默认配置
    ├── dev.js                  开发环境配置
    └── prod.js                 生产环境配置
```

用于配置 Taro 项目的编译行为、修改 Webpack 配置等，详情请参考[编译配置](config.md)和[编译配置详情](config-detail.md)。

<a id="源码组织"></a>

## 源码组织

和小程序规范一样，Taro 包含一个描述整体程序的 `app` 和多个描述各自页面的 `page`。

<a id="app"></a>

### app

```text
└── src                         源码目录
    ├── app.js                  项目入口文件
    ├── app.css                 项目总通用样式
    └── app.config.js           项目入口配置
```

小程序的主体由下面三个文件组成：

| 文件 | 必须 | 作用 |
| --- | --- | --- |
| app.js | 是 | 小程序入口逻辑 |
| app.css | 否 | 小程序全局样式 |
| app.config.js | 是 | 小程序全局配置 |

代码示例请根据你选择的框架进行查看：[React](react-overall.md), [Preact](preact.md), [Vue](vue-overall.md), [Vue3](vue3.md)。

<a id="1-小程序全局配置"></a>

#### 1. 小程序全局配置

`app.config.js` 对应小程序规范的全局配置文件 `app.json`，优势在于它是 JS 文件可以编写逻辑。配置以**微信小程序的全局配置**为规范。详情请参考[全局配置](app-config.md)。

<a id="2-小程序全局样式"></a>

#### 2. 小程序全局样式

小程序全局样式文件可以通过 ES6 规范的 `import` 进行引入。

app.js

```js
import './app.css'
```

<a id="page"></a>

### page

```text
└── src                         源码目录
    └── pages                   页面文件目录
        └── index               index 页面目录
            ├── index.js        index 页面逻辑
            ├── index.css       index 页面样式
            └── index.config.js index 页面配置
```

一个小程序页面由三个文件组成，如下：

| 文件 | 必须 | 作用 |
| --- | --- | --- |
| page.js | 是 | 页面入口逻辑 |
| page.css | 否 | 页面样式 |
| page.config.js | 否 | 页面配置 |

<a id="1-页面配置"></a>

#### 1. 页面配置

`page.config.js` 对应小程序规范的页面配置文件 `page.json`，优势在于它是 JS 文件可以编写逻辑。配置以**微信小程序的页面配置**为规范。详情请参考[页面配置](page-config.md)。

<a id="2-页面样式"></a>

#### 2. 页面样式

页面的样式文件可以通过 ES6 规范的 `import` 进行引入。

pages/index/index.js

```js
import './index.css'
```

<a id="3-页面路由"></a>

#### 3. 页面路由

页面路由与小程序规范一致，需要在小程序全局配置 `app.config.js` 中进行配置。

<a id="项目配置"></a>

## 项目配置

```text
└──project.config.json         微信小程序项目配置 project.config.json
```

各类小程序平台均有自己的项目配置文件，Taro 支持对它们进行适配，详情请参考[项目配置](project-config.md)。

<a id="babel-配置"></a>

## Babel 配置

```text
└── babel.config.js             Babel 配置
```

请参考 [Babel 配置](babel-config.md)

<a id="eslint-配置"></a>

## ESLint 配置

```text
└── .eslintrc                   ESLint 配置
```

ESLint 配置请参考 [Github](https://github.com/NervJS/taro/tree/next/packages/eslint-config-taro)
