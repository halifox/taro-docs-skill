# Taro.startDeviceMotionListening(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/device/deviceMotion/startDeviceMotionListening)

开始监听设备方向的变化。

<a id="参数"></a>

## 参数

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| interval | `'game'` / `'ui'` / `'normal'` | `normal` | 监听设备方向回调函数的执行频率 game 适用于更新游戏的回调频率，在 20ms/次 左右 ui 适用于更新 UI 的回调频率，在 60ms/次 左右 normal 普通的回调频率，在 200ms/次 左右 |
| success | `function` |  | 接口调用成功的回调函数 |
| fail | `function` |  | 接口调用失败的回调函数 |
| complete | `function` |  | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.startDeviceMotionListening | ✔️ | ✔️ | ✔️ |
