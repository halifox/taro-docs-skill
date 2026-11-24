# Taro.setEnable1v1Chat(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/media/voip/setEnable1v1Chat)

开启双人通话

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/voip/wx.setEnable1v1Chat.html)

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

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| enable | `boolean` |  | 是 | 是否开启 |
| backgroundType | `keyof ColorType` | `0` | 否 | 窗口背景色 |
| minWindowType | `keyof ColorType` | `1` | 否 | 小窗样式 |
| complete | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="colortype"></a>

### ColorType

音频通话背景以及小窗模式背景

| 参数 | 说明 |
| --- | --- |
| 0 | #262930 |
| 1 | #FA5151 |
| 2 | #FA9D3B |
| 3 | #3D7257 |
| 4 | #1485EE |
| 5 | #6467F0 |
