# RootPortal

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/viewContainer/root-portal)

root-portal
使整个子树从页面中脱离出来，类似于在 CSS 中使用 fixed position 的效果。主要用于制作弹窗、弹出层等。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/root-portal.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<RootPortalProps>
```

<a id="示例代码"></a>

## 示例代码

**React**

```tsx
import { useState } from 'react'
import { RootPortal, View, Button } from '@tarojs/components'

export default function RootPortalExample {
  const [show, setShow] = useState(false)
  const toggle = () => {
    setShow(!show)
  }
  render () {
    return (
      <View>
        <Button onClick={toggle}>显示root-portal</Button>
        {
          show && (<RootPortal><View>content</View></RootPortal>)
        }
      </View>
    )
  }
}
```

<a id="rootportalprops"></a>

## RootPortalProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| enable | `boolean` | `true` | 否 | 是否从页面中脱离出来 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 支付宝小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| RootPortalProps.enable | ✔️ | ✔️ |  |  |  |  |
