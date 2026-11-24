# Taro.getCurrentPages()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/framework/getCurrentPages)

获取当前页面栈。数组中第一个元素为首页，最后一个元素为当前页面。
**注意：**

- **不要尝试修改页面栈，会导致路由以及页面状态错误。**
- 不要在 `App.onLaunch` 的时候调用 `getCurrentPages()`，此时 `page` 还没有生成。

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/reference/api/getCurrentPages.html)

<a id="类型"></a>

## 类型

```tsx
() => Page[]
```

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getCurrentPages().length
```
