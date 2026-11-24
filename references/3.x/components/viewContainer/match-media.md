# MatchMedia

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/viewContainer/match-media)

media query 匹配检测节点。可以指定一组 media query 规则，满足时，这个节点才会被展示。
通过这个节点可以实现“页面宽高在某个范围时才展示某个区域”这样的效果。

支持情况：微信小程序 支付宝小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/match-media.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<MatchMediaProps>
```

<a id="示例代码"></a>

## 示例代码

**React**

```tsx
class App extends Components {
  render () {
    return (
      <View>
        <MatchMedia minWidth="300" maxWidth="600">
          <view>当页面宽度在 300 ~ 500 px 之间时展示这里</view>
        </MatchMedia>
        <MatchMedia minHeight="400" orientation="landscape">
          <view>当页面高度不小于 400 px 且屏幕方向为纵向时展示这里</view>
        </MatchMedia>
      </View>
    )
  }
}
```

**Vue**

```html
<template>
  <view class="components-page">
    <match-media min-width="300" max-width="500">
      <view>当页面宽度在 300 ~ 500 px 之间时展示这里</view>
    </match-media>
    <match-media min-height="400" orientation="landscape">
      <view>当页面高度不小于 400 px 且屏幕方向为纵向时展示这里</view>
    </match-media>
  </view>
</template>
```

<a id="matchmediaprops"></a>

## MatchMediaProps

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| minWidth | `number` | 否 | 页面最小宽度（ px 为单位） |
| maxWidth | `number` | 否 | 页面最大宽度（ px 为单位） |
| width | `number` | 否 | 页面宽度（ px 为单位） |
| minHeight | `number` | 否 | 页面最小高度（ px 为单位） |
| maxHeight | `number` | 否 | 页面最大高度（ px 为单位） |
| height | `number` | 否 | 页面高度（ px 为单位） |
| orientation | `string` | 否 | 屏幕方向（ landscape 或 portrait ） |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 支付宝小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| MatchMediaProps.minWidth | ✔️ | ✔️ |  |  |  |  |
| MatchMediaProps.maxWidth | ✔️ | ✔️ |  |  |  |  |
| MatchMediaProps.width | ✔️ | ✔️ |  |  |  |  |
| MatchMediaProps.minHeight | ✔️ | ✔️ |  |  |  |  |
| MatchMediaProps.maxHeight | ✔️ | ✔️ |  |  |  |  |
| MatchMediaProps.height | ✔️ | ✔️ |  |  |  |  |
| MatchMediaProps.orientation | ✔️ | ✔️ |  |  |  |  |
