# InnerAudioContext

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/audio/InnerAudioContext)

InnerAudioContext 实例，可通过 Taro.createInnerAudioContext 接口获取实例。

**支持格式**

| 格式 | iOS | Android |
| --- | --- | --- |
| flac | x | √ |
| m4a | √ | √ |
| ogg | x | √ |
| ape | x | √ |
| amr | x | √ |
| wma | x | √ |
| wav | √ | √ |
| mp3 | √ | √ |
| mp4 | x | √ |
| aac | √ | √ |
| aiff | √ | x |
| caf | √ | x |

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/InnerAudioContext.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 默认值 | 只读 | 说明 |
| --- | --- | --- | --- | --- |
| autoplay | `boolean` | `false` | 否 | 是否自动开始播放 |
| buffered | `number` |  | 是 | 音频缓冲的时间点，仅保证当前播放时间点到此时间点内容已缓冲 |
| currentTime | `number` |  | 是 | 当前音频的播放位置（单位 s）。只有在当前有合法的 src 时返回，时间保留小数点后 6 位 |
| duration | `number` |  | 是 | 当前音频的长度（单位 s）。只有在当前有合法的 src 时返回 |
| loop | `boolean` | `false` | 否 | 是否循环播放 |
| obeyMuteSwitch | `boolean` | `true` | 否 | 是否遵循系统静音开关。当此参数为 `false` 时，即使用户打开了静音开关，也能继续发出声音。从 2.3.0 版本开始此参数不生效，使用 [Taro.setInnerAudioOption](https://developers.weixin.qq.com/miniprogram/dev/api/media/audio/wx.setInnerAudioOption.html) 接口统一设置。 |
| paused | `boolean` |  | 是 | 当前是是否暂停或停止状态 |
| src | `string` |  | 否 | 音频资源的地址，用于直接播放。 |
| startTime | `number` | `0` | 否 | 开始播放的位置（单位：s） |
| volume | `number` | `1` | 否 | 音量。范围 0~1。 |

<a id="play"></a>

### play

播放

```tsx
() => void
```

<a id="pause"></a>

### pause

暂停

```tsx
() => void
```

<a id="stop"></a>

### stop

停止

```tsx
() => void
```

<a id="seek"></a>

### seek

跳转到指定位置，单位 s

```tsx
(position: number) => void
```

| 参数 | 类型 |
| --- | --- |
| position | `number` |

<a id="destroy"></a>

### destroy

销毁当前实例

```tsx
() => void
```

<a id="oncanplay"></a>

### onCanplay

音频进入可以播放状态，但不保证后面可以流畅播放

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="onplay"></a>

### onPlay

音频播放事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="onpause"></a>

### onPause

音频暂停事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="onstop"></a>

### onStop

音频停止事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="onended"></a>

### onEnded

音频自然播放结束事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="ontimeupdate"></a>

### onTimeUpdate

音频播放进度更新事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="onerror"></a>

### onError

音频播放错误事件

```tsx
(callback?: (res: onErrorDetail) => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `(res: onErrorDetail) => void` |

<a id="onwaiting"></a>

### onWaiting

音频加载中事件，当音频因为数据不足，需要停下来加载时会触发

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="onseeking"></a>

### onSeeking

音频进行 seek 操作事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="onseeked"></a>

### onSeeked

音频完成 seek 操作事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="offcanplay"></a>

### offCanplay

取消监听 onCanplay 事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="offplay"></a>

### offPlay

取消监听 onPlay 事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="offpause"></a>

### offPause

取消监听 onPause 事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="offstop"></a>

### offStop

取消监听 onStop 事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="offended"></a>

### offEnded

取消监听 onEnded 事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="offtimeupdate"></a>

### offTimeUpdate

取消监听 onTimeUpdate 事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="offerror"></a>

### offError

取消监听 onError 事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="offwaiting"></a>

### offWaiting

取消监听 onWaiting 事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="offseeking"></a>

### offSeeking

取消监听 onSeeking 事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="offseeked"></a>

### offSeeked

取消监听 onSeeked 事件

```tsx
(callback?: () => void) => void
```

| 参数 | 类型 |
| --- | --- |
| callback | `() => void` |

<a id="参数"></a>

## 参数

<a id="onerrordetail"></a>

### onErrorDetail

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errCode | `number` | 错误码 |
| errMsg | `string` | 错误信息 |

<a id="onerrordetailerrcode"></a>

### onErrorDetailErrCode

| 参数 | 说明 |
| --- | --- |
| 10001 | 系统错误 |
| 10002 | 网络错误 |
| 10003 | 文件错误 |
| 10004 | 格式错误 |
| -1 | 未知错误 |

<a id="示例代码"></a>

## 示例代码

```tsx
const innerAudioContext = Taro.createInnerAudioContext()
innerAudioContext.autoplay = true
innerAudioContext.src = 'https://ws.stream.qqmusic.qq.com/M500001VfvsJ21xFqb.mp3?guid=ffffffff82def4af4b12b3cd9337d5e7&uin=346897220&vkey=6292F51E1E384E061FF02C31F716658E5C81F5594D561F2E88B854E81CAAB7806D5E4F103E55D33C16F3FAC506D1AB172DE8600B37E43FAD&fromtag=46'
innerAudioContext.onPlay(() => {
  console.log('开始播放')
})
innerAudioContext.onError((res) => {
  console.log(res.errMsg)
  console.log(res.errCode)
})
```
