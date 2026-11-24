# Taro.getStorageInfoSync()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/storage/getStorageInfoSync)

同步获取当前 storage 的相关信息。

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

const res = Taro.getStorageInfoSync()
console.log(res.keys)
```

<a id="api支持度"></a>

## API支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.getStorageInfoSync | ✔️ | ✔️ |  |
