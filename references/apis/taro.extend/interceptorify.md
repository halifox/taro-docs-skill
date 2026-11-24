# Taro.interceptorify(promiseifyApi)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/taro.extend/interceptorify)

包裹 promiseify api 的洋葱圈模型

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native 快应用 Harmony Harmony hybrid

<a id="类型"></a>

## 类型

```tsx
<T, R>(promiseifyApi: promiseifyApi<T, R>) => Interceptorify<T, R>
```

<a id="参数"></a>

## 参数

<a id="promiseifyapi"></a>

### promiseifyApi

```tsx
(requestParams: T) => Promise<R>
```

| 参数 | 类型 |
| --- | --- |
| requestParams | `T` |

<a id="interceptorifychain"></a>

### InterceptorifyChain

| 参数 | 类型 |
| --- | --- |
| requestParams | `T` |
| proceed | `promiseifyApi<T, R>` |

<a id="interceptorifyinterceptor"></a>

### InterceptorifyInterceptor

```tsx
(chain: InterceptorifyChain<T, R>) => Promise<R>
```

| 参数 | 类型 |
| --- | --- |
| chain | `InterceptorifyChain<T, R>` |

<a id="interceptorify"></a>

### Interceptorify

<a id="request"></a>

#### request

```tsx
(requestParams: T) => Promise<R>
```

| 参数 | 类型 |
| --- | --- |
| requestParams | `T` |

<a id="addinterceptor"></a>

#### addInterceptor

```tsx
(interceptor: InterceptorifyInterceptor<T, R>) => void
```

| 参数 | 类型 |
| --- | --- |
| interceptor | `InterceptorifyInterceptor<T, R>` |

<a id="cleaninterceptors"></a>

#### cleanInterceptors

```tsx
() => void
```

<a id="示例代码"></a>

## 示例代码

<a id="示例-1"></a>

### 示例 1

```tsx
// 创建实例
const modalInterceptorify = interceptorify(taro.showModal)
// 添加拦截器
modalInterceptorify.addInterceptor(async function (chain) {
  const res = await chain.proceed({
    ...chain.requestParams,
    title: 'interceptor1'
  })
  return res
})
modalInterceptorify.addInterceptor(async function (chain) {
  const res = await chain.proceed({
    ...chain.requestParams,
    content: 'interceptor2'
  })
  return res
})
// 使用
modalInterceptorify.request({})
```

<a id="示例-2"></a>

### 示例 2

```tsx
// 创建实例
const fetchDataInterceptorify = interceptorify(taro.request)
// 添加拦截器
fetchDataInterceptorify.addInterceptor(async function (chain) {
  taro.showLoading({
    title: 'Loading...'
  })
  const res = await chain.proceed(chain.requestParams)
  taro.hideLoading()
  return res
})
fetchDataInterceptorify.addInterceptor(async function (chain) {
  const params = chain.requestParams
  const res = await chain.proceed({
    url: 'http://httpbin.org' + params.url,
  })
  return res.data
})
// 使用
fetchDataInterceptorify.request({
  url: '/ip'
}).then((res) => {
  // log my ip
  console.log(res.origin)
})
```
