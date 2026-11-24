# Taro.createInferenceSession(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/ai/inference/createInferenceSession)

创建 AI 推理 Session

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/ai/inference/wx.createInferenceSession.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => InferenceSession
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| model | `string` | 是 | 模型文件路径，目前只执行后缀为.onnx格式(支持代码包路径，和本地文件系统路径） |
| precesionLevel | `PrecesionLevel` | 否 | 推理精度，有效值为 0 - 4。<br>一般来说，使用的precesionLevel等级越低，推理速度越快，但可能会损失精度。<br>推荐开发者在开发时，在效果满足需求时优先使用更低精度以提高推理速度，节约能耗。 |
| allowQuantize | `boolean` | 否 | 是否生成量化模型推理 |
| allowNPU | `boolean` | 否 | 是否使用NPU推理，仅对IOS有效 |
| typicalShape | `boolean` | 否 | 输入典型分辨率 |

<a id="precesionlevel"></a>

### PrecesionLevel

| 参数 | 说明 |
| --- | --- |
| 0 | 使用fp16 存储浮点，fp16计算，Winograd 算法也采取fp16 计算，开启近似math计算 |
| 1 | 使用fp16 存储浮点，fp16计算，禁用 Winograd 算法，开启近似math计算 |
| 2 | 使用fp16 存储浮点，fp32计算，开启 Winograd，开启近似math计算 |
| 3 | 使用fp32 存储浮点，fp32计算，开启 Winograd，开启近似math计算 |
| 4 | 使用fp32 存储浮点，fp32计算，开启 Winograd，关闭近似math计算 |
