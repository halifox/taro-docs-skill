# Taro.sendHCEMessage(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/device/nfc/sendHCEMessage)

发送 NFC 消息。仅在安卓系统下有效。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/nfc/wx.sendHCEMessage.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<TaroGeneral.NFCError>
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
| data | `ArrayBuffer` | 是 | 二进制数据 |
| complete | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.NFCError) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
const buffer = new ArrayBuffer(1)
const dataView = new DataView(buffer)
dataView.setUint8(0, 0)
      Taro.startHCE({
  success: function (res) {
    Taro.onHCEMessage(function (res) {
      if (res.messageType === 1) {
        Taro.sendHCEMessage({data: buffer})
      }
    })
  }
})
```
