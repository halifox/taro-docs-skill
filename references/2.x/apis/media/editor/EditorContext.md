# EditorContext

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/editor/EditorContext)

`EditorContext` 实例，可通过 `Taro.createSelectorQuery` 获取。
`EditorContext` 通过 `id` 跟一个 `editor` 组件绑定，操作对应的 `editor` 组件。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/editor/EditorContext.html)

<a id="方法"></a>

## 方法

<a id="blur"></a>

### blur

编辑器失焦，同时收起键盘。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/editor/EditorContext.blur.html)

```tsx
(option?: BlurOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `BlurOption` |

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| EditorContext.blur | ✔️ |  |  |

<a id="clear"></a>

### clear

清空编辑器内容

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/editor/EditorContext.clear.html)

```tsx
(option?: ClearOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `ClearOption` |

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| EditorContext.clear | ✔️ |  |  |

<a id="format"></a>

### format

修改样式

---

<a id="支持设置的样式列表"></a>

## 支持设置的样式列表

| name | value |
| --- | --- |
| bold |  |
| italic |  |
| underline |  |
| strike |  |
| ins |  |
| script | sub / super |
| header | H1 / H2 / h3 / H4 / h5 / H6 |
| align | left / center / right / justify |
| direction | rtl |
| indent | -1 / +1 |
| list | ordered / bullet / check |
| color | hex color |
| backgroundColor | hex color |
| margin/marginTop/marginBottom/marginLeft/marginRight | css style |
| padding/paddingTop/paddingBottom/paddingLeft/paddingRight | css style |
| font/fontSize/fontStyle/fontVariant/fontWeight/fontFamily | css style |
| lineHeight | css style |
| letterSpacing | css style |
| textDecoration | css style |
| textIndent | css style |

对已经应用样式的选区设置会取消样式。css style 表示 css 中规定的允许值。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/editor/EditorContext.format.html)

```tsx
(name: string, value?: string) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| name | `string` | 属性 |
| value | `string` | 值 |

<a id="api-支持度-2"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| EditorContext.format | ✔️ |  |  |

<a id="getcontents"></a>

### getContents

获取编辑器内容

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/editor/EditorContext.getContents.html)

```tsx
(option?: GetContentsOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `GetContentsOption` |

<a id="api-支持度-3"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| EditorContext.getContents | ✔️ |  |  |

<a id="insertdivider"></a>

### insertDivider

插入分割线

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/editor/EditorContext.insertDivider.html)

```tsx
(option?: InsertDividerOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `InsertDividerOption` |

<a id="api-支持度-4"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| EditorContext.insertDivider | ✔️ |  |  |

<a id="insertimage"></a>

### insertImage

插入图片。

地址为临时文件时，获取的编辑器html格式内容中 `<img>` 标签增加属性 data-local，delta 格式内容中图片 attributes 属性增加 data-local 字段，该值为传入的临时文件地址。

开发者可选择在提交阶段上传图片到服务器，获取到网络地址后进行替换。替换时对于html内容应替换掉 `<img>` 的 src 值，对于 delta 内容应替换掉 `insert { image: abc }` 值。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/editor/EditorContext.insertImage.html)

```tsx
(option: InsertImageOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `InsertImageOption` |

<a id="示例代码"></a>

#### 示例代码

```tsx
this.editorCtx.insertImage({
  src: 'xx',
  width: '100px',
  height: '50px',
  extClass: className
})
```

<a id="api-支持度-5"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| EditorContext.insertImage | ✔️ |  |  |

<a id="inserttext"></a>

### insertText

覆盖当前选区，设置一段文本

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/editor/EditorContext.insertText.html)

```tsx
(option: InsertTextOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `InsertTextOption` |

<a id="api-支持度-6"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| EditorContext.insertText | ✔️ |  |  |

<a id="redo"></a>

### redo

恢复

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/editor/EditorContext.redo.html)

```tsx
(option?: RedoOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `RedoOption` |

<a id="api-支持度-7"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| EditorContext.redo | ✔️ |  |  |

<a id="removeformat"></a>

### removeFormat

清除当前选区的样式

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/editor/EditorContext.removeFormat.html)

```tsx
(option?: RemoveFormatOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `RemoveFormatOption` |

<a id="api-支持度-8"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| EditorContext.removeFormat | ✔️ |  |  |

<a id="scrollintoview"></a>

### scrollIntoView

使得编辑器光标处滚动到窗口可视区域内。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/editor/EditorContext.scrollIntoView.html)

```tsx
() => void
```

<a id="api-支持度-9"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| EditorContext.scrollIntoView | ✔️ |  |  |

<a id="setcontents"></a>

### setContents

初始化编辑器内容，html和delta同时存在时仅delta生效

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/editor/EditorContext.setContents.html)

```tsx
(option: SetContentsOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `SetContentsOption` |

<a id="api-支持度-10"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| EditorContext.setContents | ✔️ |  |  |

<a id="undo"></a>

### undo

撤销

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/editor/EditorContext.undo.html)

```tsx
(option?: UndoOption) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `UndoOption` |

<a id="api-支持度-11"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| EditorContext.undo | ✔️ |  |  |

<a id="参数"></a>

## 参数

<a id="bluroption"></a>

### BlurOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="clearoption"></a>

### ClearOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="getcontentsoption"></a>

### GetContentsOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="insertdivideroption"></a>

### InsertDividerOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="insertimageoption"></a>

### InsertImageOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| src | `string` | 是 | 图片地址，仅支持 http(s)、base64、云图片(2.8.0)、临时文件(2.8.3)。 |
| alt | `string` | 否 | 图像无法显示时的替代文本 |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| data | `Record<string, any>` | 否 | data 被序列化为 name=value;name1=value2 的格式挂在属性 data-custom 上 |
| extClass | `string` | 否 | 添加到图片 img 标签上的类名 |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| height | `string` | 否 | 图片高度 (pixels/百分比) |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |
| width | `string` | 否 | 图片宽度（pixels/百分比) |

<a id="inserttextoption"></a>

### InsertTextOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |
| text | `string` | 否 | 文本内容 |

<a id="redooption"></a>

### RedoOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="removeformatoption"></a>

### RemoveFormatOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="setcontentsoption"></a>

### SetContentsOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| delta | `Record<string, any>` | 否 | 表示内容的delta对象 |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| html | `string` | 否 | 带标签的HTML内容 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="undooption"></a>

### UndoOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="api-支持度-12"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| EditorContext.blur | ✔️ |  |  |
| EditorContext.clear | ✔️ |  |  |
| EditorContext.format | ✔️ |  |  |
| EditorContext.getContents | ✔️ |  |  |
| EditorContext.insertDivider | ✔️ |  |  |
| EditorContext.insertImage | ✔️ |  |  |
| EditorContext.insertText | ✔️ |  |  |
| EditorContext.redo | ✔️ |  |  |
| EditorContext.removeFormat | ✔️ |  |  |
| EditorContext.scrollIntoView | ✔️ |  |  |
| EditorContext.setContents | ✔️ |  |  |
| EditorContext.undo | ✔️ |  |  |
