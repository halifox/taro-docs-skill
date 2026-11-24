# AudioContext

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/audio/AudioContext)

`AudioContext` 实例，可通过 `Taro.createAudioContext` 获取。
`AudioContext` 通过 `id` 跟一个 `audio` 组件绑定，操作对应的 audio 组件。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/AudioContext.html)

<a id="方法"></a>

## 方法

<a id="pause"></a>

### pause

暂停音频。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/AudioContext.pause.html)

```tsx
() => void
```

<a id="api-支持度"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| AudioContext.pause | ✔️ |  |  |

<a id="play"></a>

### play

播放音频。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/AudioContext.play.html)

```tsx
() => void
```

<a id="api-支持度-1"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| AudioContext.play | ✔️ |  |  |

<a id="seek"></a>

### seek

跳转到指定位置。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/AudioContext.seek.html)

```tsx
(position: number) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| position | `number` | 跳转位置，单位 s |

<a id="api-支持度-2"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| AudioContext.seek | ✔️ |  |  |

<a id="setsrc"></a>

### setSrc

设置音频地址

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/AudioContext.setSrc.html)

```tsx
(src: string) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| src | `string` | 音频地址 |

<a id="api-支持度-3"></a>

#### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| AudioContext.setSrc | ✔️ |  |  |

<a id="api-支持度-4"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| AudioContext.pause | ✔️ |  |  |
| AudioContext.play | ✔️ |  |  |
| AudioContext.seek | ✔️ |  |  |
| AudioContext.setSrc | ✔️ |  |  |
