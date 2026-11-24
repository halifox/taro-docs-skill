# Taro.createAnimation(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/ui/animation/createAnimation)

创建一个动画实例 [animation](../animation.md)。调用实例的方法来描述动画。最后通过动画实例的 export 方法导出动画数据传递给组件的 animation 属性。

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/wx.createAnimation.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Animation
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| duration | `number` |  | 否 | 动画持续时间，单位 ms |
| timingFunction | `keyof TimingFunction` |  | 否 | 动画的效果 |
| delay | `number` | `0` | 否 | 动画延迟时间，单位 ms |
| transformOrigin | `string` | `"50% 50% 0"` | 否 |  |
| unit | `string` |  | 否 | 单位<br>API 支持度: h5 |

<a id="timingfunction"></a>

### TimingFunction

| 参数 | 说明 |
| --- | --- |
| linear | 动画从头到尾的速度是相同的 |
| ease | 动画以低速开始，然后加快，在结束前变慢 |
| ease-in | 动画以低速开始 |
| ease-in-out | 动画以低速开始和结束 |
| ease-out | 动画以低速结束 |
| step-start | 动画第一帧就跳至结束状态直到结束 |
| step-end | 动画一直保持开始状态，最后一帧跳到结束状态 |

<a id="示例代码"></a>

## 示例代码

```tsx
var animation = Taro.createAnimation({
  transformOrigin: "50% 50%",
  duration: 1000,
  timingFunction: "ease",
  delay: 0
})
```
