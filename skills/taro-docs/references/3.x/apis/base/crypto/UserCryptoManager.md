# UserCryptoManager

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/base/crypto/UserCryptoManager)

用户加密模块

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/crypto/UserCryptoManager.html)

<a id="方法"></a>

## 方法

<a id="getlatestuserkey"></a>

### getLatestUserKey

获取最新的用户加密密钥

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/crypto/UserCryptoManager.getLatestUserKey.html)

```tsx
(option: Option) => Promise<SuccessCallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="示例代码"></a>

#### 示例代码

```tsx
const userCryptoManager = Taro.getUserCryptoManager()
userCryptoManager.getLatestUserKey({
  success: res => {
    const { encryptKey, iv, version, expireTime } = res
    console.log(encryptKey, iv, version, expireTime)
  }
})
```

<a id="getrandomvalues"></a>

### getRandomValues

获取密码学安全随机数

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/crypto/UserCryptoManager.getRandomValues.html)

```tsx
(option: Option) => void
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="示例代码-1"></a>

#### 示例代码

```tsx
Taro.getUserCryptoManager().getRandomValues({
  length: 6 // 生成 6 个字节长度的随机数,
  success: res => {
    console.log(Taro.arrayBufferToBase64(res.randomValues)) // 转换为 base64 字符串后打印
  }
})
```

<a id="参数"></a>

## 参数

<a id="getlatestuserkey-1"></a>

### getLatestUserKey

<a id="option"></a>

#### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| success | `(res: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| complete | `(res: SuccessCallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="successcallbackresult"></a>

#### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| encryptKey | `string` | 用户加密密钥 |
| iv | `string` | 密钥初始向量 |
| version | `number` | 密钥版本 |
| expireTime | `number` | 密钥过期时间 |

<a id="getrandomvalues-1"></a>

### getRandomValues

<a id="option-1"></a>

#### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| length | `number` | 是 | 整数，生成随机数的字节数，最大 1048576 |
| success | `(res: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| complete | `(res: SuccessCallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="successcallbackresult-1"></a>

#### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| randomValues | `ArrayBuffer` | 随机数内容，长度为传入的字节数 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| UserCryptoManager | ✔️ |  |  |  |  |
| UserCryptoManager.getLatestUserKey | ✔️ |  |  |  |  |
| UserCryptoManager.getRandomValues | ✔️ |  |  |  |  |
