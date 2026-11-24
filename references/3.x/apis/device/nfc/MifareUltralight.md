# MifareUltralight

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/device/nfc/MifareUltralight)

MifareUltralight 标签

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/nfc/MifareUltralight.html)

<a id="方法"></a>

## 方法

<a id="close"></a>

### close

断开连接

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/nfc/MifareUltralight.close.html)

```tsx
(option?: Option) => Promise<TaroGeneral.NFCError>
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="connect"></a>

### connect

连接 NFC 标签

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/nfc/MifareUltralight.connect.html)

```tsx
(option?: Option) => Promise<TaroGeneral.NFCError>
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="getmaxtransceivelength"></a>

### getMaxTransceiveLength

获取最大传输长度

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/nfc/MifareUltralight.getMaxTransceiveLength.html)

```tsx
(option?: Option) => Promise<TaroGeneral.NFCError>
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="isconnected"></a>

### isConnected

检查是否已连接

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/nfc/MifareUltralight.isConnected.html)

```tsx
(option?: Option) => Promise<TaroGeneral.NFCError>
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="settimeout"></a>

### setTimeout

设置超时时间

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/nfc/MifareUltralight.setTimeout.html)

```tsx
(option?: Option) => Promise<TaroGeneral.NFCError>
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="transceive"></a>

### transceive

发送数据

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/nfc/MifareUltralight.transceive.html)

```tsx
(option?: Option) => Promise<TaroGeneral.NFCError>
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="参数"></a>

## 参数

<a id="close-1"></a>

### close

<a id="option"></a>

#### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用成功的回调函数 |

<a id="connect-1"></a>

### connect

<a id="option-1"></a>

#### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用成功的回调函数 |

<a id="getmaxtransceivelength-1"></a>

### getMaxTransceiveLength

<a id="option-2"></a>

#### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

#### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| length | `number` | 最大传输长度 |

<a id="isconnected-1"></a>

### isConnected

<a id="option-3"></a>

#### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用成功的回调函数 |

<a id="settimeout-1"></a>

### setTimeout

<a id="option-4"></a>

#### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| timeout | `number` | 是 | 设置超时时间 (ms) |
| complete | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用成功的回调函数 |

<a id="transceive-1"></a>

### transceive

<a id="option-5"></a>

#### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| data | `ArrayBuffer` | 是 | 需要传递的二进制数据 |
| complete | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult-1"></a>

#### SuccessCallbackResult

| 参数 | 类型 |
| --- | --- |
| data | `ArrayBuffer` |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- |
| MifareUltralight | ✔️ |  |  |  |  |
| MifareUltralight.close | ✔️ |  |  |  |  |
| MifareUltralight.connect | ✔️ |  |  |  |  |
| MifareUltralight.getMaxTransceiveLength | ✔️ |  |  |  |  |
| MifareUltralight.isConnected | ✔️ |  |  |  |  |
| MifareUltralight.setTimeout | ✔️ |  |  |  |  |
| MifareUltralight.transceive | ✔️ |  |  |  |  |
