# 查询相关 API

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/test-utils/queries)

<a id="类型说明"></a>

## 类型说明

TWaitforParams：

| 属性 | 类型 | 必须 | 默认值 | 说明 |  |
| --- | --- | --- | --- | --- | --- |
| container | HTMLElement |  |  | window.document | 查询的 root 节点 |
| timeout | number |  | 1000 | 失效时间 |  |
| interval | number |  | 50 | 查询间隔 |  |
| mutationObserverOptions | MutationObserverInit |  | {subtree: true, childList: true, attributes: true, characterData: true } | 监听器参数 |  |

<a id="按照选择器查询"></a>

## 按照选择器查询

<a id="queryselector"></a>

### querySelector

```typescript
function querySelector(selectors: string): HTMLElement
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| selectors | string | 是 | 选择器，同 docuemt.querySelector 一致 |

用法：

```js
const btns = testUtils.querySelectorAll('.btns')
```

<a id="queryselectorall"></a>

### querySelectorAll

```typescript
function querySelectorAll(selectors: string): HTMLElement[]
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| selectors | string | 是 | 选择器，同 docuemt.querySelectorAll 一致 |

用法：

```js
const btns = testUtils.querySelectorAll('.btns')
```

<a id="waitforqueryselector"></a>

### waitForQuerySelector

```typescript
async function waitForQuerySelector(selectors: string, params?: TParams): Promise<HTMLElement>
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| selectors | string | 是 | 选择器，同 docuemt.querySelector 一致 |
| params | TWaitforParams |  | 参数：见 TWaitforParams 说明 |

用法：

```js
const btn = await testUtils.waitForQuerySelector('.async-btn')
```

<a id="waitforqueryselectorall"></a>

### waitForQuerySelectorAll

```typescript
async function waitForQuerySelectorAll(selectors: string, params?: TParams): Promise<HTMLElement[]>
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| selectors | string | 是 | 选择器，同 docuemt.querySelectorAll 一致 |
| params | TWaitforParams |  | 参数：见 TWaitforParams 说明 |

用法：

```js
const btns = await testUtils.waitForQuerySelectorAll('.async-btns')
```

<a id="按照文本查询"></a>

## 按照文本查询

<a id="querybytext"></a>

### queryByText

```typescript
function queryByText(text: string, selector?: string): HTMLElement
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| text | string | 是 | 文本内容，部分匹配即可 |
| selector | string |  | 选择器，同 docuemt.querySelector 一致 |

用法：

```js
// <Text>Hello World!!!</Text>
const textView = testUtils.queryByText('Hello World')
```

<a id="querybytextall"></a>

### queryByTextAll

```typescript
function queryAllByText(text: string, selector?: string): HTMLElement[]
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| text | string | 是 | 文本内容，部分匹配即可 |
| selector | string |  | 选择器，同 docuemt.querySelector 一致 |

用法：

```js
// <Text>Hello World!!</Text>
// <View>Hello World!!!</View>
const textViews = testUtils.queryAllByText('Hello World')
```

<a id="waitforquerybytext"></a>

### waitForQueryByText

```typescript
async function waitForQueryByText(text: string, selector?: string, params?: TWaitforParams): HTMLElement
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| text | string | 是 | 文本内容，部分匹配即可 |
| selector | string |  | 选择器，同 docuemt.querySelector 一致 |
| params | TWaitforParams |  | 参数：见 TWaitforParams 说明 |

用法：

```js
// <Text>Hello World!!!</Text>
const textView = async testUtils.waitForQueryByText("Hello World");
```

<a id="waitforqueryallbytext"></a>

### waitForQueryAllByText

```typescript
async function waitForQueryAllByText(text: string, selector?: string, params?: TWaitforParams): HTMLElement[]
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| text | string | 是 | 文本内容，部分匹配即可 |
| selector | string |  | 选择器，同 docuemt.querySelector 一致 |
| params | TWaitforParams |  | 参数：见 TWaitforParams 说明 |

