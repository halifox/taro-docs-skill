# VKDepthAnchor

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/ai/visionkit/VKDepthAnchor)

depth anchor

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/visionkit/VKDepthAnchor.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| id | `number` | 唯一标识 |
| type | `8` | 类型 |
| size | `ISize` | 相对视窗的尺寸，取值范围为 [0, 1]，0 为左/上边缘，1 为右/下边缘 |
| depthArray | `number[]` | 包含深度信息的数组 |

<a id="参数"></a>

## 参数

<a id="itype"></a>

### IType

类型

| 参数 | 说明 |
| --- | --- |
| 8 | DEPTH |

<a id="isize"></a>

### ISize

相对视窗的尺寸

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| width | `number` | 宽度 |
| height | `number` | 高度 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| VKDepthAnchor | ✔️ |  |  |  |  |
