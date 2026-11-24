# Taro.createAnimation(OBJECT)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/interface/animation/createAnimation)

使用方式同 [`wx.createAnimation`](https://developers.weixin.qq.com/miniprogram/dev/api/wx.createAnimation.html)。

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

const animation = Taro.createAnimation({
  transformOrigin: "50% 50%",
  duration: 1000,
  timingFunction: "ease",
  delay: 0
})
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.createAnimation | ✔️ | ✔️ |  |
