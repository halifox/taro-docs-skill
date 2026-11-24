# AnimationVideo

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/media/animation-video)

透明视频动画

支持情况：微信小程序 百度小程序 H5 React Native Harmony

> [参考文档](https://smartprogram.baidu.com/docs/develop/component/animation-video/)

<a id="类型"></a>

## 类型

```tsx
ComponentType<AnimationVideoProps>
```

<a id="animationvideoprops"></a>

## AnimationVideoProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| resourceWidth | `number` | `800` | 否 | 组件使用的 video 视频资源的宽度（单位：px） |
| resourceHeight | `number` | `400` | 否 | 组件使用的 video 视频资源的高度（单位：px） |
| canvasStyle | `string` | `"width: 400px;height: 400px"` | 否 | 用于设置动画画布的 CSS 样式 |
| path | `string` |  | 否 | 动画资源地址，支持相对路径以及远程地址。如果是远程路径，注意 response header 里需要设置 Access-Control-Allow-Origin 来防止跨域问题 |
| loop | `boolean` | `false` | 否 | 动画是否循环播放 |
| autoplay | `boolean` | `false` | 否 | 动画是否自动播放 |
| alphaDirection | `string` | `"left"` | 否 | 视频资源中 alpha 通道的方向，left 表示 alpha 通道在资源的左边，right 表示 alpha 通道在资源的右边。详情请参考透明视频设计资源示例 |
| onStarted | `CommonEventFunction` |  | 否 | 动画开始播放的回调 |
| onEnded | `CommonEventFunction` |  | 否 | 当播放到末尾时触发 ended 事件（自然播放结束会触发回调，循环播放结束及暂停动画不会触发） |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- | --- |
| AnimationVideoProps.resourceWidth |  | ✔️ |  |  |  |
| AnimationVideoProps.resourceHeight |  | ✔️ |  |  |  |
| AnimationVideoProps.canvasStyle |  | ✔️ |  |  |  |
| AnimationVideoProps.path |  | ✔️ |  |  |  |
| AnimationVideoProps.loop |  | ✔️ |  |  |  |
| AnimationVideoProps.autoplay |  | ✔️ |  |  |  |
| AnimationVideoProps.alphaDirection |  | ✔️ |  |  |  |
| AnimationVideoProps.onStarted |  | ✔️ |  |  |  |
| AnimationVideoProps.onEnded |  | ✔️ |  |  |  |
