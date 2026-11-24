# MediaRecorder

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/media/media-recorder/MediaRecorder)

<a id="方法"></a>

## 方法

<a id="destroy"></a>

### destroy

销毁录制器

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/MediaRecorder.destroy.html)

```tsx
() => Promise<void>
```

<a id="off"></a>

### off

取消监听录制事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/MediaRecorder.off.html)

```tsx
(eventName: keyof EventName, callback: Callback) => Promise<void>
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| eventName | `keyof EventName` | 事件名 |
| callback | `Callback` | 事件触发时执行的回调函数 |

<a id="on"></a>

### on

注册监听录制事件的回调函数

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/MediaRecorder.on.html)

```tsx
(eventName: keyof EventName, callback: Callback) => Promise<void>
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| eventName | `keyof EventName` | 事件名 |
| callback | `Callback` | 事件触发时执行的回调函数 |

<a id="pause"></a>

### pause

暂停录制

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/MediaRecorder.pause.html)

```tsx
() => Promise<void>
```

<a id="requestframe"></a>

### requestFrame

请求下一帧录制，在 callback 里完成一帧渲染后开始录制当前帧

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/MediaRecorder.requestFrame.html)

```tsx
(callback: Callback) => Promise<void>
```

| 参数 | 类型 |
| --- | --- |
| callback | `Callback` |

<a id="resume"></a>

### resume

恢复录制

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/MediaRecorder.resume.html)

```tsx
() => Promise<void>
```

<a id="start"></a>

### start

开始录制

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/MediaRecorder.start.html)

```tsx
() => Promise<void>
```

<a id="stop"></a>

### stop

结束录制

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-decoder/MediaRecorder.stop.html)

```tsx
() => Promise<void>
```

<a id="参数"></a>

## 参数

<a id="on-1"></a>

### on

<a id="eventname"></a>

#### EventName

eventName 的合法值

| 参数 | 说明 |
| --- | --- |
| start | 录制开始事件。 |
| stop | 录制结束事件。返回 {tempFilePath, duration, fileSize} |
| pause | 录制暂停事件。 |
| resume | 录制继续事件。 |
| timeupdate | 录制时间更新事件。 |

<a id="callback"></a>

#### Callback

事件触发时执行的回调函数

```tsx
(res: { tempFilePath: string; duration: number; fileSize: number; }) => void
```

| 参数 | 类型 |
| --- | --- |
| res | `{ tempFilePath: string; duration: number; fileSize: number; }` |

<a id="requestframe-1"></a>

### requestFrame

<a id="callback-1"></a>

#### Callback

事件触发时执行的回调函数

```tsx
() => void
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| MediaRecorder.destroy | ✔️ |  |  |  |  |
| MediaRecorder.off | ✔️ |  |  |  |  |
| MediaRecorder.on | ✔️ |  |  |  |  |
| MediaRecorder.pause | ✔️ |  |  |  |  |
| MediaRecorder.requestFrame | ✔️ |  |  |  |  |
| MediaRecorder.resume | ✔️ |  |  |  |  |
| MediaRecorder.start | ✔️ |  |  |  |  |
| MediaRecorder.stop | ✔️ |  |  |  |  |
