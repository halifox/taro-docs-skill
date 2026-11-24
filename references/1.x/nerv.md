# Nerv

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/nerv)

[Nerv](https://github.com/NervJS/nerv) 是凹凸实验室研发的高性能类 React 框架。在 Taro 中使用 Nerv 基本遵循和[在 Taro 中使用 React](react.md) 一样的用法（只不过相比起 `import * as React from 'React'`，你需要 `import Nerv from 'nervjs'`）。相比起 React，Nerv 能提高[更高的性能](https://stefankrause.net/js-frameworks-benchmark8/table.html)和更小的体积，这在小程序开发中非常关键。

<a id="使用第三方-react-库"></a>

## 使用第三方 React 库

在使用第三方 React 库时，需要在[配置文件](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/config-detail#miniwebpackchain) `webpack.resolve.alias`，把 `react` 和 `react-dom` 映射到 `nervjs`:

```js
{
  webpackChain (chain, webpack) {
    chain.merge({
      resolve: {
        alias: {
          react: 'nervjs',
          'react-dom': 'nervjs'
        }
      }
    })
  }
}
```
