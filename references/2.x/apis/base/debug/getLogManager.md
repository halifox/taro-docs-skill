# Taro.getLogManager(res)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/base/debug/getLogManager)

获取日志管理器对象。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/wx.getLogManager.html)

<a id="类型"></a>

## 类型

```tsx
(res?: Option) => LogManager
```

<a id="参数"></a>

## 参数

<a id="option"></a>

### Option

| 参数 | 类型 | 默认值 | 必填 |
| --- | --- | --- | --- |
| level | `0 \| 1` | `0` | 否 |

<a id="level"></a>

### level

| 参数 | 说明 |
| --- | --- |
| 0 | 表示会把 App、Page 的生命周期函数和 wx 命名空间下的函数调用写入日志 |
| 1 | 表示不会把 App、Page 的生命周期函数和 wx 命名空间下的函数调用写入日志 |

<a id="示例代码"></a>

## 示例代码

```tsx
const logger = Taro.getLogManager({level: 1})

logger.log({str: 'hello world'}, 'basic log', 100, [1, 2, 3])
logger.info({str: 'hello world'}, 'info log', 100, [1, 2, 3])
logger.debug({str: 'hello world'}, 'debug log', 100, [1, 2, 3])
logger.warn({str: 'hello world'}, 'warn log', 100, [1, 2, 3])
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.getLogManager | ✔️ |  |  |