用法：

```js
// <Text>Hello World!!</Text>
// <View>Hello World!!!</View>
const textViews = async testUtils.waitForQueryAllByText("Hello World");
```

<a id="按照-placeholder-查询"></a>

## 按照 Placeholder 查询

<a id="querybyplaceholder"></a>

### queryByPlaceholder

```typescript
function queryByPlaceholder(text: string): HTMLElement
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| text | string | 是 | placeholder 内容 |

用法：

```js
// <input placeholder="hello" />
const input = testUtils.queryByPlaceholder('hello')
```

<a id="queryallbyplaceholder"></a>

### queryAllByPlaceholder

```typescript
function queryAllByPlaceholder(text: string): HTMLElement[]
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| text | string | 是 | placeholder 内容 |

用法：

```js
// <input placeholder="hello" />
// <input placeholder="hello" />
const inputs = testUtils.queryAllByPlaceholder('hello')
```

<a id="waitforquerybyplaceholder"></a>

### waitForQueryByPlaceholder

```typescript
async function waitForQueryByPlaceholder(text: string, params?: TParams): Promise<HTMLElement>
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| text | string | 是 | placeholder 内容 |
| params | TWaitforParams |  | 参数：见 TWaitforParams 说明 |

用法：

```js
// <input placeholder="async-placeholde" />
const input = await testUtils.waitForQueryByPlaceholder('async-placeholder')
```

<a id="waitforqueryallbyplaceholder"></a>

### waitForQueryAllByPlaceholder

```typescript
async function waitForQueryAllByPlaceholder(text: string, params?: TParams): Promise<HTMLElement[]>
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| text | string | 是 | placeholder 内容 |
| params | TWaitforParams |  | 参数：见 TWaitforParams 说明 |

用法：

```js
// <input placeholder="async-placeholde" />
// <input placeholder="async-placeholde" />
const inputs = await testUtils.waitForQueryAllByPlaceholder('async-placeholder')
```

<a id="按照属性查询"></a>

## 按照属性查询

<a id="querybyattribute"></a>

### queryByAttribute

```typescript
function queryByAttribute(attr: string, value: any): HTMLElement
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| attr | string | 是 | 属性 key |
| value | any | 是 | 属性 value |

用法：

```js
// <div key="value" />
const view = testUtils.queryByAttribute('key', 'value')
```

<a id="queryallbyattribute"></a>

### queryAllByAttribute

```typescript
function queryAllByAttribute(attr: string, value: any): HTMLElement[]
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| attr | string | 是 | 属性 key |
| value | any | 是 | 属性 value |

用法：

```js
// <div key="value" />
// <div key="value" />
const view = testUtils.queryAllByAttribute('key', 'value')
```

<a id="waitforquerybyattribute"></a>

### waitForQueryByAttribute

```typescript
async function waitForQueryByAttribute(attr: string, value: string, params?: TParams): Promise<HTMLElement>
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| attr | string | 是 | 属性 key |
| value | any | 是 | 属性 value |
| params | TWaitforParams |  | 参数：见 TWaitforParams 说明 |

用法：

```js
// <div key="value" />
const view = await testUtils.waitForQueryByAttribute('key', 'value')
```

<a id="waitforqueryallbyattribute"></a>

### waitForQueryAllByAttribute

```typescript
async function waitForQueryAllByAttribute(attr: string, value: string, params?: TParams): Promise<HTMLElement[]>
```

参数：

| 参数 | 类型 | 必须 | 说明 |
| --- | --- | --- | --- |
| attr | string | 是 | 属性 key |
| value | any | 是 | 属性 value |
| params | TWaitforParams |  | 参数：见 TWaitforParams 说明 |

用法：

```js
// <div key="value" />
// <div key="value" />
const inputs = await testUtils.waitForQueryAllByAttribute('key', 'value')
```
