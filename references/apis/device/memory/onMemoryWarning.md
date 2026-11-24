# Taro.onMemoryWarning(callback)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/device/memory/onMemoryWarning)

监听内存不足告警事件。

当 iOS/Android 向小程序进程发出内存警告时，触发该事件。触发该事件不意味小程序被杀，大部分情况下仅仅是告警，开发者可在收到通知后回收一些不必要资源避免进一步加剧内存紧张。

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/performance/wx.onMemoryWarning.html)

<a id="类型"></a>

## 类型

```tsx
(callback: Callback) => void
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 内存不足告警事件的回调函数 |

<a id="callback"></a>

### Callback

内存不足告警事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="callbackresult"></a>

### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| level | `keyof Level` | 内存告警等级，只有 Android 才有，对应系统宏定义 |

<a id="level"></a>

### Level

| 参数 | 说明 |
| --- | --- |
| 5 | TRIM\_MEMORY\_RUNNING\_MODERATE |
| 10 | TRIM\_MEMORY\_RUNNING\_LOW |
| 15 | TRIM\_MEMORY\_RUNNING\_CRITICAL |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.onMemoryWarning(function () {
  console.log('onMemoryWarningReceive')
})
```
