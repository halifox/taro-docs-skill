# Taro.createVideoContext(videoId, componentInstance)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/multimedia/video/createVideoContext)

创建 video 上下文 VideoContext 对象。

使用方式同 [`wx.createVideoContext`](https://developers.weixin.qq.com/miniprogram/dev/api/wx.createVideoContext.html)。

<a id="参数"></a>

## 参数

<a id="string-videoid"></a>

### string videoId

<Video> 组件的 id

<a id="component-componentinstance"></a>

### Component componentInstance

在自定义组件下，当前组件实例的this，以操作组件内 <Video> 组件

<a id="返回值"></a>

## 返回值

<a id="object-videocontext"></a>

### object VideoContext

| Property | Type | Description |
| --- | --- | --- |
| play() | function | 播放视频 |
| pause() | function | 暂停视频 |
| stop() | function | 停止视频 |
| seek(number position) | function | 跳转到指定位置 |
| sendDanmu(object data) | function | 发送弹幕 |
| playbackRate(number rate) | function | 设置倍速播放 |
| requestFullScreen(object object) | function | 进入全屏 |
| exitFullScreen() | function | 退出全屏 |
| showStatusBar() | function | 显示状态栏，仅在iOS全屏下有效 |
| hideStatusBar() | function | 隐藏状态栏，仅在iOS全屏下有效 |

注: IOS系统下，h5端部分VideoContext的属性未完全实现。

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

const videoContext = Taro.createVideoContext('myVideo')
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.createVideoContext | ✔️ | ✔️ |  |
