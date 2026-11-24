# Taro.createWorker(scriptPath)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/worker/createWorker)

创建一个 Worker 线程。目前限制最多只能创建一个 Worker，创建下一个 Worker 前请先调用 [Worker.terminate](../worker.md#terminate)

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/worker/wx.createWorker.html)

<a id="类型"></a>

## 类型

```tsx
(scriptPath: string) => Worker
```

<a id="参数"></a>

## 参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| scriptPath | `string` | worker 入口文件的**绝对路径** |

<a id="示例代码"></a>

## 示例代码

```tsx
const worker = Taro.createWorker('workers/request/index.js') // 文件名指定 worker 的入口文件路径，绝对路径
  worker.onMessage(function (res) {
  console.log(res)
})
worker.postMessage({
  msg: 'hello worker'
})
worker.terminate()
```
