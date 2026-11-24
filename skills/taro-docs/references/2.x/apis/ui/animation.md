# Animation

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/ui/animation/)

<a id="方法"></a>

## 方法

<a id="export"></a>

### export

导出动画队列。**export 方法每次调用后会清掉之前的动画操作。**

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.export.html)

```tsx
() => Record<string, any>[]
```

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.export | ✔️ |  |  |

<a id="backgroundcolor"></a>

### backgroundColor

设置背景色

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.backgroundColor.html)

```tsx
(value: string) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| value | `string` | 颜色值 |

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.backgroundColor | ✔️ |  |  |

<a id="bottom"></a>

### bottom

设置 bottom 值

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.bottom.html)

```tsx
(value: string | number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| value | `string \| number` | 长度值，如果传入 number 则默认使用 px，可传入其他自定义单位的长度值 |

<a id="api-支持度-2"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.bottom | ✔️ |  |  |

<a id="height"></a>

### height

设置高度

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.height.html)

```tsx
(value: string | number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| value | `string \| number` | 长度值，如果传入 number 则默认使用 px，可传入其他自定义单位的长度值 |

<a id="api-支持度-3"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.height | ✔️ |  |  |

<a id="left"></a>

### left

设置 left 值

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.left.html)

```tsx
(value: string | number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| value | `string \| number` | 长度值，如果传入 number 则默认使用 px，可传入其他自定义单位的长度值 |

<a id="api-支持度-4"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.left | ✔️ |  |  |

<a id="matrix"></a>

### matrix

同 [transform-function matrix](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/matrix)

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.matrix.html)

```tsx
() => Animation
```

<a id="api-支持度-5"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.matrix | ✔️ |  |  |

<a id="matrix3d"></a>

### matrix3d

同 [transform-function matrix3d](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/matrix3d)

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.matrix3d.html)

```tsx
() => Animation
```

<a id="api-支持度-6"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.matrix3d | ✔️ |  |  |

<a id="opacity"></a>

### opacity

设置透明度

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.opacity.html)

```tsx
(value: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| value | `number` | 透明度，范围 0-1 |

<a id="api-支持度-7"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.opacity | ✔️ |  |  |

<a id="right"></a>

### right

设置 right 值

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.right.html)

```tsx
(value: string | number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| value | `string \| number` | 长度值，如果传入 number 则默认使用 px，可传入其他自定义单位的长度值 |

<a id="api-支持度-8"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.right | ✔️ |  |  |

<a id="rotate"></a>

### rotate

从原点顺时针旋转一个角度

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.rotate.html)

```tsx
(angle: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| angle | `number` | 旋转的角度。范围 [-180, 180] |

<a id="api-支持度-9"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.rotate | ✔️ |  |  |

<a id="rotate3d"></a>

### rotate3d

从 固定 轴顺时针旋转一个角度

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.rotate3d.html)

```tsx
(x: number, y: number, z: number, angle: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| x | `number` | 旋转轴的 x 坐标 |
| y | `number` | 旋转轴的 y 坐标 |
| z | `number` | 旋转轴的 z 坐标 |
| angle | `number` | 旋转的角度。范围 [-180, 180] |

<a id="api-支持度-10"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.rotate3d | ✔️ |  |  |

<a id="rotatex"></a>

### rotateX

从 X 轴顺时针旋转一个角度

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.rotateX.html)

```tsx
(angle: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| angle | `number` | 旋转的角度。范围 [-180, 180] |

<a id="api-支持度-11"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.rotateX | ✔️ |  |  |

<a id="rotatey"></a>

### rotateY

从 Y 轴顺时针旋转一个角度

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.rotateY.html)

```tsx
(angle: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| angle | `number` | 旋转的角度。范围 [-180, 180] |

<a id="api-支持度-12"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.rotateY | ✔️ |  |  |

<a id="rotatez"></a>

### rotateZ

从 Z 轴顺时针旋转一个角度

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.rotateZ.html)

