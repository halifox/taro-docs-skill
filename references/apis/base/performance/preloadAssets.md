# Taro.preloadAssets(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/base/performance/preloadAssets)

为视图层预加载媒体资源文件, 目前支持：font，image

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/performance/wx.preloadAssets.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<TaroGeneral.CallbackResult>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="assetsobjecttype"></a>

### AssetsObjectType

| 参数 | 说明 |
| --- | --- |
| font | 字体 |
| image | 图片 |

<a id="assetsobject"></a>

### AssetsObject

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| type | `keyof AssetsObjectType` | 类型 |
| src | `string` | 资源地址 |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| data | `AssetsObject[]` | 是 |  |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |
