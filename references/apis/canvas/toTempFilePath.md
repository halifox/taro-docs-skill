# toTempFilePath

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/canvas/toTempFilePath)

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| x | `number` |  | 否 | 指定的画布区域的左上角横坐标 |
| y | `number` |  | 否 | 指定的画布区域的左上角纵坐标 |
| width | `number` |  | 否 | 指定的画布区域的宽度 |
| height | `number` |  | 否 | 指定的画布区域的高度 |
| destHeight | `number` |  | 否 | 输出的图片的高度 |
| destWidth | `number` |  | 否 | 输出的图片的宽度 |
| fileType | `keyof FileType` | `"png"` | 否 | 目标文件的类型 |
| quality | `number` |  | 否 | 图片的质量，目前仅对 jpg 有效。取值范围为 (0, 1]，不在范围内时当作 1.0 处理。 |
| complete | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="filetype"></a>

### FileType

| 参数 | 说明 |
| --- | --- |
| jpg | jpg 图片 |
| png | png 图片 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| tempFilePath | `string` | 生成文件的临时路径 |
