# Taro.getStorageSync(KEY)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/storage/getStorageSync)

从本地缓存中同步获取指定 key 对应的内容。

**参数说明：**

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| key | String | 是 | 本地缓存中的指定的 key |

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

const data = Taro.getStorageSync('key')
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.getStorageSync | ✔️ | ✔️ |  |
