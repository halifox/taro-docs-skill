# Taro.onAccelerometerChange(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/device/accelerometer/onAccelerometerChange)

监听加速度数据事件。频率根据 `startAccelerometer()` 的 `interval` 参数。可使用 `stopAccelerometer()` 停止监听。

<a id="参数"></a>

## 参数

<a id="function-callbackres"></a>

### function callback(res)

加速度数据事件的回调函数。

<a id="参数-1"></a>

#### 参数

<a id="object-res"></a>

##### object res

| Name | Type | Description |
| --- | --- | --- |
| x | `number` | X 轴 |
| y | `number` | Y 轴 |
| z | `number` | Z 轴 |

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.onAccelerometerChange(res => {
  console.log(res.x)
  console.log(res.y)
  console.log(res.z)
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.onAccelerometerChange | ✔️ | ✔️ | ✔️ |
