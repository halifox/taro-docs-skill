# TapGestureHandler

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/gesture/tap-gesture-handler)

点击时触发手势
微信小程序下 skyline 的手势标签，只能在 CompileMode 中使用

支持情况：微信小程序 H5 React Native Harmony

<a id="类型"></a>

## 类型

```tsx
ComponentType<TapGestureHandlerProps>
```

<a id="示例代码"></a>

## 示例代码

**React**

```tsx
import { Component } from 'react'
import { View, TapGestureHandler } from '@tarojs/components'

export function Index () {
  return (
    <View compileMode>
      <TapGestureHandler onGestureWorklet="onGesture">
         <View className='circle'></View>
      </TapGestureHandler>
    </View>
  )
}
```

<a id="tapgesturehandlerprops"></a>

## TapGestureHandlerProps

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| tag | `string` | 否 | 声明手势协商时的组件标识 |
| onGestureWorklet | `string` | 否 | 手势识别成功的回调 |
| shouldResponseOnMoveWorklet | `string` | 否 | 手指移动过程中手势是否响应 |
| shouldAcceptGestureWorklet | `string` | 否 | 手势是否应该被识别 |
| simultaneousHandlers | `string[]` | 否 | 声明可同时触发的手势节点 |
| nativeView | `string` | 否 | 代理的原生节点类型 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- |
| TapGestureHandlerProps.tag | ✔️ |  |  |  |
| TapGestureHandlerProps.onGestureWorklet | ✔️ |  |  |  |
| TapGestureHandlerProps.shouldResponseOnMoveWorklet | ✔️ |  |  |  |
| TapGestureHandlerProps.shouldAcceptGestureWorklet | ✔️ |  |  |  |
| TapGestureHandlerProps.simultaneousHandlers | ✔️ |  |  |  |
| TapGestureHandlerProps.nativeView | ✔️ |  |  |  |
