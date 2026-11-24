# Taro.createBufferURL(buffer)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/storage/createBufferURL)

根据传入的 buffer 创建一个唯一的 URL 存在内存中

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/storage/wx.createBufferURL.html)

<a id="类型"></a>

## 类型

```tsx
(buffer: TypedArray | ArrayBuffer) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| buffer | TypedArray or ArrayBuffer | 需要存入内存的二进制数据 |
