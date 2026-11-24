# 微信小程序独立分包

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/independent-subpackage)

Taro 支持使用微信小程序的独立分包功能，配置方法和微信小程序中一致，请参考[《微信小程序独立分包文档》](https://developers.weixin.qq.com/miniprogram/dev/framework/subpackages/independent.html)。

<a id="示例"></a>

## 示例

- [weapp-independent-subpackages](https://github.com/NervJS/taro/tree/next/examples/weapp-independent-subpackages)

<a id="配置方法"></a>

## 配置方法

假设小程序目录结构如下：

```text
├── config
├── src
|   ├── pages
|   |   └── index
|   ├── moduleA
|   |   └── pages
|   |       ├── rabbit
|   |       └── squirrel
|   ├── moduleB
|   |   └── pages
|   |       ├── pear
|   |       └── pineapple
|   ├── app.css
|   ├── app.json
|   └── app.js
└── package.json
```

开发者通过在 `app.json` 的 `subpackages` 字段中，给对应的分包配置项中定义的 `independent` 字段声明对应分包为独立分包：

app.json

```js
{
  "pages": [
    "pages/index"
  ],
  "subpackages": [
    {
      "root": "moduleA",
      "pages": [
        "pages/rabbit",
        "pages/squirrel"
      ]
    }, {
      "root": "moduleB",
      "pages": [
        "pages/pear",
        "pages/pineapple"
      ],
      "independent": true
    }
  ]
}
```
