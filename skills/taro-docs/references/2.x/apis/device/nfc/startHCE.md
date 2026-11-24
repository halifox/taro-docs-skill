# Taro.startHCE(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/device/nfc/startHCE)

初始化 NFC 模块。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/nfc/wx.startHCE.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<NFCError>
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| aid\_list | `string[]` | 是 | 需要注册到系统的 AID 列表 |
| complete | `(res: NFCError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: NFCError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: NFCError) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.startHCE({
  aid_list: ['F222222222']
  success: function (res) {
    console.log(res.errMsg)
  }
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.startHCE | ✔️ |  |  |
