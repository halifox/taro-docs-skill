# VKOSDAnchor

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/ai/visionkit/VKOSDAnchor)

OSD anchor

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/visionkit/VKOSDAnchor.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| id | `number` | 唯一标识 |
| type | `2` | 类型 |
| markerId | `number` | marker id |
| size | `ISize` | 相对视窗的尺寸，取值范围为 [0, 1]，0 为左/上边缘，1 为右/下边缘 |
| path | `string` | 图片路径 |
| origin | `IOrigin` | 相对视窗的位置信息，取值范围为 [0, 1]，0 为左/上边缘，1 为右/下边缘 |

<a id="参数"></a>

## 参数

<a id="itype"></a>

### IType

类型

| 参数 | 说明 |
| --- | --- |
| 2 | OSD |

<a id="isize"></a>

### ISize

相对视窗的尺寸

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| width | `number` | 宽度 |
| height | `number` | 高度 |

<a id="iorigin"></a>

### IOrigin

相对视窗的位置信息

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| x | `number` | 横坐标 |
| y | `number` | 纵坐标 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| VKOSDAnchor | ✔️ |  |  |  |  |
