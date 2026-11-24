# Taro.setClipboardData(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/device/clipboard/setClipboardData)

设置系统剪贴板的内容。调用成功后，会弹出 toast 提示"内容已复制"，持续 1.5s

支持情况：微信小程序 百度小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> H5: 部分实现

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/clipboard/wx.setClipboardData.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<Promised>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="promised"></a>

### Promised

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errMsg | `string` | 调用信息 |
| data | `string` | 剪贴板的内容 |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| data | `string` | 是 | 剪贴板的内容 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.setClipboardData({
  data: 'data',
  success: function (res) {
    Taro.getClipboardData({
      success: function (res) {
        console.log(res.data) // data
      }
    })
  }
})
```
