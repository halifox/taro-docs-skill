# CoverView

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/components/viewContainer/cover-view)

覆盖在原生组件之上的文本视图。可覆盖的原生组件包括 map、video、canvas、camera、live-player、live-pusher 只支持嵌套 cover-view、cover-image，可在 cover-view 中使用 button。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/cover-view.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<CoverViewProps>
```

<a id="示例代码"></a>

## 示例代码

```tsx
class App extends Components {
  render () {
    return (
      <Video id='myVideo' src='src'>
        <CoverView class='controls'>
          <CoverView class='play' onClick='play'>
            <CoverImage class='img' src='src' />
          </CoverView>
        </CoverView>
      </Video>
    )
  }
}
```

<a id="coverviewprops"></a>

## CoverViewProps

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| scrollTop | `number` | 否 | 设置顶部滚动偏移量，仅在设置了 overflow-y: scroll 成为滚动元素后生效 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| CoverViewProps.scrollTop | ✔️ |  |  |

<a id="api-支持度-1"></a>

## API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | H5 | React Native |
| --- | --- | --- | --- | --- | --- |
| CoverView | ✔️ | ✔️ | ✔️ |  |  |
