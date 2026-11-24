# Taro.isAddedToMyApps(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/qq/isAddedToMyApps)

查询用户是否已经将本小程序添加到下拉页面中“我的小程序”当中，手Q8.9.13及以上版本支持，建议使用qq.applyAddToMyApps之前先调用qq.isAddedToMyApps来作前置判断

支持情况：微信小程序 QQ 小程序 H5 React Native Harmony

> [参考文档](https://q.qq.com/wiki/develop/miniprogram/API/open_port/port_addToMyApps.html#qq-isaddedtomyapps)

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
| success | `(res: SuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="successcallbackresult"></a>

### SuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| isAdded | `boolean` | true 代表用户已经添加，false 则还没添加 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.isAddedToMyApps({
  success(res) {
    if (res.isAdded) {
      // 用户已经添加
    } else {
      // 用户还未添加
    }
  }
})
```
