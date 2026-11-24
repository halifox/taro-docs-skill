# VKFaceAnchor

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/ai/visionkit/VKFaceAnchor)

人脸 anchor

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/visionkit/VKFaceAnchor.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| id | `number` | 唯一标识 |
| type | `3` | 类型 |
| detectId | `number` | 识别序号 |
| origin | `IOrigin` | 相对视窗的位置信息，取值范围为 [0, 1]，0 为左/上边缘，1 为右/下边缘 |
| size | `ISize` | 相对视窗的尺寸，取值范围为 [0, 1]，0 为左/上边缘，1 为右/下边缘 |
| points | `IPoint[]` | 人脸 106 个关键点的坐标 |
| angle | `number[]` | 人脸角度信息 |
| confidence | `number` | 关键点的置信度 |

<a id="参数"></a>

## 参数

<a id="itype"></a>

### IType

类型

| 参数 | 说明 |
| --- | --- |
| 3 | 人脸 |

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

<a id="ipoint"></a>

### IPoint

关键点

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| x | `number` | 横坐标 |
| y | `number` | 纵坐标 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| VKFaceAnchor | ✔️ |  |  |  |  |
