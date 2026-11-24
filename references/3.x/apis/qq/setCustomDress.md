# Taro.setCustomDress(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/qq/setCustomDress)

QQ美化平台内测阶段，仅被邀请的商户可使用此接口。

支持情况：微信小程序 QQ 小程序 H5 React Native Harmony

> [参考文档](https://q.qq.com/wiki/develop/miniprogram/API/open_port/personalize.html#qq-setcustomdress)

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
| action | `string` | 是 | 方法名，设置头像填"uploadAvatar"，其他方法后续开放 |
| path | `string` | 是 | 素材路径，必须为本地文件，路径为 wxfile:// 的形式 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.setCustomDress({
  action: "uploadAvatar",
  path:"wxfile://images/1.png"
  success(res) {
    console.log("success"+res);
  },
  fail(res) {
    console.log("fail"+res);
  }
})
```
