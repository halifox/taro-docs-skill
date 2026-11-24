# MovableArea

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/viewContainer/movable-area)

movable-view 的可移动区域

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/movable-area.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<MovableAreaProps>
```

<a id="示例代码"></a>

## 示例代码

**React**

```tsx
class App extends Components {
  render () {
    return (
      <MovableArea style='height: 200px; width: 200px; background: red;'>
        <MovableView style='height: 50px; width: 50px; background: blue;' direction='all'>旅行的意义</MovableView>
      </MovableArea>
    )
  }
}
```

**Vue**

```html
  <movable-area style='height: 200px; width: 200px; background: red;'>
    <movable-view style='height: 50px; width: 50px; background: blue;' direction='all'>在路上</movable-view>
  </movable-area>
```

<a id="movableareaprops"></a>

## MovableAreaProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| scaleArea | `boolean` | `false` | 否 | 当里面的 movable-view 设置为支持双指缩放时，设置此值可将缩放手势生效区域修改为整个 movable-area |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | 京东小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| MovableAreaProps.scaleArea | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  |  | ✔️ | ✔️ |
