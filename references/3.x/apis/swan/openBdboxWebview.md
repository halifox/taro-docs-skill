# Taro.openBdboxWebview(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/swan/openBdboxWebview)

小程序跳转百度 App 内特定页面。接入本 API 的开发者，需要了解跳转页面的 scheme，并根据文档调用 API 完成跳转。可在百度 App 中，通过将跳转页面 scheme 生成对应二维码，并使用百度 APP 相机扫描二维码调起的方式，来确保 scheme 是否正确。
Web 态说明：
1.由于浏览器的限制，Web 态暂时无法准确获取跳转百度 App 成功 / 失败状态，会执行失败回调；
2.在用户未安装手百、部分第三方浏览器封禁百度 App 的情况下，Web 态会尝试降级调起应用商店。

支持情况：微信小程序 百度小程序 H5 React Native Harmony

> [参考文档](https://smartprogram.baidu.com/docs/develop/api/open/swan-openBdboxWebview/)

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
| module | `string` | 否 | 跳转百度 App 特定页面的 scheme 的 module |
| action | `string` | 否 | 跳转百度 App 特定页面的 scheme 的 action |
| path | `string` | 否 | 跳转百度 App 特定页面的 scheme 的 path |
| authority | `string` | 否 | 跳转百度 App 特定页面的 scheme 的 authority |
| parameters | `Object` | 否 | 跳转百度 App 特定页面的 scheme 的参数 |
| success | `(res: any) => any` | 否 | 接口调用成功的回调函数 |
| fail | `(err: any) => any` | 否 | 接口调用失败的回调函数 |
| complete | `(res: any) => any` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
