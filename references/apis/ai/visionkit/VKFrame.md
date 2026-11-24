# VKFrame

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/ai/visionkit/VKFrame)

vision kit 会话对象

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/visionkit/VKFrame.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| timestamp | `number` | 生成时间 |
| camera | `VKCamera` | 相机对象 |

<a id="getcameratexture"></a>

### getCameraTexture

获取当前帧纹理，目前只支持 YUV 纹理

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/visionkit/VKFrame.getCameraTexture.html)

```tsx
(ctx: WebGLRenderingContext) => IGetCameraTextureResult
```

| 参数 | 类型 |
| --- | --- |
| ctx | `WebGLRenderingContext` |

<a id="getcamerabuffer"></a>

### getCameraBuffer

获取当前帧 rgba buffer。iOS 端微信在 v8.0.20 开始支持，安卓端微信在 v8.0.30 开始支持。
按 aspect-fill 规则裁剪，此接口要求在创建 VKSession 对象时必须传入 gl 参数。
此接口仅建议拿来做帧分析使用，上屏请使用 getCameraTexture 来代替。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/visionkit/VKFrame.getCameraBuffer.html)

```tsx
(widht: number, height: number) => ArrayBuffer
```

| 参数 | 类型 |
| --- | --- |
| widht | `number` |
| height | `number` |

<a id="getdisplaytransform"></a>

### getDisplayTransform

获取纹理调整矩阵。默认获取到的纹理是未经裁剪调整的纹理，此矩阵可用于在着色器中根据帧对象尺寸对纹理进行裁剪

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/visionkit/VKFrame.getDisplayTransform.html)

```tsx
() => Float32Array
```

<a id="参数"></a>

## 参数

<a id="igetcameratextureresult"></a>

### IGetCameraTextureResult

帧纹理对象

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| yTexture | `WebGLTexture` | Y 分量纹理 |
| uvTexture | `WebGLTexture` | UV 分量纹理 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| VKFrame | ✔️ |  |  |  |  |
| VKFrame.getCameraTexture | ✔️ |  |  |  |  |
| VKFrame.getCameraBuffer | ✔️ |  |  |  |  |
| VKFrame.getDisplayTransform | ✔️ |  |  |  |  |
