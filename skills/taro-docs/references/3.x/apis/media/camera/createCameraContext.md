# Taro.createCameraContext(id)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/media/camera/createCameraContext)

创建 camera 上下文 CameraContext 对象。

支持情况：微信小程序 支付宝小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> 支付宝小程序: 支付宝小程序需指定 camera 组件中的 id 属性

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/camera/wx.createCameraContext.html)

<a id="类型"></a>

## 类型

```tsx
(id?: string) => CameraContext
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| id | `string` |

<a id="示例代码"></a>

## 示例代码

```tsx
const cameraContext = Taro.createCameraContext()
```
