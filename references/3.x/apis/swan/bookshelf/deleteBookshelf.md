# Taro.deleteBookshelf(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/swan/bookshelf/deleteBookshelf)

删除书架中的内容（需宿主支持书架入口)

支持情况：微信小程序 百度小程序 H5 React Native Harmony

> [参考文档](https://smartprogram.baidu.com/docs/develop/api/open/swan-deleteBookshelf/)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| category | `string` | 是 | 要删除的内容分类 |
| contentIds | `string[]` | 是 | 要删除书架内容的 id，支持传多个，最多 100 条；注释：contentId 为内容 id，内容的唯一标识，自定义，最长 22 字符（不能含有空格、中文字符）。支持批量删除的同一个 category 下的多个 id，不同 category 下的 id 请分别调用该接口删除 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="category"></a>

### Category

| 参数 | 说明 |
| --- | --- |
| article | 专栏模板 |
| doc | 文档模板 |
| cartoon | 动漫模板 |
| av | 影音模板 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| list | `IListItem[]` | 添加到书架的结果列表 |

<a id="ilistitem"></a>

### IListItem

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| contentId | `string` | 内容的唯一标识 |
| status | `keyof Status` | 删除状态：值为 0 时是失败，为 1 时是成功 |
| msg | `string` | 删除信息 |

<a id="status"></a>

### Status

| 参数 | 说明 |
| --- | --- |
| 0 | 失败 |
| 1 | 成功 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.deleteBookshelf({
  category: 'doc',
  contentIds: ['test1', 'test2'],
  success(res) {
    Taro.showModal({
      title: 'success',
      content: JSON.stringify(res)
    })
  },
  fail(err) {
    Taro.showModal({
      title: 'fail',
      content: JSON.stringify(err)
    })
  }
})
```
