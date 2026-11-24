# Taro.onNetworkStatusChange(CALLBACK)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/device/netstat/onNetworkStatusChange)

监听网络状态变化。

**CALLBACK 返回参数：**

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| isConnected | Boolean | 当前是否有网络连接 |
| networkType | String | 网络类型 |

注意：**H5** 端兼容情况较差，只有当 navigator.connection 支持监听 onChange 事件时才会生效。

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.onNetworkStatusChange(res => {
  console.log(res.isConnected)
  console.log(res.networkType)
})
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | ReactNative |
| --- | --- | --- | --- |
| Taro.onNetworkStatusChange | ✔️ | ✔️ | ✔️ |
