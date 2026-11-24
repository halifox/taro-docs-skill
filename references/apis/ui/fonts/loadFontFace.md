# Taro.loadFontFace(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/ui/fonts/loadFontFace)

动态加载网络字体。文件地址需为下载类型。iOS 仅支持 https 格式文件地址。

注意：

1. 字体文件返回的 context-type 参考 [font](https://www.iana.org/assignments/media-types/media-types.xhtml#font)，格式不正确时会解析失败。
2. 字体链接必须是https（ios不支持http)
3. 字体链接必须是同源下的，或开启了cors支持，小程序的域名是`servicewechat.com`
4. canvas等原生组件不支持使用接口添加的字体
5. 工具里提示 Failed to load font 可以忽略

支持情况：微信小程序 支付宝小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> 支付宝小程序: source 地址格式为 `url('https://...')`，而不是单纯 URL 地址
>
> H5: 不支持 global (默认全局加载)

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/font/wx.loadFontFace.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<CallbackResult>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| global | `boolean` | `false` | 否 | 是否全局生效 |
| family | `string` |  | 是 | 定义的字体名称 |
| source | `string` |  | 是 | 字体资源的地址。建议格式为 TTF 和 WOFF，WOFF2 在低版本的 iOS 上会不兼容。 |
| desc | `DescOption` |  | 否 | 可选的字体描述符 |
| success | `(res: CallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |
| fail | `(res: CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| complete | `(res: CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="callbackresult"></a>

### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| status | `string` | 加载字体结果 |

<a id="descoption"></a>

### DescOption

可选的字体描述符

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| ascentOverride | `string` | 否 | <br>API 支持度: h5 |
| descentOverride | `string` | 否 | <br>API 支持度: h5 |
| featureSettings | `string` | 否 | <br>API 支持度: h5 |
| lineGapOverride | `string` | 否 | <br>API 支持度: h5 |
| stretch | `string` | 否 | <br>API 支持度: h5 |
| style | `string` | 否 | 字体样式，可选值为 normal / italic / oblique |
| unicodeRange | `string` | 否 | <br>API 支持度: h5 |
| variant | `string` | 否 | 设置小型大写字母的字体显示文本，可选值为 normal / small-caps / inherit |
| variationSettings | `string` | 否 | <br>API 支持度: h5 |
| weight | `string` | 否 | 字体粗细，可选值为 normal / bold / 100 / 200../ 900 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.loadFontFace({
  family: 'Bitstream Vera Serif Bold',
  source: 'url("https://sungd.github.io/Pacifico.ttf")',
  success: console.log
})
```
