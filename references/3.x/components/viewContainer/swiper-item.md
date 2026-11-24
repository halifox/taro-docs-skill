# SwiperItem

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/viewContainer/swiper-item)

仅可放置在 swiper 组件中，宽高自动设置为100%

> 不要为 `SwiperItem` 设置 **style** 属性，可以通过 class 设置样式。[7147](https://github.com/NervJS/taro/issues/7147)

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/swiper-item.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<SwiperItemProps>
```

<a id="示例代码"></a>

## 示例代码

**React**

```tsx
class App extends Component {
  render () {
    return (
      <Swiper
        className='test-h'
        indicatorColor='#999'
        indicatorActiveColor='#333'
        vertical
        circular
        indicatorDots
        autoplay>
        <SwiperItem>
          <View className='demo-text-1'>1</View>
        </SwiperItem>
        <SwiperItem>
          <View className='demo-text-2'>2</View>
        </SwiperItem>
        <SwiperItem>
          <View className='demo-text-3'>3</View>
        </SwiperItem>
      </Swiper>
    )
  }
}
```

**Vue**

```html
<template>
  <swiper
    class='test-h'
    indicator-color='#999'
    indicator-active-color='#333'
    :vertical="true"
    :circular="true"
    :indicator-dots="true"
    :autoplay="true"
  >
    <swiper-item>
      <view class='demo-text-1'>1</view>
    </swiper-item>
    <swiper-item>
      <view class='demo-text-2'>2</view>
    </swiper-item>
    <swiper-item>
      <view class='demo-text-3'>3</view>
    </swiper-item>
  </swiper>
</template>
```

<a id="swiperitemprops"></a>

## SwiperItemProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| itemId | `string` |  | 否 | 该 swiper-item 的标识符 |
| skipHiddenItemLayout | `boolean` | `false` | 否 | 是否跳过未显示的滑块布局，设为 true 可优化复杂情况下的滑动性能，但会丢失隐藏状态滑块的布局信息 |
| deep | `boolean` | `false` | 否 | Swiper 循环状态下，前后垫片节点拷贝模式，用于修复 Vue 在 CustomElements 下的节点拷贝问题 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | 抖音小程序 | 京东小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| SwiperItemProps.itemId | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| SwiperItemProps.skipHiddenItemLayout | ✔️ |  |  |  |  |  |  |  |  |
| SwiperItemProps.deep |  |  |  |  | ✔️ |  |  |  |  |
