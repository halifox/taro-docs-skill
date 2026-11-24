# Taro.authorizeForMiniProgram(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/open-api/authorize/authorizeForMiniProgram)

**仅小程序插件中能调用该接口**，用法同 [Taro.authorize](../authorize.md)。目前仅支持三种 scope

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/authorize/wx.authorizeForMiniProgram.html)

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

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| scope | `string` | 是 | 需要获取权限的 scope，详见 [scope 列表](https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/authorize.html#scope-%E5%88%97%E8%A1%A8) |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="scope"></a>

### Scope

scope 合法值

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/authorize.html#scope-%E5%88%97%E8%A1%A8)

<a id="示例代码"></a>

## 示例代码

```tsx
// 可以通过 Taro.getSetting 先查询一下用户是否授权了 "scope.record" 这个 scope
Taro.authorizeForMiniProgram({
  scope: 'scope.record',
  success () {
    // 用户已经同意小程序使用录音功能，后续调用 Taro.startRecord 接口不会弹窗询问
    Taro.startRecord()
  }
})
```
