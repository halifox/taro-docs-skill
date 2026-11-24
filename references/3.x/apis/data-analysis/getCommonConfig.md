# Taro.getCommonConfig(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/data-analysis/getCommonConfig)

给定实验参数数组，获取对应的实验参数值

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/data-analysis/wx.getCommonConfig.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => Promise<SuccessCallbackResult>
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
| keys | `string[]` | 否 | 需要获取的数据指标的对象数组，每个string的格式约定：配置类型\_分表key |
| mode | 0 or 1 | 是 | 0：通用配置模式 1：实验模式, 参数与返回结果的使用等效于接口wx.getExptInfoSync |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| errcode | `number` | 错误码 |
| errmsg | `string` | 错误信息 |
| conf\_type | `number` | 配置类型, 1-表类型 2-kv类型 |
| conf | `string` | 根据conf\_type来确定conf内容, conf\_type为1时conf是一个json数组, 类似"[{xxx},{xxx}]", 每一项对应表类型每一行配置内容, 其中conf\_type为2时conf是一个json对象，类似"{xxxx}" |
| expire\_sec | `number` | 过期时间,单位秒. 0表示当次有效 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getCommonConfig({
  keys:["key1", "key2"],
  mode: 0,
  success: (res) => {
    console.log("success")
    console.log(res)
  },
  fail: (res) => {
    console.log("fail")
    console.log(res)
  }
})
```
