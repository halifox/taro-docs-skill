# Taro.createInnerAudioContext()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/multimedia/audio/createInnerAudioContext)

创建内部 audio 上下文 InnerAudioContext 对象。

使用方式同 [`wx.createInnerAudioContext`](https://developers.weixin.qq.com/miniprogram/dev/api/wx.createInnerAudioContext.html)。

<a id="返回值"></a>

## 返回值

<a id="object-inneraudiocontext"></a>

### object InnerAudioContext

| Property | Type | Default | Description |
| --- | --- | --- | --- |
| src | `string` |  | 音频资源的地址，用于直接播放。 |
| [startTime] | `number` | `0` | 开始播放的位置（单位：s），默认为 0 |
| [autoplay] | `boolean` | `false` | 是否自动开始播放，默认为 false |
| [loop] | `boolean` | `false` | 是否循环播放，默认为 false |
| [obeyMuteSwitch] | `boolean` | `true` | 是否遵循系统静音开关，默认为 true。当此参数为 false 时，即使用户打开了静音开关，也能继续发出声音。 |
| [volume] | `number` | `1` | 音量。范围 0~1。默认为 1 |
| duration | `number` |  | 当前音频的长度（单位 s）。只有在当前有合法的 src 时返回（只读） |
| currentTime | `number` |  | 当前音频的播放位置（单位 s）。只有在当前有合法的 src 时返回，时间保留小数点后 6 位（只读） |
| paused | `boolean` |  | 当前是是否暂停或停止状态（只读） |
| buffered | `number` |  | 音频缓冲的时间点，仅保证当前播放时间点到此时间点内容已缓冲（只读） |
| play | `function` |  | 播放 |
| pause | `function` |  | 暂停。暂停后的音频再播放会从暂停处开始播放 |
| stop | `function` |  | 停止。停止后的音频再播放会从头开始播放。 |
| seek | `function` |  | 跳转到指定位置 |
| destroy | `function` |  | 销毁当前实例 |
| offCanplay | `function` |  | 取消监听音频进入可以播放状态的事件 |
| offEnded | `function` |  | 取消监听音频自然播放至结束的事件 |
| offError | `function` |  | 取消监听音频播放错误事件 |
| offPause | `function` |  | 取消监听音频暂停事件 |
| offPlay | `function` |  | 取消监听音频播放事件 |
| offSeeked | `function` |  | 取消监听音频完成跳转操作的事件 |
| offSeeking | `function` |  | 取消监听音频进行跳转操作的事件 |
| offStop | `function` |  | 取消监听音频停止事件 |
| offTimeUpdate | `function` |  | 取消监听音频播放进度更新事件 |
| offWaiting | `function` |  | 取消监听音频加载中事件 |
| onCanplay | `function` |  | 监听音频进入可以播放状态的事件。但不保证后面可以流畅播放 |
| onEnded | `function` |  | 监听音频自然播放至结束的事件 |
| onError | `function` |  | 监听音频播放错误事件 |
| onPause | `function` |  | 监听音频暂停事件 |
| onPlay | `function` |  | 监听音频播放事件 |
| onSeeked | `function` |  | 监听音频完成跳转操作的事件 |
| onSeeking | `function` |  | 监听音频进行跳转操作的事件 |
| onStop | `function` |  | 监听音频停止事件 |
| onTimeUpdate | `function` |  | 监听音频播放进度更新事件 |
| onWaiting | `function` |  | 监听音频加载中事件。当音频因为数据不足，需要停下来加载时会触发 |

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

const innerAudioContext = Taro.createInnerAudioContext()
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native | 支付宝小程序 | 百度小程序 |
| --- | --- | --- | --- | --- | --- |
| Taro.createInnerAudioContext | ✔️ | ✔️ |  |  |  |
