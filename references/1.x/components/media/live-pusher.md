# LivePusher

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/components/media/live-pusher)

<a id="实时音视频录制"></a>

## 实时音视频录制

> 组件 支持度

| 微信小程序 | H5 | ReactNative |
| --- | --- | --- |
| ✔️ | x | x |

小程序全部支持，属性参考[live-pusher](https://developers.weixin.qq.com/miniprogram/dev/component/live-pusher.html)。属性值请改写为驼峰式命名。

```jsx
import Taro, { Component } from '@tarojs/taro'
// 引入 LivePusher 组件
import { LivePusher } from '@tarojs/components'

class App extends Components {
  render () {
    return (
      <LivePusher url='url' mode='RTC' autopush  />
    )
  }
}
```
