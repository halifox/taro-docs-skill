# VKPlaneAnchor

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/ai/visionkit/VKPlaneAnchor)

平面 anchor，只有 v2 版本支持

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/visionkit/VKPlaneAnchor.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| id | `number` | 唯一标识 |
| type | `0` | 类型 |
| transform | `Float32Array` | 包含位置、旋转、放缩信息的矩阵，以列为主序 |
| size | `ISize` | 尺寸 |
| alignment | `number` | 方向 |

<a id="参数"></a>

## 参数

<a id="itype"></a>

### IType

类型

| 参数 | 说明 |
| --- | --- |
| 0 | 平面 |

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
| VKPlaneAnchor | ✔️ |  |  |  |  |
