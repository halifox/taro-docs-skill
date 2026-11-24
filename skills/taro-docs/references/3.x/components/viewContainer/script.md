# Script

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/viewContainer/script)

script 类似微信小程序的 wxs 标签，支持引用各种小程序的 xs 文件
只能在 CompileMode 中使用

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony

<a id="类型"></a>

## 类型

```tsx
ComponentType<ScriptProps>
```

<a id="示例代码"></a>

## 示例代码

**React**

```tsx
import { Component } from 'react'
import { View, Script } from '@tarojs/components'

export function Index () {
  return (
    <View compileMode>
      <Script src="./logic.wxs" module="logic"></Script>
      <Text>Hello, {logic.name}!</Text>
    </View>
  )
}
```

<a id="scriptprops"></a>

## ScriptProps

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| src | `string` | xs 文件的相对路径 |
| module | `string` | xs 模块名 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | 京东小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ScriptProps.src | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  |  |  | ✔️ |
| ScriptProps.module | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  |  |  | ✔️ |
