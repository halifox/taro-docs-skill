# Taro.getStorageInfo(OBJECT)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/storage/getStorageInfo)

异步获取当前 storage 的相关信息，支持 `Promise` 化使用。

**OBJECT 参数说明：**

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| success | Function | 否 | 接口调用成功的回调函数，详见返回参数说明 |
| fail | Function | 否 | 接口调用失败的回调函数 |
| complete | Function | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |

**success 返回参数说明：**

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| keys | String Array | 当前 storage 中所有的 key |

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.getStorageInfo()
  .then(res => console.log(res.keys))
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.getStorageInfo | ✔️ | ✔️ | ✔️ |
| Taro.getStorageInfoSync | ✔️ | ✔️ |  |
