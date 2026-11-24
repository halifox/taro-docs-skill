# VKCamera

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/ai/visionkit/VKCamera)

相机对象

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/visionkit/VKCamera.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| viewMatrix | `Float32Array` | 视图矩阵 |
| intrinsics | `Float32Array` | 相机内参，只有 v2 版本支持 |

<a id="getprojectionmatrix"></a>

### getProjectionMatrix

获取投影矩阵

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/visionkit/VKCamera.getProjectionMatrix.html)

```tsx
(near: number, far: number) => Float32Array
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| near | `number` | 近视点 |
| far | `number` | 远视点 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| VKCamera | ✔️ |  |  |  |  |
| VKCamera.getProjectionMatrix | ✔️ |  |  |  |  |
