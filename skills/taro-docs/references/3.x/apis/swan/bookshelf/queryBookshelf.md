# Taro.queryBookshelf(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/swan/bookshelf/queryBookshelf)

查询宿主书架的相关内容

支持情况：微信小程序 百度小程序 QQ 小程序 H5 React Native Harmony

> 百度小程序: （需宿主支持书架入口）

> [参考文档](https://smartprogram.baidu.com/docs/develop/api/open/swan-queryBookshelf/)

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
| contentIds | `string[]` | 是 | 要查询内容的 id，支持传多个，最多 100 条；注释：contentId 为内容 id，内容的唯一标识，自定义，最长 22 字符（不能含有空格、中文字符） |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| list | `IListItem[]` | 查询的内容结果列表 |

<a id="ilistitem"></a>

### IListItem

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| contentId | `string` | 内容的唯一标识 |
| status | `keyof Status` | 状态 |

<a id="status"></a>

### Status

| 参数 | 说明 |
| --- | --- |
| 0 | 不存在 |
| 1 | 存在 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.queryBookshelf({
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
