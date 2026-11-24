# Taro.downloadPackages(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/swan/download-package/downloadPackages)

针对在小程序中调用其他小程序的场景，预下载其他小程序的包内容。
Web 态说明：Web 态不支持预下载的能力。

支持情况：微信小程序 百度小程序 H5 React Native Harmony

> [参考文档](https://smartprogram.baidu.com/docs/develop/api/open/swan-downloadPackages/)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => void
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
| pageList | `IPageItem[]` | 是 | 预下载的小程序的列表。 |
| success | `(res: SuccessCallbackResult) => any` | 否 | 接口调用成功的回调函数 |
| fail | `(err: TaroGeneral.CallbackResult) => any` | 否 | 接口调用失败的回调函数 |
| complete | `(res: TaroGeneral.CallbackResult) => any` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="ipageitem"></a>

### IPageItem

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| appKey | `string` | 预下载的小程序的 appKey |
| pages | `string[]` | 页面路径 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| \_\_index | `__index` | 小程序包预下载结果回调 |

<a id="iappkeyresult"></a>

### IAppKeyResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| pageUrl | `string` | 页面路径 |
| status | `string` | 预下载能力调用结果。值为 "0" 时是成功，非 "0" 时是失败 |
| message | `string` | 预下载结果信息 |