```tsx
(angle: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| angle | `number` | 旋转的角度。范围 [-180, 180] |

<a id="api-支持度-13"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.rotateZ | ✔️ |  |  |

<a id="scale"></a>

### scale

缩放

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.scale.html)

```tsx
(sx: number, sy?: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| sx | `number` | 当仅有 sx 参数时，表示在 X 轴、Y 轴同时缩放sx倍数 |
| sy | `number` | 在 Y 轴缩放 sy 倍数 |

<a id="api-支持度-14"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.scale | ✔️ |  |  |

<a id="scale3d"></a>

### scale3d

缩放

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.scale3d.html)

```tsx
(sx: number, sy: number, sz: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| sx | `number` | x 轴的缩放倍数 |
| sy | `number` | y 轴的缩放倍数 |
| sz | `number` | z 轴的缩放倍数 |

<a id="api-支持度-15"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.scale3d | ✔️ |  |  |

<a id="scalex"></a>

### scaleX

缩放 X 轴

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.scaleX.html)

```tsx
(scale: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| scale | `number` | X 轴的缩放倍数 |

<a id="api-支持度-16"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.scaleX | ✔️ |  |  |

<a id="scaley"></a>

### scaleY

缩放 Y 轴

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.scaleY.html)

```tsx
(scale: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| scale | `number` | Y 轴的缩放倍数 |

<a id="api-支持度-17"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.scaleY | ✔️ |  |  |

<a id="scalez"></a>

### scaleZ

缩放 Z 轴

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.scaleZ.html)

```tsx
(scale: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| scale | `number` | Z 轴的缩放倍数 |

<a id="api-支持度-18"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.scaleZ | ✔️ |  |  |

<a id="skew"></a>

### skew

对 X、Y 轴坐标进行倾斜

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.skew.html)

```tsx
(ax: number, ay: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| ax | `number` | 对 X 轴坐标倾斜的角度，范围 [-180, 180] |
| ay | `number` | 对 Y 轴坐标倾斜的角度，范围 [-180, 180] |

<a id="api-支持度-19"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.skew | ✔️ |  |  |

<a id="skewx"></a>

### skewX

对 X 轴坐标进行倾斜

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.skewX.html)

```tsx
(angle: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| angle | `number` | 倾斜的角度，范围 [-180, 180] |

<a id="api-支持度-20"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.skewX | ✔️ |  |  |

<a id="skewy"></a>

### skewY

对 Y 轴坐标进行倾斜

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.skewY.html)

```tsx
(angle: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| angle | `number` | 倾斜的角度，范围 [-180, 180] |

<a id="api-支持度-21"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.skewY | ✔️ |  |  |

<a id="step"></a>

### step

表示一组动画完成。可以在一组动画中调用任意多个动画方法，一组动画中的所有动画会同时开始，一组动画完成后才会进行下一组动画。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.step.html)

```tsx
(option?: StepOption) => Animation
```

| 参数 | 类型 |
| --- | --- |
| option | `StepOption` |

<a id="api-支持度-22"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.step | ✔️ |  |  |

<a id="top"></a>

### top

设置 top 值

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.top.html)

```tsx
(value: string | number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| value | `string \| number` | 长度值，如果传入 number 则默认使用 px，可传入其他自定义单位的长度值 |

<a id="api-支持度-23"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.top | ✔️ |  |  |

<a id="translate"></a>

### translate

平移变换

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.translate.html)

```tsx
(tx?: number, ty?: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| tx | `number` | 当仅有该参数时表示在 X 轴偏移 tx，单位 px |
| ty | `number` | 在 Y 轴平移的距离，单位为 px |

<a id="api-支持度-24"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.translate | ✔️ |  |  |

<a id="translate3d"></a>

### translate3d

对 xyz 坐标进行平移变换

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.translate3d.html)

```tsx
(tx?: number, ty?: number, tz?: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| tx | `number` | 在 X 轴平移的距离，单位为 px |
| ty | `number` | 在 Y 轴平移的距离，单位为 px |
| tz | `number` | 在 Z 轴平移的距离，单位为 px |

<a id="api-支持度-25"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.translate3d | ✔️ |  |  |

<a id="translatex"></a>

### translateX

对 X 轴平移

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.translateX.html)

```tsx
(translation: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| translation | `number` | 在 X 轴平移的距离，单位为 px |

<a id="api-支持度-26"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.translateX | ✔️ |  |  |

<a id="translatey"></a>

### translateY

对 Y 轴平移

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.translateY.html)

```tsx
(translation: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| translation | `number` | 在 Y 轴平移的距离，单位为 px |

<a id="api-支持度-27"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.translateY | ✔️ |  |  |

<a id="translatez"></a>

### translateZ

对 Z 轴平移

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.translateZ.html)

```tsx
(translation: number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| translation | `number` | 在 Z 轴平移的距离，单位为 px |

<a id="api-支持度-28"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.translateZ | ✔️ |  |  |

<a id="width"></a>

### width

设置宽度

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ui/animation/Animation.width.html)

```tsx
(value: string | number) => Animation
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| value | `string \| number` | 长度值，如果传入 number 则默认使用 px，可传入其他自定义单位的长度值 |

<a id="api-支持度-29"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.width | ✔️ |  |  |

<a id="参数"></a>

## 参数

<a id="stepoption"></a>

### StepOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| delay | `number` | 否 | 动画延迟时间，单位 ms |
| duration | `number` | 否 | 动画持续时间，单位 ms |
| timingFunction | `"linear" \| "ease" \| "ease-in" \| "ease-in-out" \| "ease-out" \| "step-start" \| "step-end"` | 否 | 动画的效果 |
| transformOrigin | `string` | 否 |  |

<a id="timingfunction"></a>

### timingFunction

| 参数 | 说明 |
| --- | --- |
| linear | 动画从头到尾的速度是相同的 |
| ease | 动画以低速开始，然后加快，在结束前变慢 |
| ease-in | 动画以低速开始 |
| ease-in-out | 动画以低速开始和结束 |
| ease-out | 动画以低速结束 |
| step-start | 动画第一帧就跳至结束状态直到结束 |
| step-end | 动画一直保持开始状态，最后一帧跳到结束状态 |

<a id="api-支持度-30"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Animation.export | ✔️ |  |  |
| Animation.backgroundColor | ✔️ |  |  |
| Animation.bottom | ✔️ |  |  |
| Animation.height | ✔️ |  |  |
| Animation.left | ✔️ |  |  |
| Animation.matrix | ✔️ |  |  |
| Animation.matrix3d | ✔️ |  |  |
| Animation.opacity | ✔️ |  |  |
| Animation.right | ✔️ |  |  |
| Animation.rotate | ✔️ |  |  |
| Animation.rotate3d | ✔️ |  |  |
| Animation.rotateX | ✔️ |  |  |
| Animation.rotateY | ✔️ |  |  |
| Animation.rotateZ | ✔️ |  |  |
| Animation.scale | ✔️ |  |  |
| Animation.scale3d | ✔️ |  |  |
| Animation.scaleX | ✔️ |  |  |
| Animation.scaleY | ✔️ |  |  |
| Animation.scaleZ | ✔️ |  |  |
| Animation.skew | ✔️ |  |  |
| Animation.skewX | ✔️ |  |  |
| Animation.skewY | ✔️ |  |  |
| Animation.step | ✔️ |  |  |
| Animation.top | ✔️ |  |  |
| Animation.translate | ✔️ |  |  |
| Animation.translate3d | ✔️ |  |  |
| Animation.translateX | ✔️ |  |  |
| Animation.translateY | ✔️ |  |  |
| Animation.translateZ | ✔️ |  |  |
| Animation.width | ✔️ |  |  |
