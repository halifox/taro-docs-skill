# VideoDecoder

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/media/video-decoder/VideoDecoder)

<a id="方法"></a>

## 方法

<a id="getframedata"></a>

### getFrameData

获取下一帧的解码数据

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/VideoDecoder.getFrameData.html)

```tsx
() => Promise<Result>
```

<a id="off"></a>

### off

取消监听录制事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/VideoDecoder.off.html)

```tsx
(eventName: keyof EventName, callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| eventName | `keyof EventName` | 事件名 |
| callback | `Callback` | 事件触发时执行的回调函数 |

<a id="on"></a>

### on

注册监听录制事件的回调函数

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/VideoDecoder.on.html)

```tsx
(eventName: keyof EventName, callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| eventName | `keyof EventName` | 事件名 |
| callback | `Callback` | 事件触发时执行的回调函数 |

<a id="remove"></a>

### remove

移除解码器

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/VideoDecoder.remove.html)

```tsx
() => Promise<void>
```

<a id="seek"></a>

### seek

跳到某个时间点解码

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/VideoDecoder.seek.html)

```tsx
(position: number) => Promise<void>
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| position | `number` | 跳转的解码位置，单位 ms |

<a id="start"></a>

### start

开始解码

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/VideoDecoder.start.html)

```tsx
(option: Option) => Promise<void>
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="stop"></a>

### stop

停止解码

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/VideoDecoder.stop.html)

```tsx
() => Promise<void>
```

<a id="参数"></a>

## 参数

<a id="getframedata-1"></a>

### getFrameData

<a id="result"></a>

#### Result

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| width | `number` | 帧数据宽度 |
| height | `number` | 帧数据高度 |
| data | `ArrayBuffer` | 帧数据 |
| pkPts | `number` | 帧原始 pts |
| pkDts | `number` | 帧原始 dts |

<a id="on-1"></a>

### on

<a id="eventname"></a>

#### EventName

eventName 的合法值

| 参数 | 说明 |
| --- | --- |
| start | 开始事件。返回 {width, height} |
| stop | 结束事件。 |
| seek | seek 完成事件。 |
| bufferchange | 缓冲区变化事件。 |
| ended | 解码结束事件。 |

<a id="callback"></a>

#### Callback

事件触发时执行的回调函数

```tsx
(res: { width: number; height: number; }) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `{ width: number; height: number; }` |

<a id="start-1"></a>

### start

<a id="option"></a>

#### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| source | `string` |  | 是 | 需要解码的视频源文件。 |
| mode | `number` | `1` | 否 | 解码模式。0：按 pts 解码；1：以最快速度解码 |
| abortAudio | `boolean` | `false` | 否 | 是否不需要音频轨道 |
| abortVideo | `boolean` | `false` | 否 | 是否不需要视频轨道 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| VideoDecoder.getFrameData | ✔️ |  |  |  |  |
| VideoDecoder.off | ✔️ |  |  |  |  |
| VideoDecoder.on | ✔️ |  |  |  |  |
| VideoDecoder.remove | ✔️ |  |  |  |  |
| VideoDecoder.seek | ✔️ |  |  |  |  |
| VideoDecoder.start | ✔️ |  |  |  |  |
| VideoDecoder.stop | ✔️ |  |  |  |  |
