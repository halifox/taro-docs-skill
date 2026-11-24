# Taro.shareVideoMessage(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/share/shareVideoMessage)

转发视频到聊天

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/share/wx.shareVideoMessage.html)

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
| videoPath | `string` | 是 | 要分享的视频地址，必须为本地路径或临时路径 |
| thumbPath | `string` | 否 | 缩略图路径，若留空则使用视频首帧 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="示例代码"></a>

## 示例代码

callback 写法

```tsx
Taro.downloadFile({
  url: URL, // 下载url
  success (res) {
    // 下载完成后转发
    Taro.shareVideoMessage({
      videoPath: res.tempFilePath,
      success() {},
      fail: console.error,
    })
  },
  fail: console.error,
})
```

async await 写法

```tsx
const { tempFilePath } = await Taro.downloadFile({
  url: URL, // 下载url
})
// 下载完成后转发
await Taro.shareVideoMessage({
  videoPath: res.tempFilePath,
})
```
