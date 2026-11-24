# MediaTrack

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/video-processing/MediaTrack)

可通过 [MediaContainer.extractDataSource](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-processing/MediaContainer.extractDataSource.html) 返回。
[MediaTrack](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-processing/MediaTrack.html) 音频或视频轨道，可以对轨道进行一些操作

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video-processing/MediaTrack.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 只读 | 说明 |
| --- | --- | --- | --- |
| duration | `number` | 是 | 轨道长度 |
| kind | `"audio" \| "video"` | 是 | 轨道类型 |
| volume | `number` | 否 | 音量，音频轨道下有效，可写 |

<a id="参数"></a>

## 参数

<a id="kind"></a>

### kind

| 参数 | 说明 |
| --- | --- |
| audio | 音频轨道 |
| video | 视频轨道 |
