# Taro.chooseMessageFile(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/image/chooseMessageFile)

从客户端会话选择文件。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/image/wx.chooseMessageFile.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<SuccessCallbackResult>
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| count | `number` | 是 | 最多可以选择的文件个数，可以 0～100 |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| extension | `string[]` | 否 | 根据文件拓展名过滤，仅 type==file 时有效。每一项都不能是空字符串。默认不过滤。 |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |
| type | `"all" \| "video" \| "image" \| "file"` | 否 | 所选的文件的类型 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| tempFiles | `ChooseFile[]` | 返回选择的文件的本地临时文件对象数组 |
| errMsg | `string` | 调用结果 |

<a id="choosefile"></a>

### ChooseFile

返回选择的文件的本地临时文件对象数组

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| name | `string` | 选择的文件名称 |
| path | `string` | 本地临时文件路径 |
| size | `number` | 本地临时文件大小，单位 B |
| time | `number` | 选择的文件的会话发送时间，Unix时间戳，工具暂不支持此属性 |
| type | `"video" \| "image" \| "file"` | 选择的文件类型 |

<a id="selecttype"></a>

### selectType

| 参数 | 说明 |
| --- | --- |
| all | 从所有文件选择 |
| video | 只能选择视频文件 |
| image | 只能选择图片文件 |
| file | 可以选择除了图片和视频之外的其它的文件 |

<a id="selectedtype"></a>

### selectedType

| 参数 | 说明 |
| --- | --- |
| video | 选择了视频文件 |
| image | 选择了图片文件 |
| file | 选择了除图片和视频的文件 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.chooseMessageFile({
  count: 10,
  type: 'image',
  success: function (res) {
    // tempFilePath可以作为img标签的src属性显示图片
    const tempFilePaths = res.tempFiles
  }
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.chooseMessageFile | ✔️ |  |  |
