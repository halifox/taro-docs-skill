# Taro.saveFileToDisk(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/files/saveFileToDisk)

保存文件系统的文件到用户磁盘，仅在 PC 端支持

支持情况：微信小程序 支付宝小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/file/wx.saveFileToDisk.html)

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
| filePath | `string` | 是 | 待保存文件路径 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(result: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.saveFileToDisk({
  filePath: `${Taro.env.USER_DATA_PATH}/hello.txt`,
  success(res) {
    console.log(res)
  },
  fail(res) {
    console.error(res)
  }
})
```
