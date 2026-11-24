# Taro.saveVideoToPhotosAlbum(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/media/video/saveVideoToPhotosAlbum)

保存视频到系统相册。支持mp4视频格式。需要[用户授权](https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/authorize.html) scope.writePhotosAlbum

**Bug & Tip：**

1. `tip`: camera 参数在部分 Android 手机下由于系统 ROM 不支持无法生效

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/video/wx.saveVideoToPhotosAlbum.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<CallbackResult>
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| filePath | `string` | 是 | 视频文件路径，可以是临时文件路径也可以是永久文件路径 |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.saveVideoToPhotosAlbum({
  filePath: 'wxfile://xxx'
  success: function (res) {
    console.log(res.errMsg)
  }
})
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.saveVideoToPhotosAlbum | ✔️ |  | ✔️ |
