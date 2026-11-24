# Taro.onDeviceMotionChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/device/deviceMotion/onDeviceMotionChange)

监听设备方向变化事件。频率根据 wx.startDeviceMotionListeningListening() 的 interval 参数。可以使用 wx.stopDeviceMotionListeningListening() 停止监听。

<a id="参数"></a>

## 参数

<a id="callbackres"></a>

### callback(res)

设备方向变化事件的回调函数。

<a id="参数-1"></a>

#### 参数

<a id="object-res"></a>

##### object res

| Name | Type | Description |
| --- | --- | --- |
| alpha | `number` | 当手机坐标 X/Y 和 地球 X/Y 重合时，绕着 Z 轴转动的夹角为 alpha，范围值为 [0, 2\*PI)。逆时针转动为正。 |
| beta | `number` | 当手机坐标 Y/Z 和地球 Y/Z 重合时，绕着 X 轴转动的夹角为 beta。范围值为 [-1\*PI, PI) 。顶部朝着地球表面转动为正。也有可能朝着用户为正。 |
| gamma | `number` | 当手机 X/Z 和地球 X/Z 重合时，绕着 Y 轴转动的夹角为 gamma。范围值为 [-1\*PI/2, PI/2)。右边朝着地球表面转动为正。 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.onDeviceMotionChange | ✔️ | ✔️ | ✔️ |
