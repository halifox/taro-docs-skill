# 安装及使用

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/GETTING-STARTED)

<a id="安装"></a>

## 安装

Taro 项目基于 node，请确保已具备较新的 node 环境（>=8.0.0），推荐使用 node 版本管理工具 [nvm](https://github.com/creationix/nvm) 来管理 node，这样不仅可以很方便地切换 node 版本，而且全局安装时候也不用加 sudo 了。

<a id="cli-工具安装"></a>

### CLI 工具安装

首先，你需要使用 npm 或者 yarn 全局安装 `@tarojs/cli`，或者直接使用 [npx](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b):

```bash
# 使用 npm 安装 CLI
$ npm install -g @tarojs/cli
# OR 使用 yarn 安装 CLI
$ yarn global add @tarojs/cli
# OR 安装了 cnpm，使用 cnpm 安装 CLI
$ cnpm install -g @tarojs/cli
```

<a id="查看-taro-全部版本信息"></a>

#### 查看 Taro 全部版本信息

可以使用 `npm info` 查看 Taro 版本信息，在这里你可以看到当前最新版本

```bash
npm info @tarojs/cli
```

![npm info @tarojs/cli screenshot](https://img13.360buyimg.com/ling/jfs/t1/144770/7/20011/138415/5fe40491Ed0883578/11236962a3e672db.png)

由图第 1 行可知最新版本，如果你用的是 beta 或者 canary 你可以通过 `dist-tags:` 下面那行看到最新的版本。

<a id="注意事项"></a>

### 注意事项

值得一提的是，如果安装过程出现`sass`相关的安装错误，请在安装[`mirror-config-china`](https://www.npmjs.com/package/mirror-config-china)后重试。

```bash
$ npm install -g mirror-config-china
```

<a id="项目初始化"></a>

## 项目初始化

使用命令创建模板项目

```bash
$ taro init myApp
```

npm 5.2+ 也可在不全局安装的情况下使用 npx 创建模板项目

```bash
$ npx @tarojs/cli init myApp
```

![taro init myApp command screenshot](https://img30.360buyimg.com/ling/jfs/t1/121270/15/15083/672721/5f89357dEf36b7fe2/ecb98df1436cd3d5.jpg)

在创建完项目之后，Taro 会默认开始安装项目所需要的依赖，安装使用的工具按照 yarn>cnpm>npm 顺序进行检测，一般来说，依赖安装会比较顺利，但某些情况下可能会安装失败，这时候你可以在项目目录下自己使用安装命令进行安装

```bash
# 使用 yarn 安装依赖
$ yarn
# OR 使用 cnpm 安装依赖
$ cnpm install
# OR 使用 npm 安装依赖
$ npm install
```

进入项目目录开始开发，目前已经支持 微信/百度/支付宝/字节跳动/QQ/京东小程序、H5、快应用以及 ReactNative 等端的代码转换，针对不同端的启动以及预览、打包方式并不一致

<a id="运行"></a>

## 运行

Taro 需要运行不同的命令，将 Taro 代码编译成不同端的代码，然后在对应的开发工具中查看效果。

![image](https://storage.360buyimg.com/taro-resource/platforms.jpg)

<a id="保持-tarojscli-的版本与各端依赖版本一致"></a>

### 保持 `@tarojs/cli` 的版本与各端依赖版本一致

在使用 Taro 进行多端开发中，请确保 Taro CLI 的版本与你项目的依赖版本一致，否则可能会出现编译错误或者运行时错误。

如果你所使用的 Taro CLI 版本为 1.3.9，而项目里使用的依赖版本为 1.3.20，则有可能会出现问题，查询方法请参见本章 "环境及依赖检测" 章节，这时请将你的 Taro CLI 版本更新至项目依赖版本号相同的版本，如果还是出现问题，请向我们提出 [Issue](https://github.com/NervJS/taro/issues/new?assignees=&labels=&template=bug_report.md&title=)。

<a id="微信小程序"></a>

### 微信小程序

选择微信小程序模式，需要自行下载并打开[微信开发者工具](https://developers.weixin.qq.com/miniprogram/dev/devtools/download.html)，然后选择项目根目录进行预览。

微信小程序编译预览及打包（去掉 --watch 将不会监听文件修改，并会对代码进行压缩打包）

```bash
# yarn
$ yarn dev:weapp
$ yarn build:weapp
# npm script
$ npm run dev:weapp
$ npm run build:weapp
# 仅限全局安装
$ taro build --type weapp --watch
$ taro build --type weapp
# npx 用户也可以使用
$ npx taro build --type weapp --watch
$ npx taro build --type weapp
```

<a id="百度小程序"></a>

### 百度小程序

选择百度小程序模式，需要自行下载并打开[百度开发者工具](https://smartprogram.baidu.com/docs/develop/devtools/show_sur/)，然后在项目编译完后选择项目根目录下 `dist` 目录进行预览。

百度小程序编译预览及打包（去掉 --watch 将不会监听文件修改，并会对代码进行压缩打包）

```bash
# yarn
$ yarn dev:swan
$ yarn build:swan
# npm script
$ npm run dev:swan
$ npm run build:swan
# 仅限全局安装
$ taro build --type swan --watch
$ taro build --type swan
# npx 用户也可以使用
$ npx taro build --type swan --watch
$ npx taro build --type swan
```

<a id="支付宝小程序"></a>

### 支付宝小程序

选择支付宝小程序模式，需要自行下载并打开[支付宝小程序开发者工具](https://docs.alipay.com/mini/developer/getting-started/)，然后在项目编译完后选择项目根目录下 `dist` 目录进行预览。

支付宝小程序编译预览及打包（去掉 --watch 将不会监听文件修改，并会对代码进行压缩打包）

```bash
# yarn
$ yarn dev:alipay
$ yarn build:alipay
# npm script
$ npm run dev:alipay
$ npm run build:alipay
# 仅限全局安装
$ taro build --type alipay --watch
$ taro build --type alipay
# npx 用户也可以使用
$ npx taro build --type alipay --watch
$ npx taro build --type alipay
```

<a id="抖音小程序"></a>

### 抖音小程序

选择抖音小程序模式，需要自行下载并打开[抖音小程序开发者工具](https://developer.open-douyin.com/docs/resource/zh-CN/mini-app/develop/developer-instrument/download/developer-instrument-update-and-download)，然后在项目编译完后选择项目根目录下 `dist` 目录进行预览。

抖音小程序编译预览及打包（去掉 --watch 将不会监听文件修改，并会对代码进行压缩打包）

```bash
# yarn
$ yarn dev:tt
$ yarn build:tt
# npm script
$ npm run dev:tt
$ npm run build:tt
# 仅限全局安装
$ taro build --type tt --watch
$ taro build --type tt
# npx 用户也可以使用
$ npx taro build --type tt --watch
$ npx taro build --type tt
```

<a id="qq-小程序"></a>

### QQ 小程序

选择 QQ 小程序模式，需要自行下载并打开[QQ 小程序开发者工具](https://q.qq.com/wiki/#_4-%E7%BC%96%E7%A0%81%E5%BC%80%E5%8F%91%E5%B0%8F%E7%A8%8B%E5%BA%8F)，然后在项目编译完后选择项目根目录下 `dist` 目录进行预览。

QQ 小程序编译预览及打包（去掉 --watch 将不会监听文件修改，并会对代码进行压缩打包）

```bash
# yarn
$ yarn dev:qq
$ yarn build:qq
# npm script
$ npm run dev:qq
$ npm run build:qq
# 仅限全局安装
$ taro build --type qq --watch
$ taro build --type qq
# npx 用户也可以使用
$ npx taro build --type qq --watch
$ npx taro build --type qq
```

<a id="京东小程序"></a>

### 京东小程序

选择京东小程序模式，需要自行下载并打开京东小程序开发者工具（可邮件联系 **[mp@jd.com](mailto:mp@jd.com)** 获取内测版本），然后在项目编译完后选择项目根目录下 `dist` 目录进行预览。

京东小程序编译预览及打包（去掉 --watch 将不会监听文件修改，并会对代码进行压缩打包）

```bash
# yarn
$ yarn dev:jd
$ yarn build:jd
# npm script
$ npm run dev:jd
$ npm run build:jd
# 仅限全局安装
$ taro build --type jd --watch
$ taro build --type jd
# npx 用户也可以使用
$ npx taro build --type jd --watch
$ npx taro build --type jd
```

<a id="快应用"></a>

### 快应用

选择快应用模式，需要自行下载并打开[快应用开发者工具](https://www.quickapp.cn/docCenter/IDEPublicity)，然后在项目编译完后，在开发者工具中选择「打开文件夹」选择项目根目录下 `dist` 目录，点击左边的预览图标（那个眼睛图标）进行预览。

快应用编译预览及打包（去掉 --watch 将不会监听文件修改，并会对代码进行压缩打包）

```bash
# yarn
$ yarn dev:quickapp
$ yarn build:quickapp
# npm script
$ npm run dev:quickapp
$ npm run build:quickapp
# 仅限全局安装
$ taro build --type quickapp --watch
$ taro build --type quickapp
# npx 用户也可以使用
$ npx taro build --type quickapp --watch
$ npx taro build --type quickapp
```

[快应用开发者工具如何使用？点击了解](https://doc.quickapp.cn/tutorial/ide/overview.html)

[快应用端开发流程](../quick-app.md)

<a id="h5"></a>

### H5

H5 模式，无需特定的开发者工具，在执行完下述命令之后即可通过浏览器进行预览

H5 预览项目

```bash
# yarn
$ yarn dev:h5
# npm script
$ npm run dev:h5
# 仅限全局安装
$ taro build --type h5 --watch
# npx 用户也可以使用
$ npx taro build --type h5 --watch
```

H5 打包项目

```bash
# yarn
$ yarn build:h5
# npm script
$ npm run build:h5
# 仅限全局安装
$ taro build --type h5
# npx 用户也可以使用
$ npx taro build --type h5
```

<a id="react-native"></a>

### React Native

React Native 端运行需执行如下命令，React Native 端相关的运行说明请参见 [React Native 教程](react-native.md)

```bash
# yarn
$ yarn dev:rn
# npm script
$ npm run dev:rn
# 仅限全局安装
$ taro build --type rn --watch
# npx 用户也可以使用
$ npx taro build --type rn --watch
```

> Note：React Native 端和其他端样式兼容性差异较大，如果需要兼容 React Native 端，建议 React Native 端和其他端同步开发。

> Note：如果要支持 React Native 端，必须采用 Flex 布局，并且样式选择器仅支持类选择器，且不
> 支持 **组合器** [Combinators and groups of selectors](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Combinators_and_multiple_selectors)。

以下选择器的写法都是不支持的，在样式转换时会自动忽略。

```css
.button.button_theme_islands {
  font-style: bold;
}

img + p {
  font-style: bold;
}

p ~ span {
  color: red;
}

div > span {
  background-color: DodgerBlue;
}

div span {
  background-color: DodgerBlue;
}
```

样式上 H5 最为灵活，小程序次之，RN 最弱，统一多端样式即是对齐短板，也就是要以 RN 的约束来管理样式，同时兼顾小程序的限制，核心可以用三点来概括：

- 使用 Flex 布局
- 基于 BEM 写样式
- 采用 style 属性覆盖组件样式

RN 中 View 标签默认主轴方向是 column，如果不将其他端改成与 RN 一致，就需要在所有用到 display: flex 的地方都显式声明主轴方向。

<a id="常用-cli-命令"></a>

## 常用 CLI 命令

<a id="查看-taro-所有命令及帮助"></a>

### 查看 Taro 所有命令及帮助

```bash
$ taro --help
```

<a id="更新"></a>

### 更新

Taro 提供了更新命令来更新 CLI 工具自身和项目中 Taro 相关的依赖

更新 Taro CLI 工具

```bash
# taro
$ taro update self [version]
# npm
npm i -g @tarojs/cli@[version]
# yarn
yarn global add @tarojs/cli@[version]
```

更新项目中 Taro 相关的依赖

```bash
$ taro update project [version]
```

> `version` 为选填，如：`1.x.x/latest` 等，将会直接更新到指定版本。
> 若不填写 `version`，将会更新到当前项目 Taro 依赖的 `主版本（major）`的最新稳定版，如当前主版本没有稳定版本，则会更新到 `latest` 指定的版本。

如命令更新失败，需要在 package.json 文件手动更新依赖版本，然后重新安装依赖。

<a id="环境及依赖检测"></a>

### 环境及依赖检测

Taro 提供了命令来一键检测 Taro 环境及依赖的版本等信息，方便大家查看项目的环境及依赖，排查环境问题。在提 issue 的时候，请附上 `taro info` 打印的信息，帮助开发人员快速定位问题。

```bash
$ taro info
👽 Taro v1.2.0-beta.15


  Taro CLI 1.2.0-beta.15 environment info:
    System:
      OS: macOS High Sierra 10.13.5
      Shell: 5.3 - /bin/zsh
    Binaries:
      Node: 8.11.2 - /usr/local/bin/node
      Yarn: 1.8.0 - /usr/local/bin/yarn
      npm: 5.6.0 - /usr/local/bin/npm
    npmPackages:
      @tarojs/components: ^1.2.0-beta.3 => 1.2.0-beta.3
      @tarojs/plugin-babel: ^1.2.0-beta.3 => 1.2.0-beta.3
      @tarojs/plugin-csso: ^1.2.0-beta.3 => 1.2.0-beta.3
      @tarojs/plugin-sass: ^1.2.0-beta.4 => 1.2.0-beta.4
      @tarojs/plugin-uglifyjs: ^1.2.0-beta.3 => 1.2.0-beta.3
      @tarojs/rn-runner: ^1.2.0-beta.4 => 1.2.0-beta.4
      @tarojs/router: ^1.2.0-beta.3 => 1.2.0-beta.3
      @tarojs/taro: ^1.2.0-beta.3 => 1.2.0-beta.3
      @tarojs/taro-alipay: ^1.2.0-beta.3 => 1.2.0-beta.3
      @tarojs/taro-h5: ^1.2.0-beta.3 => 1.2.0-beta.3
      @tarojs/taro-swan: ^1.2.0-beta.3 => 1.2.0-beta.3
      @tarojs/taro-weapp: ^1.2.0-beta.3 => 1.2.0-beta.3
      @tarojs/webpack-runner: ^1.2.0-beta.3 => 1.2.0-beta.3
      eslint-config-taro: ^1.2.0-beta.3 => 1.2.0-beta.3
      eslint-plugin-taro: ^1.2.0-beta.3 => 1.2.0-beta.3
```

<a id="taro-doctor"></a>

### Taro Doctor

Taro Doctor 就像一个医生一样，可以诊断项目的依赖、设置、结构，以及代码的规范是否存在问题，并尝试给出解决方案。

但和真正的医生不一样，Taro Doctor 不需要排队挂号，也不用花钱。你只需要在终端运行命令：`taro doctor`，就像图里一样：

![Taro Doctor 诊断结果图](https://img10.360buyimg.com/ling/jfs/t1/46613/36/5573/202581/5d357d14E6f0df7e1/fc026be7dc69dcf2.png)

<a id="快速创建新页面"></a>

### 快速创建新页面

Taro create --name [页面名称] 能够在当前项目的 pages 目录下快速生成新的页面文件，并填充基础代码，是一个提高开发效率的利器。

<a id="cli-配置"></a>

### CLI 配置

> 自 `1.3.9` 开始支持

`1.3.9` 开始 Taro 会在用户根目录下创建 .taro 文件夹，其中 .taro/index.json 用于存放 CLI 相关配置。

开发者可以使用 `taro config` 命令对配置项进行一系列操作：

```bash
# 查看用法
$ taro config --help
# 设置配置项<key>的值为<value>
$ taro config set <key> <value>
# 读取配置项<key>
$ taro config get <key>
# 删除配置项<key>
$ taro config delete <key>
# 打印所有配置项
$ taro config list [--json]
```

<a id="其他常见问题"></a>

## 其他常见问题

<a id="回到某个版本"></a>

### 回到某个版本

需要安装某个固定版本，或者回到某个版本，例如我们要安装 `1.3.9` ， 则如下：

```bash
# 使用 npm 安装 CLI
$ npm install -g @tarojs/cli@1.3.9
# OR 使用 yarn 安装 CLI
$ yarn global add @tarojs/cli@1.3.9
# OR 安装了 cnpm，使用 cnpm 安装 CLI
$ cnpm install -g @tarojs/cli@1.3.9
```
