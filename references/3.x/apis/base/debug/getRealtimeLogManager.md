# Taro.getRealtimeLogManager()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/base/debug/getRealtimeLogManager)

获取实时日志管理器对象。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

<a id="类型"></a>

## 类型

```tsx
() => RealtimeLogManager
```

<a id="示例代码"></a>

## 示例代码

```tsx
const logger = Taro.getRealtimeLogManager()
logger.info({str: 'hello world'}, 'info log', 100, [1, 2, 3])
logger.error({str: 'hello world'}, 'error log', 100, [1, 2, 3])
logger.warn({str: 'hello world'}, 'warn log', 100, [1, 2, 3])
```
