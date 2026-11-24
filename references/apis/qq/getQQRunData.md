# Taro.getQQRunData(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/qq/getQQRunData)

获取用户过去三十天QQ运动步数。需要先调用 qq.login 接口。步数信息会在用户主动进入小程序时更新。

支持情况：微信小程序 QQ 小程序 H5 React Native Harmony

> [参考文档](https://q.qq.com/wiki/develop/miniprogram/API/open_port/port_sport.html)

<a id="类型"></a>

## 类型

```tsx
(option: Option) => void
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
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| encryptedData | `string` | 包括敏感数据在内的完整用户信息的加密数据，详细见加密数据解密算法。 |
| iv | `string` | 加密算法的初始向量，详细见加密数据解密算法 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.getQQRunData({
  success(res) {
    // 拿 encryptedData 到开发者后台解密开放数据
    const encryptedData = res.encryptedData
  }
})
```

**开放数据 JSON 结构**
敏感数据有两种获取方式，一是使用 加密数据解密算法 。 获取得到的开放数据为以下 json 结构：

```json
{
  "stepInfoList": [
    {
      "timestamp": 1445866601,
      "step": 100
    },
    {
      "timestamp": 1445876601,
      "step": 120
    }
  ]
}
```

- stepInfoList 中，每一项结构如下：

| 属性 | 类型 | 说明 |
| --- | --- | --- |
| timestamp | number | 时间戳，表示数据对应的时间 |
| step | number | QQ运动步数 |
