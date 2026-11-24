# ReadResult

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/files/ReadResult)

文件读取结果。 通过 [FileSystemManager.readSync](FileSystemManager.md#readsync) 接口返回

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/file/ReadResult.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| bytesRead | `number` | 实际读取的字节数 |
| arrayBuffer | `ArrayBuffer` | 被写入的缓存区的对象，即接口入参的 arrayBuffer |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| ReadResult | ✔️ |  |  |  | ✔️ |
