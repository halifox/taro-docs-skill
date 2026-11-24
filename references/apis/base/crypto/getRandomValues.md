# Taro.getRandomValues(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/base/crypto/getRandomValues)

获取密码学安全随机数

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/crypto/UserCryptoManager.getRandomValues.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<SuccessCallbackResult>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getRandomValues({
  length: 6 // 生成 6 个字节长度的随机数
}).then(res => {
  console.log(Taro.arrayBufferToBase64(res.randomValues)) // 转换为 base64 字符串后打印
})
```
