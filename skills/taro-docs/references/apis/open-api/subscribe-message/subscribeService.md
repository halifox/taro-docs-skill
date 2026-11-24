# Taro.subscribeService(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/open-api/subscribe-message/subscribeService)

小程序消息订阅服务，包括取消订阅和查询订阅；订阅操作详见 [form 表单](https://smartprogram.baidu.com/docs/develop/component/formlist_form/)。

支持情况：微信小程序 百度小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://smartprogram.baidu.com/docs/develop/api/open/swan-subscribeService/)

<a id="类型"></a>

## 类型

```tsx
(option: subscribeService.Option) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `subscribeService.Option` |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.subscribeService({
  templateId: 'BD0003',
  subscribeId: '8026',
  type: 'query',
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
