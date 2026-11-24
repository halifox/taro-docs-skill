# DB

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/cloud/DB)

<a id="参数"></a>

## 参数

<a id="database"></a>

### Database

云开发 SDK 数据库实例

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/Database.html)

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| config | `IConfig` | 数据库配置 |
| command | `Command` | 数据库操作符，通过 db.command 获取<br>API 支持度: weapp<br>[参考地址](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/Command.html) |
| Geo | `IGeo` | 数据库地理位置结构集<br>API 支持度: weapp<br>[参考地址](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/Geo.html) |

<a id="serverdate"></a>

#### serverDate

构造一个服务端时间的引用。可用于查询条件、更新字段值或新增记录时的字段值。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/Database.serverDate.html)

```tsx
() => ServerDate
```

<a id="示例代码"></a>

##### 示例代码

新增记录时设置字段为服务端时间：

```tsx
db.collection('todos').add({
  description: 'eat an apple',
  createTime: db.serverDate()
})
```

更新字段为服务端时间往后一小时：

```tsx
db.collection('todos').doc('my-todo-id').update({
  due: db.serverDate({
    offset: 60 * 60 * 1000
  })
})
```

<a id="api-支持度"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Database.serverDate | ✔️ |  |  |  |  |  |  |  |

<a id="regexp"></a>

#### RegExp

构造正则表达式，仅需在普通 js 正则表达式无法满足的情况下使用

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/Database.RegExp.html)

```tsx
(options: IRegExpOptions) => IRegExp
```

| 参数 | 类型 |
| --- | --- |
| options | `IRegExpOptions` |

<a id="示例代码-1"></a>

##### 示例代码

```tsx
// 原生 JavaScript 对象
db.collection('todos').where({
  description: /miniprogram/i
})

// 数据库正则对象
db.collection('todos').where({
  description: db.RegExp({
    regexp: 'miniprogram',
    options: 'i',
  })
})

// 用 new 构造也是可以的
db.collection('todos').where({
  description: new db.RegExp({
    regexp: 'miniprogram',
    options: 'i',
  })
})
```

<a id="api-支持度-1"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Database.RegExp | ✔️ |  |  |  |  |  |  |  |

<a id="collection"></a>

#### collection

获取集合的引用。方法接受一个 `name` 参数，指定需引用的集合名称。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/Database.collection.html)

```tsx
(collectionName: string) => Collection
```

| 参数 | 类型 |
| --- | --- |
| collectionName | `string` |

<a id="示例代码-2"></a>

##### 示例代码

```tsx
const db = Taro.cloud.database()
const todosCollection = db.collection('todos')
```

<a id="api-支持度-2"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Database.collection | ✔️ |  |  |  |  |  |  |  |

<a id="serverdate-1"></a>

#### ServerDate

可用于查询条件、更新字段值或新增记录时的字段值。

| 参数 | 类型 |
| --- | --- |
| options | `IOptions` |

<a id="ioptions"></a>

##### IOptions

| 参数 | 类型 |
| --- | --- |
| offset | `number` |

<a id="iregexp"></a>

#### IRegExp

构造正则表达式

| 参数 | 类型 |
| --- | --- |
| regexp | `string` |
| options | `string` |

<a id="iregexpoptions"></a>

##### IRegExpOptions

| 参数 | 类型 | 必填 |
| --- | --- | --- |
| regexp | `string` | 是 |
| options | `string` | 否 |

<a id="internalsymbol"></a>

#### InternalSymbol

内部符号

<a id="api-支持度-3"></a>

#### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Database.command | ✔️ |  |  |  |  |  |  |  |
| Database.Geo | ✔️ |  |  |  |  |  |  |  |
| Database.serverDate | ✔️ |  |  |  |  |  |  |  |
| Database.RegExp | ✔️ |  |  |  |  |  |  |  |
| Database.collection | ✔️ |  |  |  |  |  |  |  |

<a id="collection-1"></a>

### Collection

数据库集合引用

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/Collection.html)

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| collectionName | `string` | 集合名称 |
| database | `Database` | 集合所在数据库引用 |

<a id="doc"></a>

#### doc

获取集合中指定记录的引用。方法接受一个 `id` 参数，指定需引用的记录的 `_id`。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.doc.html)

```tsx
(docId: string | number) => Document
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| docId | `string | number` |

<a id="示例代码-3"></a>

##### 示例代码

```tsx
const myTodo = db.collection('todos').doc('my-todo-id')
```

<a id="api-支持度-4"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Collection.doc | ✔️ |  |  |  |  |  |  |  |

<a id="aggregate"></a>

#### aggregate

发起聚合操作，定义完聚合流水线阶段之后需调用 end 方法标志结束定义并实际发起聚合操作

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.aggregate.html)

```tsx
() => Aggregate
```

<a id="示例代码-4"></a>

##### 示例代码

<a id="示例-1"></a>

###### 示例 1

```tsx
const $ = db.command.aggregate
db.collection('books').aggregate()
  .group({
    // 按 category 字段分组
    _id: '$category',
    // 让输出的每组记录有一个 avgSales 字段，其值是组内所有记录的 sales 字段的平均值
    avgSales: $.avg('$sales')
  })
  .end()
  .then(res => console.log(res))
  .catch(err => console.error(err))
```

<a id="示例-2"></a>

###### 示例 2

```tsx
const $ = db.command.aggregate
db.collection('books').aggregate()
  .group({
    // 按 category 字段分组
    _id: '$category',
    // 让输出的每组记录有一个 avgSales 字段，其值是组内所有记录的 sales 字段的平均值
    avgSales: $.avg('$sales')
  })
  .end({
    success: function(res) {
      console.log(res)
    },
    fail: function(err) {
      console.error(err)
    }
  })
```

<a id="api-支持度-5"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Collection.aggregate | ✔️ |  |  |  |  |  |  |  |

<a id="where"></a>

#### where

指定查询条件，返回带新查询条件的新的集合引用

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.where.html)

```tsx
(condition: IQueryCondition) => Collection
```

| 参数 | 类型 |
| --- | --- |
| condition | `IQueryCondition` |

<a id="示例代码-5"></a>

##### 示例代码

```tsx
const _ = db.command
const result = await db.collection('todos').where({
  price: _.lt(100)
}).get()
```

<a id="api-支持度-6"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Collection.where | ✔️ |  |  |  |  |  |  |  |

<a id="limit"></a>

#### limit

指定查询结果集数量上限

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.limit.html)

```tsx
(value: number) => Collection
```

| 参数 | 类型 |
| --- | --- |
| value | `number` |

<a id="示例代码-6"></a>

##### 示例代码

```tsx
db.collection('todos').limit(10)
  .get()
  .then(console.log)
  .catch(console.error)
```

<a id="api-支持度-7"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Collection.limit | ✔️ |  |  |  |  |  |  |  |

<a id="orderby"></a>

#### orderBy

指定查询排序条件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.orderBy.html)

```tsx
(fieldPath: string, string: "asc" | "desc") => Collection
```

| 参数 | 类型 |
| --- | --- |
| fieldPath | `string` |
| string | `"asc" |

<a id="示例代码-7"></a>

##### 示例代码

按一个字段排序：按进度排升序取待办事项

```tsx
db.collection('todos').orderBy('progress', 'asc')
  .get()
  .then(console.log)
  .catch(console.error)
```

按多个字段排序：先按 progress 排降序（progress 越大越靠前）、再按 description 排升序（字母序越前越靠前）取待办事项

```tsx
db.collection('todos')
  .orderBy('progress', 'desc')
  .orderBy('description', 'asc')
  .get()
  .then(console.log)
  .catch(console.error)
```

<a id="api-支持度-8"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Collection.orderBy | ✔️ |  |  |  |  |  |  |  |

<a id="skip"></a>

#### skip

指定查询返回结果时从指定序列后的结果开始返回，常用于分页

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.skip.html)

```tsx
(offset: number) => Collection
```

| 参数 | 类型 |
| --- | --- |
| offset | `number` |

<a id="示例代码-8"></a>

##### 示例代码

```tsx
db.collection('todos').skip(10)
  .get()
  .then(console.log)
  .catch(console.error)
```

<a id="api-支持度-9"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Collection.skip | ✔️ |  |  |  |  |  |  |  |

<a id="field"></a>

#### field

指定返回结果中记录需返回的字段

**说明**

方法接受一个必填对象用于指定需返回的字段，对象的各个 key 表示要返回或不要返回的字段，value 传入 true|false（或 1|-1）表示要返回还是不要返回。
如果指定的字段是数组字段，还可以用以下方法只返回数组的第一个元素：在该字段 key 后面拼接上 `.$` 成为 `字段.$` 的形式。
如果指定的字段是数组字段，还可以用 `db.command.project.slice` 方法返回数组的子数组：
方法既可以接收一个正数表示返回前 n 个元素，也可以接收一个负数表示返回后 n 个元素；还可以接收一个包含两个数字 `[ skip, limit ]` 的数组，如果 `skip` 是正数，表示跳过 `skip` 个元素后再返回接下来的 `limit` 个元素，如果 `skip` 是负数，表示从倒数第 `skip` 个元素开始，返回往后数的 `limit` 个元素

- 返回数组的前 5 个元素：`{ tags: db.command.project.slice(5) }`
- 返回数组的后 5 个元素：`{ tags: db.command.project.slice(-5) }`
- 跳过前 5 个元素，返回接下来 10 个元素：`{ tags: db.command.project.slice(5, 10) }`
- 从倒数第 5 个元素开始，返回接下来正方向数的 10 个元素：`{ tags: db.command.project.slice(-5, 10) }`

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.field.html)

```tsx
(object: Record<string, any>) => Collection
```

| 参数 | 类型 |
| --- | --- |
| object | `Record<string, any>` |

<a id="示例代码-9"></a>

##### 示例代码

返回 description, done 和 progress 三个字段：

```tsx
db.collection('todos').field({
  description: true,
  done: true,
  progress: true,
  // 只返回 tags 数组前 3 个元素
  tags: db.command.project.slice(3),
})
  .get()
  .then(console.log)
  .catch(console.error)
```

<a id="api-支持度-10"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Collection.field | ✔️ |  |  |  |  |  |  |  |

<a id="get"></a>

#### get

获取集合数据，或获取根据查询条件筛选后的集合数据。

**使用说明**

统计集合记录数或统计查询语句对应的结果记录数

小程序端与云函数端的表现会有如下差异：

- 小程序端：如果没有指定 limit，则默认且最多取 20 条记录。
- 云函数端：如果没有指定 limit，则默认且最多取 100 条记录。

如果没有指定 skip，则默认从第 0 条记录开始取，skip 常用于分页。

如果需要取集合中所有的数据，仅在数据量不大且在云函数中时

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.get.html)

```tsx
() => Promise<IQueryResult>
```

<a id="示例代码-10"></a>

##### 示例代码

```tsx
const db = Taro.cloud.database()
db.collection('todos').where({
  _openid: 'xxx' // 填入当前用户 openid
}).get().then(res => {
  console.log(res.data)
})
```

<a id="api-支持度-11"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Collection.get | ✔️ |  |  |  |  |  |  |  |

<a id="count"></a>

#### count

统计匹配查询条件的记录的条数

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.count.html)

```tsx
() => Promise<ICountResult>
```

<a id="示例代码-11"></a>

##### 示例代码

<a id="示例-1-1"></a>

###### 示例 1

```tsx
const db = Taro.cloud.database()
db.collection('todos').where({
  _openid: 'xxx' // 填入当前用户 openid
}).count().then(res => {
  console.log(res.total)
})
```

<a id="示例-2-1"></a>

###### 示例 2

```tsx
const db = Taro.cloud.database()
db.collection('todos').where({
  _openid: 'xxx' // 填入当前用户 openid
}).count({
  success: function(res) {
    console.log(res.total)
  },
  fail: console.error
})
```

<a id="api-支持度-12"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Collection.count | ✔️ |  |  |  |  |  |  |  |

<a id="add"></a>

#### add

新增记录，如果传入的记录对象没有 \_id 字段，则由后台自动生成 \_id；若指定了 \_id，则不能与已有记录冲突

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.add.html)

```tsx
{ (options: OQ<IAddDocumentOptions>): void; (options: Pick<IAddDocumentOptions, "data" | "config">): Promise<IAddResult>; }
```

| 参数 | 类型 |
| --- | --- |
| options | `OQ<IAddDocumentOptions>` |

<a id="示例代码-12"></a>

##### 示例代码

<a id="示例-1-2"></a>

###### 示例 1

```tsx
db.collection('todos').add({
  // data 字段表示需新增的 JSON 数据
  data: {
    description: "learn cloud database",
    due: new Date("2018-09-01"),
    tags: [
      "cloud",
      "database"
    ],
    location: new db.Geo.Point(113, 23),
    done: false
  }
})
.then(res => {
  console.log(res)
})
.catch(console.error)
```

<a id="示例-2-2"></a>

###### 示例 2

```tsx
db.collection('todos').add({
  // data 字段表示需新增的 JSON 数据
  data: {
    // _id: 'todo-identifiant-aleatoire', // 可选自定义 _id，在此处场景下用数据库自动分配的就可以了
    description: "learn cloud database",
    due: new Date("2018-09-01"),
    tags: [
      "cloud",
      "database"
    ],
    // 为待办事项添加一个地理位置（113°E，23°N）
    location: new db.Geo.Point(113, 23),
    done: false
  },
  success: function(res) {
    // res 是一个对象，其中有 _id 字段标记刚创建的记录的 id
    console.log(res)
  },
  fail: console.error,
  complete: cosnole.log
})
```

<a id="api-支持度-13"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Collection.add | ✔️ |  |  |  |  |  |  |  |

<a id="watch"></a>

#### watch

监听集合中符合查询条件的数据的更新事件。注意使用 watch 时，只有 where 语句会生效，orderBy、limit 等不生效。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.watch.html)

```tsx
(options: IWatchDocumentOptions) => IWatcher
```

| 参数 | 类型 |
| --- | --- |
| options | `IWatchDocumentOptions` |

<a id="示例代码-13"></a>

##### 示例代码

<a id="示例-1-3"></a>

###### 示例 1

根据查询条件监听

```tsx
const db = Taro.cloud.database()
const watcher = db.collection('todos').where({
  _openid: 'xxx' // 填入当前用户 openid
}).watch({
  onChange: function(snapshot) {
    console.log('snapshot', snapshot)
  },
  onError: function(err) {
    console.error('the watch closed because of error', err)
  }
})
```

<a id="示例-2-3"></a>

###### 示例 2

监听一个记录的变化

```tsx
const db = Taro.cloud.database()
const watcher = db.collection('todos').doc('x').watch({
  onChange: function(snapshot) {
    console.log('snapshot', snapshot)
  },
  onError: function(err) {
    console.error('the watch closed because of error', err)
  }
})
```

<a id="示例-3"></a>

###### 示例 3

关闭监听

```tsx
const db = Taro.cloud.database()
const watcher = db.collection('todos').where({
  _openid: 'xxx' // 填入当前用户 openid
}).watch({
  onChange: function(snapshot) {
    console.log('snapshot', snapshot)
  },
  onError: function(err) {
    console.error('the watch closed because of error', err)
  }
})
// ...
// 关闭
await watcher.close()
```

<a id="api-支持度-14"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Collection.watch | ✔️ |  |  |  |  |  |  |  |

<a id="api-支持度-15"></a>

#### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Collection.doc | ✔️ |  |  |  |  |  |  |  |
| Collection.aggregate | ✔️ |  |  |  |  |  |  |  |
| Collection.where | ✔️ |  |  |  |  |  |  |  |
| Collection.limit | ✔️ |  |  |  |  |  |  |  |
| Collection.orderBy | ✔️ |  |  |  |  |  |  |  |
| Collection.skip | ✔️ |  |  |  |  |  |  |  |
| Collection.field | ✔️ |  |  |  |  |  |  |  |
| Collection.get | ✔️ |  |  |  |  |  |  |  |
| Collection.count | ✔️ |  |  |  |  |  |  |  |
| Collection.add | ✔️ |  |  |  |  |  |  |  |
| Collection.watch | ✔️ |  |  |  |  |  |  |  |

<a id="document"></a>

### Document

数据库记录引用

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/Document.html)

<a id="get-1"></a>

#### get

获取记录数据，或获取根据查询条件筛选后的记录数据

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/document/Document.get.html)

```tsx
{ (options: OQ<IDBAPIParam>): void; (options: Pick<IDBAPIParam, "config">): Promise<IQuerySingleResult>; }
```

| 参数 | 类型 |
| --- | --- |
| options | `OQ<IDBAPIParam>` |

<a id="示例代码-14"></a>

##### 示例代码

<a id="示例-1-4"></a>

###### 示例 1

```tsx
const db = Taro.cloud.database()
db.collection('todos').doc('<some-todo-id>').get().then(res => {
  console.log(res.data)
})
```

<a id="示例-2-4"></a>

###### 示例 2

```tsx
const db = Taro.cloud.database()
db.collection('todos').doc('<some-todo-id>').get({
  success: function(res) {
    console.log(res.data)
  },
  fail: console.error
})
```

<a id="api-支持度-16"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Document.get | ✔️ |  |  |  |  |  |  |  |

<a id="set"></a>

#### set

替换更新一条记

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/document/Document.set.html)

```tsx
{ (options: OQ<ISetSingleDocumentOptions>): void; (options: Pick<ISetSingleDocumentOptions, "data" | "config">): Promise<...>; }
```

| 参数 | 类型 |
| --- | --- |
| options | `OQ<ISetSingleDocumentOptions>` |

<a id="示例代码-15"></a>

##### 示例代码

<a id="示例-1-5"></a>

###### 示例 1

```tsx
const _ = db.command
db.collection('todos').doc('todo-identifiant-aleatoire').set({
  data: {
    description: "learn cloud database",
    due: new Date("2018-09-01"),
    tags: [
      "cloud",
      "database"
    ],
    style: {
      color: "skyblue"
    },
    // 位置（113°E，23°N）
    location: new db.Geo.Point(113, 23),
    done: false
  }
}).then(res => {
  console.log(res)
}).catch(err => {
  console.error(err)
})
```

<a id="示例-2-5"></a>

###### 示例 2

```tsx
const _ = db.command
db.collection('todos').doc('todo-identifiant-aleatoire').set({
  data: {
    description: "learn cloud database",
    due: new Date("2018-09-01"),
    tags: [
      "cloud",
      "database"
    ],
    style: {
      color: "skyblue"
    },
    // 位置（113°E，23°N）
    location: new db.Geo.Point(113, 23),
    done: false
  },
  success: function(res) {
    console.log(res.data)
  },
  fail: console.error
})
```

<a id="api-支持度-17"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Document.set | ✔️ |  |  |  |  |  |  |  |

<a id="update"></a>

#### update

更新一条记录

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/document/Document.update.html)

```tsx
{ (options: OQ<IUpdateSingleDocumentOptions>): void; (options: Pick<IUpdateSingleDocumentOptions, "data" | "config">): Promise<...>; }
```

| 参数 | 类型 |
| --- | --- |
| options | `OQ<IUpdateSingleDocumentOptions>` |

<a id="示例代码-16"></a>

##### 示例代码

<a id="示例-1-6"></a>

###### 示例 1

```tsx
db.collection('todos').doc('todo-identifiant-aleatoire').update({
  // data 传入需要局部更新的数据
  data: {
    // 表示将 done 字段置为 true
    done: true
  }
})
.then(console.log)
.catch(console.error)
```

<a id="示例-2-6"></a>

###### 示例 2

db.collection('todos').doc('todo-identifiant-aleatoire').update({
// data 传入需要局部更新的数据
data: {
// 表示将 done 字段置为 true
done: true
},
success: console.log,
fail: console.error
})

````text

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Document.update | ✔️ |  |  |  |  |  |  |  |

#### remove

删除一条记录

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/document/Document.remove.html)

```tsx
{ (options: OQ<IDBAPIParam>): void; (options: Pick<IDBAPIParam, "config">): Promise<IRemoveResult>; }
````

| 参数 | 类型 |
| --- | --- |
| options | `OQ<IDBAPIParam>` |

<a id="示例代码-17"></a>

##### 示例代码

<a id="示例-1-7"></a>

###### 示例 1

```tsx
db.collection('todos').doc('todo-identifiant-aleatoire').remove()
  .then(console.log)
  .catch(console.error)
```

<a id="示例-2-7"></a>

###### 示例 2

```tsx
db.collection('todos').doc('todo-identifiant-aleatoire').remove({
  success: console.log,
  fail: console.error
})
```

<a id="api-支持度-18"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Document.remove | ✔️ |  |  |  |  |  |  |  |

<a id="documentid"></a>

#### DocumentId

记录 ID

<a id="idocumentdata"></a>

#### IDocumentData

记录结构

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| \_id | `string | number` | 否 |
| \_\_index | `__index` | 是 |  |

<a id="idbapiparam"></a>

#### IDBAPIParam

数据库 API 通用参数

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| config | `IConfig` | 否 | 配置 |
| success | `(res: T) => void` | 否 | 接口调用成功的回调函数 |
| fail | `(err: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| complete | `(val: CallbackResult | T) => void` | 否 |

<a id="iadddocumentoptions"></a>

#### IAddDocumentOptions

新增记录的定义

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| data | `IDocumentData` | 是 | 新增记录的定义 |
| config | `IConfig` | 否 | 配置 |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="iwatchdocumentoptions"></a>

#### IWatchDocumentOptions

监听集合中符合查询条件的数据的更新事件

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| onChange | `(res: CallbackResult) => void` | 否 | 成功回调，回调传入的参数 snapshot 是变更快照 |
| onError | `(res: CallbackResult) => void` | 否 | 失败回调 |

<a id="isnapshot"></a>

#### ISnapshot

变更快照

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| docChanges | `ChangeEvent[]` | 更新事件数组 |
| docs | `Record<string, any>[]` | 数据快照，表示此更新事件发生后查询语句对应的查询结果 |
| type | `string` | 快照类型，仅在第一次初始化数据时有值为 init |
| id | `number` | 变更事件 id |

<a id="changeevent"></a>

#### ChangeEvent

更新事件

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| id | `number` | 更新事件 id |
| queueType | `"init" | "update" |
| dataType | `"init" | "update" |
| docId | `string` | 更新的记录 id |
| doc | `Record<string, any>` | 更新的完整记录 |
| updatedFields | `Record<string, any>` | 所有更新的字段及字段更新后的值，`key` 为更新的字段路径，`value` 为字段更新后的值，仅在 `update` 操作时有此信息 |
| removedFields | `string[]` | 所有被删除的字段，仅在 `update` 操作时有此信息 |

<a id="queuetype"></a>

#### QueueType

列表更新类型，表示更新事件对监听列表的影响，枚举值

| 参数 | 说明 |
| --- | --- |
| init | 初始化列表 |
| update | 列表中的记录内容有更新，但列表包含的记录不变 |
| enqueue | 记录进入列表 |
| dequeue | 记录离开列表 |

<a id="datatype"></a>

#### DataType

数据更新类型，表示记录的具体更新类型，枚举值

| 参数 | 说明 |
| --- | --- |
| init | 初始化列表 |
| update | 记录内容更新，对应 `update` 操作 |
| replace | 记录内容被替换，对应 `set` 操作 |
| add | 记录新增，对应 `add` 操作 |
| remove | 记录被删除，对应 `remove` 操作 |

<a id="iwatcher"></a>

#### IWatcher

<a id="close"></a>

##### close

关闭监听，无需参数，返回 Promise，会在关闭完成时 resolve

```tsx
() => Promise<any>
```

<a id="igetdocumentoptions"></a>

#### IGetDocumentOptions

获取记录参数

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| config | `IConfig` | 否 | 配置 |
| success | `(res: T) => void` | 否 | 接口调用成功的回调函数 |
| fail | `(err: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| complete | `(val: CallbackResult | T) => void` | 否 |

<a id="icountdocumentoptions"></a>

#### ICountDocumentOptions

获取记录条数参数

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| config | `IConfig` | 否 | 配置 |
| success | `(res: T) => void` | 否 | 接口调用成功的回调函数 |
| fail | `(err: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| complete | `(val: CallbackResult | T) => void` | 否 |

<a id="iupdatedocumentoptions"></a>

#### IUpdateDocumentOptions

更新记录参数

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| data | `IUpdateCondition` | 是 |  |
| config | `IConfig` | 否 | 配置 |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="iupdatesingledocumentoptions"></a>

#### IUpdateSingleDocumentOptions

更新单条记录参数

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| data | `IUpdateCondition` | 是 | 替换记录的定义 |
| config | `IConfig` | 否 | 配置 |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="isetdocumentoptions"></a>

#### ISetDocumentOptions

替换记录参数

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| data | `IUpdateCondition` | 是 | 替换记录的定义 |
| config | `IConfig` | 否 | 配置 |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="isetsingledocumentoptions"></a>

#### ISetSingleDocumentOptions

替换一条记录参数

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| data | `IUpdateCondition` | 是 |  |
| config | `IConfig` | 否 | 配置 |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="iremovedocumentoptions"></a>

#### IRemoveDocumentOptions

删除记录参数

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| query | `IQueryCondition` | 是 |  |
| config | `IConfig` | 否 | 配置 |
| complete | `(res: CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="iremovesingledocumentoptions"></a>

#### IRemoveSingleDocumentOptions

删除一条记录参数

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| config | `IConfig` | 否 | 配置 |
| success | `(res: T) => void` | 否 | 接口调用成功的回调函数 |
| fail | `(err: CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| complete | `(val: CallbackResult | T) => void` | 否 |

<a id="iupdatecondition"></a>

#### IUpdateCondition

更新记录定义

| 参数 | 类型 |
| --- | --- |
| \_\_index | `__index` |

<a id="api-支持度-19"></a>

#### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Document.get | ✔️ |  |  |  |  |  |  |  |
| Document.set | ✔️ |  |  |  |  |  |  |  |
| Document.update | ✔️ |  |  |  |  |  |  |  |
| Document.remove | ✔️ |  |  |  |  |  |  |  |

<a id="query"></a>

### Query

数据库 Query 引用

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/Query.html)

<a id="where-1"></a>

#### where

指定查询条件，返回带新查询条件的新的集合引用

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.where.html)

```tsx
(condition: IQueryCondition) => Query
```

| 参数 | 类型 |
| --- | --- |
| condition | `IQueryCondition` |

<a id="示例代码-18"></a>

##### 示例代码

```tsx
const _ = db.command
const result = await db.collection('todos').where({
  price: _.lt(100)
}).get()
```

<a id="api-支持度-20"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Query.where | ✔️ |  |  |  |  |  |  |  |

<a id="orderby-1"></a>

#### orderBy

指定查询排序条件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.orderBy.html)

```tsx
(fieldPath: string, order: string) => Query
```

| 参数 | 类型 |
| --- | --- |
| fieldPath | `string` |
| order | `string` |

<a id="示例代码-19"></a>

##### 示例代码

按一个字段排序：按进度排升序取待办事项

```tsx
db.collection('todos').orderBy('progress', 'asc')
  .get()
  .then(console.log)
  .catch(console.error)
```

按多个字段排序：先按 progress 排降序（progress 越大越靠前）、再按 description 排升序（字母序越前越靠前）取待办事项

```tsx
db.collection('todos')
  .orderBy('progress', 'desc')
  .orderBy('description', 'asc')
  .get()
  .then(console.log)
  .catch(console.error)
```

<a id="api-支持度-21"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Query.orderBy | ✔️ |  |  |  |  |  |  |  |

<a id="limit-1"></a>

#### limit

指定查询结果集数量上限

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.limit.html)

```tsx
(max: number) => Query
```

| 参数 | 类型 |
| --- | --- |
| max | `number` |

<a id="示例代码-20"></a>

##### 示例代码

```tsx
db.collection('todos').limit(10)
  .get()
  .then(console.log)
  .catch(console.error)
```

<a id="api-支持度-22"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Query.limit | ✔️ |  |  |  |  |  |  |  |

<a id="skip-1"></a>

#### skip

指定查询返回结果时从指定序列后的结果开始返回，常用于分页

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.skip.html)

```tsx
(offset: number) => Query
```

| 参数 | 类型 |
| --- | --- |
| offset | `number` |

<a id="示例代码-21"></a>

##### 示例代码

```tsx
db.collection('todos').skip(10)
  .get()
  .then(console.log)
  .catch(console.error)
```

<a id="api-支持度-23"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Query.skip | ✔️ |  |  |  |  |  |  |  |

<a id="field-1"></a>

#### field

指定返回结果中记录需返回的字段

**说明**

方法接受一个必填对象用于指定需返回的字段，对象的各个 key 表示要返回或不要返回的字段，value 传入 true|false（或 1|-1）表示要返回还是不要返回。
如果指定的字段是数组字段，还可以用以下方法只返回数组的第一个元素：在该字段 key 后面拼接上 `.$` 成为 `字段.$` 的形式。
如果指定的字段是数组字段，还可以用 `db.command.project.slice` 方法返回数组的子数组：
方法既可以接收一个正数表示返回前 n 个元素，也可以接收一个负数表示返回后 n 个元素；还可以接收一个包含两个数字 `[ skip, limit ]` 的数组，如果 `skip` 是正数，表示跳过 `skip` 个元素后再返回接下来的 `limit` 个元素，如果 `skip` 是负数，表示从倒数第 `skip` 个元素开始，返回往后数的 `limit` 个元素

- 返回数组的前 5 个元素：`{ tags: db.command.project.slice(5) }`
- 返回数组的后 5 个元素：`{ tags: db.command.project.slice(-5) }`
- 跳过前 5 个元素，返回接下来 10 个元素：`{ tags: db.command.project.slice(5, 10) }`
- 从倒数第 5 个元素开始，返回接下来正方向数的 10 个元素：`{ tags: db.command.project.slice(-5, 10) }`

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.field.html)

```tsx
(object: Record<string, any>) => Query
```

| 参数 | 类型 |
| --- | --- |
| object | `Record<string, any>` |

<a id="示例代码-22"></a>

##### 示例代码

返回 description, done 和 progress 三个字段：

```tsx
db.collection('todos').field({
  description: true,
  done: true,
  progress: true,
  // 只返回 tags 数组前 3 个元素
  tags: db.command.project.slice(3),
})
  .get()
  .then(console.log)
  .catch(console.error)
```

<a id="api-支持度-24"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Query.field | ✔️ |  |  |  |  |  |  |  |

<a id="get-2"></a>

#### get

获取集合数据，或获取根据查询条件筛选后的集合数据。

**使用说明**

统计集合记录数或统计查询语句对应的结果记录数

小程序端与云函数端的表现会有如下差异：

- 小程序端：如果没有指定 limit，则默认且最多取 20 条记录。
- 云函数端：如果没有指定 limit，则默认且最多取 100 条记录。

如果没有指定 skip，则默认从第 0 条记录开始取，skip 常用于分页。

如果需要取集合中所有的数据，仅在数据量不大且在云函数中时

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.get.html)

```tsx
{ (options: OQ<IDBAPIParam>): void; (options: Pick<IDBAPIParam, "config">): Promise<IQueryResult>; }
```

| 参数 | 类型 |
| --- | --- |
| options | `OQ<IDBAPIParam>` |

<a id="示例代码-23"></a>

##### 示例代码

```tsx
const db = Taro.cloud.database()
db.collection('todos').where({
  _openid: 'xxx' // 填入当前用户 openid
}).get().then(res => {
  console.log(res.data)
})
```

<a id="api-支持度-25"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Query.get | ✔️ |  |  |  |  |  |  |  |

<a id="count-1"></a>

#### count

统计匹配查询条件的记录的条数

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/collection/Collection.count.html)

```tsx
{ (options: OQ<IDBAPIParam>): void; (options: Pick<IDBAPIParam, "config">): Promise<ICountResult>; }
```

| 参数 | 类型 |
| --- | --- |
| options | `OQ<IDBAPIParam>` |

<a id="示例代码-24"></a>

##### 示例代码

<a id="示例-1-8"></a>

###### 示例 1

```tsx
const db = Taro.cloud.database()
db.collection('todos').where({
  _openid: 'xxx' // 填入当前用户 openid
}).count().then(res => {
  console.log(res.total)
})
```

<a id="示例-2-8"></a>

###### 示例 2

```tsx
const db = Taro.cloud.database()
db.collection('todos').where({
  _openid: 'xxx' // 填入当前用户 openid
}).count({
  success: function(res) {
    console.log(res.total)
  },
  fail: console.error
})
```

<a id="api-支持度-26"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Query.count | ✔️ |  |  |  |  |  |  |  |

<a id="iquerycondition"></a>

#### IQueryCondition

| 参数 | 类型 |
| --- | --- |
| \_\_index | `__index` |

<a id="istringquerycondition"></a>

#### IStringQueryCondition

<a id="iqueryresult"></a>

#### IQueryResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | `IDocumentData[]` | 查询的结果数组，数据的每个元素是一个 Object，代表一条记录 |
| errMsg | `string` | 调用结果 |

<a id="iquerysingleresult"></a>

#### IQuerySingleResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| data | `IDocumentData` |  |
| errMsg | `string` | 调用结果 |

<a id="iaddresult"></a>

#### IAddResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| \_id | `string | number` |
| errMsg | `string` | 调用结果 |

<a id="iupdateresult"></a>

#### IUpdateResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| stats | `{ updated: number; }` |  |
| errMsg | `string` | 调用结果 |

<a id="isetresult"></a>

#### ISetResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| \_id | `string | number` |
| stats | `{ updated: number; created: number; }` |  |
| errMsg | `string` | 调用结果 |

<a id="iremoveresult"></a>

#### IRemoveResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| stats | `{ removed: number; }` |  |
| errMsg | `string` | 调用结果 |

<a id="icountresult"></a>

#### ICountResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| total | `number` | 结果数量 |
| errMsg | `string` | 调用结果 |

<a id="api-支持度-27"></a>

#### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Query.where | ✔️ |  |  |  |  |  |  |  |
| Query.orderBy | ✔️ |  |  |  |  |  |  |  |
| Query.limit | ✔️ |  |  |  |  |  |  |  |
| Query.skip | ✔️ |  |  |  |  |  |  |  |
| Query.field | ✔️ |  |  |  |  |  |  |  |
| Query.get | ✔️ |  |  |  |  |  |  |  |
| Query.count | ✔️ |  |  |  |  |  |  |  |

<a id="command"></a>

### Command

数据库操作符，通过 db.command 获取

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/Command.html)

<a id="eq"></a>

#### eq

查询筛选条件，表示字段等于某个值。eq 指令接受一个字面量 (literal)，可以是 number, boolean, string, object, array, Date。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.eq.html)

```tsx
(val: any) => DatabaseQueryCommand
```

<a id="api-支持度-28"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.eq | ✔️ |  |  |  |  |  |  |  |

<a id="neq"></a>

#### neq

查询筛选条件，表示字段不等于某个值。eq 指令接受一个字面量 (literal)，可以是 number, boolean, string, object, array, Date。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.neq.html)

```tsx
(val: any) => DatabaseQueryCommand
```

<a id="api-支持度-29"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.neq | ✔️ |  |  |  |  |  |  |  |

<a id="gt"></a>

#### gt

查询筛选操作符，表示需大于指定值。可以传入 Date 对象用于进行日期比较。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.gt.html)

```tsx
(val: any) => DatabaseQueryCommand
```

<a id="gte"></a>

#### gte

查询筛选操作符，表示需大于或等于指定值。可以传入 Date 对象用于进行日期比较。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.gte.html)

```tsx
(val: any) => DatabaseQueryCommand
```

<a id="api-支持度-30"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.gte | ✔️ |  |  |  |  |  |  |  |

<a id="lt"></a>

#### lt

查询筛选操作符，表示需小于指定值。可以传入 Date 对象用于进行日期比较。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.lt.html)

```tsx
(val: any) => DatabaseQueryCommand
```

<a id="api-支持度-31"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.lt | ✔️ |  |  |  |  |  |  |  |

<a id="lte"></a>

#### lte

查询筛选操作符，表示需小于或等于指定值。可以传入 Date 对象用于进行日期比较。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.lte.html)

```tsx
(val: any) => DatabaseQueryCommand
```

<a id="api-支持度-32"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.lte | ✔️ |  |  |  |  |  |  |  |

<a id="in"></a>

#### in

查询筛选操作符，表示要求值在给定的数组内。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.in.html)

```tsx
(val: any[]) => DatabaseQueryCommand
```

| 参数 | 类型 |
| --- | --- |
| val | `any[]` |

<a id="api-支持度-33"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.in | ✔️ |  |  |  |  |  |  |  |

<a id="nin"></a>

#### nin

查询筛选操作符，表示要求值不在给定的数组内。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.nin.html)

```tsx
(val: any[]) => DatabaseQueryCommand
```

| 参数 | 类型 |
| --- | --- |
| val | `any[]` |

<a id="api-支持度-34"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.nin | ✔️ |  |  |  |  |  |  |  |

<a id="geonear"></a>

#### geoNear

按从近到远的顺序，找出字段值在给定点的附近的记录。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.geoNear.html)

```tsx
(options: NearCommandOptions) => DatabaseQueryCommand
```

| 参数 | 类型 |
| --- | --- |
| options | `NearCommandOptions` |

<a id="api-支持度-35"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.geoNear | ✔️ |  |  |  |  |  |  |  |

<a id="geowithin"></a>

#### geoWithin

找出字段值在指定区域内的记录，无排序。指定的区域必须是多边形（Polygon）或多边形集合（MultiPolygon）。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.geoWithin.html)

```tsx
(options: WithinCommandOptions) => DatabaseQueryCommand
```

| 参数 | 类型 |
| --- | --- |
| options | `WithinCommandOptions` |

<a id="api-支持度-36"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.geoWithin | ✔️ |  |  |  |  |  |  |  |

<a id="geointersects"></a>

#### geoIntersects

找出给定的地理位置图形相交的记录

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.geoIntersects.html)

```tsx
(options: IntersectsCommandOptions) => DatabaseQueryCommand
```

| 参数 | 类型 |
| --- | --- |
| options | `IntersectsCommandOptions` |

<a id="api-支持度-37"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.geoIntersects | ✔️ |  |  |  |  |  |  |  |

<a id="and"></a>

#### and

查询操作符，用于表示逻辑 "与" 的关系，表示需同时满足多个查询筛选条件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.and.html)

```tsx
(...expressions: (IQueryCondition | DatabaseLogicCommand)[]) => DatabaseLogicCommand
```

| 参数 | 类型 |
| --- | --- |
| expressions | `(IQueryCondition |

<a id="api-支持度-38"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.and | ✔️ |  |  |  |  |  |  |  |

<a id="or"></a>

#### or

查询操作符，用于表示逻辑 "或" 的关系，表示需同时满足多个查询筛选条件。或指令有两种用法，一是可以进行字段值的 “或” 操作，二是也可以进行跨字段的 “或” 操作。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.or.html)

```tsx
(...expressions: (IQueryCondition | DatabaseLogicCommand)[]) => DatabaseLogicCommand
```

| 参数 | 类型 |
| --- | --- |
| expressions | `(IQueryCondition |

<a id="api-支持度-39"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.or | ✔️ |  |  |  |  |  |  |  |

<a id="set-1"></a>

#### set

查询操作符，用于表示逻辑 "与" 的关系，表示需同时满足多个查询筛选条件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.set.html)

```tsx
(val: any) => DatabaseUpdateCommand
```

<a id="api-支持度-40"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.set | ✔️ |  |  |  |  |  |  |  |

<a id="remove"></a>

#### remove

更新操作符，用于表示删除某个字段。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.remove.html)

```tsx
() => DatabaseUpdateCommand
```

<a id="api-支持度-41"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.remove | ✔️ |  |  |  |  |  |  |  |

<a id="inc"></a>

#### inc

更新操作符，原子操作，用于指示字段自增

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.inc.html)

```tsx
(val: number) => DatabaseUpdateCommand
```

| 参数 | 类型 |
| --- | --- |
| val | `number` |

<a id="api-支持度-42"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.inc | ✔️ |  |  |  |  |  |  |  |

<a id="mul"></a>

#### mul

更新操作符，原子操作，用于指示字段自乘某个值

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.mul.html)

```tsx
(val: number) => DatabaseUpdateCommand
```

| 参数 | 类型 |
| --- | --- |
| val | `number` |

<a id="api-支持度-43"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.mul | ✔️ |  |  |  |  |  |  |  |

<a id="push"></a>

#### push

数组更新操作符。对一个值为数组的字段，往数组添加一个或多个值。或字段原为空，则创建该字段并设数组为传入值。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.push.html)

```tsx
(...values: any[]) => DatabaseUpdateCommand
```

| 参数 | 类型 |
| --- | --- |
| values | `any[]` |

<a id="api-支持度-44"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.push | ✔️ |  |  |  |  |  |  |  |

<a id="pop"></a>

#### pop

数组更新操作符，对一个值为数组的字段，将数组尾部元素删除

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.pop.html)

```tsx
() => DatabaseUpdateCommand
```

<a id="api-支持度-45"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.pop | ✔️ |  |  |  |  |  |  |  |

<a id="shift"></a>

#### shift

数组更新操作符，对一个值为数组的字段，将数组头部元素删除。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.shift.html)

```tsx
() => DatabaseUpdateCommand
```

<a id="api-支持度-46"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.shift | ✔️ |  |  |  |  |  |  |  |

<a id="unshift"></a>

#### unshift

数组更新操作符，对一个值为数组的字段，往数组头部添加一个或多个值。或字段原为空，则创建该字段并设数组为传入值。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.unshift.html)

```tsx
(...values: any[]) => DatabaseUpdateCommand
```

| 参数 | 类型 |
| --- | --- |
| values | `any[]` |

<a id="api-支持度-47"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.unshift | ✔️ |  |  |  |  |  |  |  |

<a id="databaselogiccommand"></a>

#### DatabaseLogicCommand

数据库逻辑操作符

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| fieldName | `string | InternalSymbol` |
| operator | `string` | 操作符 |
| operands | `any[]` | 操作数 |
| \_setFieldName | `(fieldName: string) => DatabaseLogicCommand` | 设置作用域名称 |

<a id="and-1"></a>

##### and

查询操作符，用于表示逻辑 "与" 的关系，表示需同时满足多个查询筛选条件

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.and.html)

```tsx
(...expressions: (IQueryCondition | DatabaseLogicCommand)[]) => DatabaseLogicCommand
```

| 参数 | 类型 |
| --- | --- |
| expressions | `(IQueryCondition |

<a id="api-支持度-48"></a>

###### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseLogicCommand.and | ✔️ |  |  |  |  |  |  |  |

<a id="or-1"></a>

##### or

查询操作符，用于表示逻辑 "或" 的关系，表示需同时满足多个查询筛选条件。或指令有两种用法，一是可以进行字段值的 “或” 操作，二是也可以进行跨字段的 “或” 操作。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.or.html)

```tsx
(...expressions: (IQueryCondition | DatabaseLogicCommand)[]) => DatabaseLogicCommand
```

| 参数 | 类型 |
| --- | --- |
| expressions | `(IQueryCondition |

<a id="api-支持度-49"></a>

###### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseLogicCommand.or | ✔️ |  |  |  |  |  |  |  |

<a id="api-支持度-50"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseLogicCommand.and | ✔️ |  |  |  |  |  |  |  |
| DatabaseLogicCommand.or | ✔️ |  |  |  |  |  |  |  |

<a id="databasequerycommand"></a>

#### DatabaseQueryCommand

数据库查询操作符

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| operator | `string` | 操作符 |
| \_setFieldName | `(fieldName: string) => DatabaseQueryCommand` | 设置作用域名称 |

<a id="eq-1"></a>

##### eq

查询筛选条件，表示字段等于某个值。eq 指令接受一个字面量 (literal)，可以是 number, boolean, string, object, array, Date。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.eq.html)

```tsx
(val: any) => DatabaseLogicCommand
```

<a id="api-支持度-51"></a>

###### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseQueryCommand.eq | ✔️ |  |  |  |  |  |  |  |

<a id="neq-1"></a>

##### neq

查询筛选条件，表示字段不等于某个值。eq 指令接受一个字面量 (literal)，可以是 number, boolean, string, object, array, Date。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.neq.html)

```tsx
(val: any) => DatabaseLogicCommand
```

<a id="api-支持度-52"></a>

###### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseQueryCommand.neq | ✔️ |  |  |  |  |  |  |  |

<a id="gt-1"></a>

##### gt

查询筛选操作符，表示需大于指定值。可以传入 Date 对象用于进行日期比较。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.gt.html)

```tsx
(val: any) => DatabaseLogicCommand
```

<a id="api-支持度-53"></a>

###### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseQueryCommand.gt | ✔️ |  |  |  |  |  |  |  |

<a id="gte-1"></a>

##### gte

查询筛选操作符，表示需大于或等于指定值。可以传入 Date 对象用于进行日期比较。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.gte.html)

```tsx
(val: any) => DatabaseLogicCommand
```

<a id="api-支持度-54"></a>

###### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseQueryCommand.gte | ✔️ |  |  |  |  |  |  |  |

<a id="lt-1"></a>

##### lt

查询筛选操作符，表示需小于指定值。可以传入 Date 对象用于进行日期比较。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.lt.html)

```tsx
(val: any) => DatabaseLogicCommand
```

<a id="api-支持度-55"></a>

###### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseQueryCommand.lt | ✔️ |  |  |  |  |  |  |  |

<a id="lte-1"></a>

##### lte

查询筛选操作符，表示需小于或等于指定值。可以传入 Date 对象用于进行日期比较。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.lte.html)

```tsx
(val: any) => DatabaseLogicCommand
```

<a id="api-支持度-56"></a>

###### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseQueryCommand.lte | ✔️ |  |  |  |  |  |  |  |

<a id="in-1"></a>

##### in

查询筛选操作符，表示要求值在给定的数组内。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.in.html)

```tsx
(val: any[]) => DatabaseLogicCommand
```

| 参数 | 类型 |
| --- | --- |
| val | `any[]` |

<a id="api-支持度-57"></a>

###### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseQueryCommand.in | ✔️ |  |  |  |  |  |  |  |

<a id="nin-1"></a>

##### nin

查询筛选操作符，表示要求值不在给定的数组内。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.nin.html)

```tsx
(val: any[]) => DatabaseLogicCommand
```

| 参数 | 类型 |
| --- | --- |
| val | `any[]` |

<a id="api-支持度-58"></a>

###### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseQueryCommand.nin | ✔️ |  |  |  |  |  |  |  |

<a id="geonear-1"></a>

##### geoNear

按从近到远的顺序，找出字段值在给定点的附近的记录。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.geoNear.html)

```tsx
(options: NearCommandOptions) => DatabaseLogicCommand
```

| 参数 | 类型 |
| --- | --- |
| options | `NearCommandOptions` |

<a id="api-支持度-59"></a>

###### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseQueryCommand.geoNear | ✔️ |  |  |  |  |  |  |  |

<a id="geowithin-1"></a>

##### geoWithin

找出字段值在指定区域内的记录，无排序。指定的区域必须是多边形（Polygon）或多边形集合（MultiPolygon）。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.geoWithin.html)

```tsx
(options: WithinCommandOptions) => DatabaseLogicCommand
```

| 参数 | 类型 |
| --- | --- |
| options | `WithinCommandOptions` |

<a id="api-支持度-60"></a>

###### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseQueryCommand.geoWithin | ✔️ |  |  |  |  |  |  |  |

<a id="geointersects-1"></a>

##### geoIntersects

找出给定的地理位置图形相交的记录

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/command/Command.geoIntersects.html)

```tsx
(options: IntersectsCommandOptions) => DatabaseLogicCommand
```

| 参数 | 类型 |
| --- | --- |
| options | `IntersectsCommandOptions` |

<a id="api-支持度-61"></a>

###### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseQueryCommand.geoIntersects | ✔️ |  |  |  |  |  |  |  |

<a id="api-支持度-62"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DatabaseQueryCommand.eq | ✔️ |  |  |  |  |  |  |  |
| DatabaseQueryCommand.neq | ✔️ |  |  |  |  |  |  |  |
| DatabaseQueryCommand.gt | ✔️ |  |  |  |  |  |  |  |
| DatabaseQueryCommand.gte | ✔️ |  |  |  |  |  |  |  |
| DatabaseQueryCommand.lt | ✔️ |  |  |  |  |  |  |  |
| DatabaseQueryCommand.lte | ✔️ |  |  |  |  |  |  |  |
| DatabaseQueryCommand.in | ✔️ |  |  |  |  |  |  |  |
| DatabaseQueryCommand.nin | ✔️ |  |  |  |  |  |  |  |
| DatabaseQueryCommand.geoNear | ✔️ |  |  |  |  |  |  |  |
| DatabaseQueryCommand.geoWithin | ✔️ |  |  |  |  |  |  |  |
| DatabaseQueryCommand.geoIntersects | ✔️ |  |  |  |  |  |  |  |

<a id="databaseupdatecommand"></a>

#### DatabaseUpdateCommand

数据库更新操作符

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| fieldName | `string | InternalSymbol` |
| operator | `"remove" | "set" |
| operands | `any[]` | 操作数 |
| \_setFieldName | `(fieldName: string) => DatabaseUpdateCommand` | 设置作用域名称 |

<a id="logic_commands_literal"></a>

#### LOGIC\_COMMANDS\_LITERAL

逻辑命令字面量

| 参数 | 说明 |
| --- | --- |
| and | 与 |
| or | 或 |
| not | 非 |
| nor | 都不 |

<a id="query_commands_literal"></a>

#### QUERY\_COMMANDS\_LITERAL

查询命令字面量

| 参数 | 说明 |
| --- | --- |
| eq | 等于 |
| neq | 不等于 |
| gt | 大于 |
| gte | 大于等于 |
| lt | 小于 |
| lte | 小于等于 |
| in | 范围内 |
| nin | 范围外 |
| geoNear | 附近排序 |
| geoWithin | 指定区域内 |
| geoIntersects | 相交区域 |

<a id="update_commands_literal"></a>

#### UPDATE\_COMMANDS\_LITERAL

更新命令字面量

| 参数 | 说明 |
| --- | --- |
| set | 等于 |
| remove | 删除 |
| inc | 自增 |
| mul | 自乘 |
| push | 尾部添加 |
| pop | 尾部删除 |
| shift | 头部删除 |
| unshift | 头部添加 |

<a id="nearcommandoptions"></a>

#### NearCommandOptions

按从近到远的顺序，找出字段值在给定点的附近的记录参数

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| geometry | `GeoPoint` | 是 | 地理位置点 (Point) |
| maxDistance | `number` | 否 | 最大距离，单位为米 |
| minDistance | `number` | 否 | 最小距离，单位为米 |

<a id="withincommandoptions"></a>

#### WithinCommandOptions

找出字段值在指定区域内的记录，无排序参数

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| geometry | `GeoPolygon | GeoMultiPolygon` |

<a id="intersectscommandoptions"></a>

#### IntersectsCommandOptions

找出给定的地理位置图形相交的记录

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| geometry | `GeoPoint | GeoPolygon |

<a id="api-支持度-63"></a>

#### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Command.eq | ✔️ |  |  |  |  |  |  |  |
| Command.neq | ✔️ |  |  |  |  |  |  |  |
| Command.gte | ✔️ |  |  |  |  |  |  |  |
| Command.lt | ✔️ |  |  |  |  |  |  |  |
| Command.lte | ✔️ |  |  |  |  |  |  |  |
| Command.in | ✔️ |  |  |  |  |  |  |  |
| Command.nin | ✔️ |  |  |  |  |  |  |  |
| Command.geoNear | ✔️ |  |  |  |  |  |  |  |
| Command.geoWithin | ✔️ |  |  |  |  |  |  |  |
| Command.geoIntersects | ✔️ |  |  |  |  |  |  |  |
| Command.and | ✔️ |  |  |  |  |  |  |  |
| Command.or | ✔️ |  |  |  |  |  |  |  |
| Command.set | ✔️ |  |  |  |  |  |  |  |
| Command.remove | ✔️ |  |  |  |  |  |  |  |
| Command.inc | ✔️ |  |  |  |  |  |  |  |
| Command.mul | ✔️ |  |  |  |  |  |  |  |
| Command.push | ✔️ |  |  |  |  |  |  |  |
| Command.pop | ✔️ |  |  |  |  |  |  |  |
| Command.shift | ✔️ |  |  |  |  |  |  |  |
| Command.unshift | ✔️ |  |  |  |  |  |  |  |

<a id="aggregate-1"></a>

### Aggregate

数据库集合的聚合操作实例

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.html)

<a id="addfields"></a>

#### addFields

聚合阶段。添加新字段到输出的记录。经过 addFields 聚合阶段，输出的所有记录中除了输入时带有的字段外，还将带有 addFields 指定的字段。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.addFields.html)

```tsx
(object: Object) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| object | `Object` |

<a id="api-支持度-64"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.addFields | ✔️ |  |  |  |  |  |  |  |

<a id="bucket"></a>

#### bucket

聚合阶段。将输入记录根据给定的条件和边界划分成不同的组，每组即一个 bucket。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.bucket.html)

```tsx
(object: Object) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| object | `Object` |

<a id="api-支持度-65"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.bucket | ✔️ |  |  |  |  |  |  |  |

<a id="bucketauto"></a>

#### bucketAuto

聚合阶段。将输入记录根据给定的条件划分成不同的组，每组即一个 bucket。与 bucket 的其中一个不同之处在于无需指定 boundaries，bucketAuto 会自动尝试将记录尽可能平均的分散到每组中。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.bucketAuto.html)

```tsx
(object: Object) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| object | `Object` |

<a id="api-支持度-66"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.bucketAuto | ✔️ |  |  |  |  |  |  |  |

<a id="count-2"></a>

#### count

聚合阶段。计算上一聚合阶段输入到本阶段的记录数，输出一个记录，其中指定字段的值为记录数。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.count.html)

```tsx
(fieldName: string) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| fieldName | `string` |

<a id="api-支持度-67"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.count | ✔️ |  |  |  |  |  |  |  |

<a id="end"></a>

#### end

标志聚合操作定义完成，发起实际聚合操作

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.end.html)

```tsx
() => Promise<Object>
```

<a id="api-支持度-68"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.end | ✔️ |  |  |  |  |  |  |  |

<a id="geonear-2"></a>

#### geoNear

聚合阶段。将记录按照离给定点从近到远输出。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.geoNear.html)

```tsx
(options: Object) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| options | `Object` |

<a id="api-支持度-69"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.geoNear | ✔️ |  |  |  |  |  |  |  |

<a id="group"></a>

#### group

聚合阶段。将输入记录按给定表达式分组，输出时每个记录代表一个分组，每个记录的 \_id 是区分不同组的 key。输出记录中也可以包括累计值，将输出字段设为累计值即会从该分组中计算累计值。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.group.html)

```tsx
(object: Object) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| object | `Object` |

<a id="api-支持度-70"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.group | ✔️ |  |  |  |  |  |  |  |

<a id="limit-2"></a>

#### limit

聚合阶段。限制输出到下一阶段的记录数。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.limit.html)

```tsx
(value: number) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| value | `number` |

<a id="api-支持度-71"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.limit | ✔️ |  |  |  |  |  |  |  |

<a id="lookup"></a>

#### lookup

聚合阶段。聚合阶段。联表查询。与同个数据库下的一个指定的集合做 left outer join(左外连接)。对该阶段的每一个输入记录，lookup 会在该记录中增加一个数组字段，该数组是被联表中满足匹配条件的记录列表。lookup 会将连接后的结果输出给下个阶段。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.lookup.html)

```tsx
(object: Object) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| object | `Object` |

<a id="api-支持度-72"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.lookup | ✔️ |  |  |  |  |  |  |  |

<a id="match"></a>

#### match

聚合阶段。根据条件过滤文档，并且把符合条件的文档传递给下一个流水线阶段。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.match.html)

```tsx
(object: Object) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| object | `Object` |

<a id="api-支持度-73"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.match | ✔️ |  |  |  |  |  |  |  |

<a id="project"></a>

#### project

聚合阶段。把指定的字段传递给下一个流水线，指定的字段可以是某个已经存在的字段，也可以是计算出来的新字段。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.project.html)

```tsx
(object: Object) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| object | `Object` |

<a id="api-支持度-74"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.project | ✔️ |  |  |  |  |  |  |  |

<a id="replaceroot"></a>

#### replaceRoot

聚合阶段。指定一个已有字段作为输出的根节点，也可以指定一个计算出的新字段作为根节点。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.replaceRoot.html)

```tsx
(object: Object) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| object | `Object` |

<a id="api-支持度-75"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.replaceRoot | ✔️ |  |  |  |  |  |  |  |

<a id="sample"></a>

#### sample

聚合阶段。随机从文档中选取指定数量的记录。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.sample.html)

```tsx
(size: number) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| size | `number` |

<a id="api-支持度-76"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.sample | ✔️ |  |  |  |  |  |  |  |

<a id="skip-2"></a>

#### skip

聚合阶段。指定一个正整数，跳过对应数量的文档，输出剩下的文档。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.skip.html)

```tsx
(value: number) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| value | `number` |

<a id="api-支持度-77"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.skip | ✔️ |  |  |  |  |  |  |  |

<a id="sort"></a>

#### sort

聚合阶段。根据指定的字段，对输入的文档进行排序。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.sort.html)

```tsx
(object: Object) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| object | `Object` |

<a id="api-支持度-78"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.sort | ✔️ |  |  |  |  |  |  |  |

<a id="sortbycount"></a>

#### sortByCount

聚合阶段。根据传入的表达式，将传入的集合进行分组（group）。然后计算不同组的数量，并且将这些组按照它们的数量进行排序，返回排序后的结果。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.sortByCount.html)

```tsx
(object: Object) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| object | `Object` |

<a id="api-支持度-79"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.sortByCount | ✔️ |  |  |  |  |  |  |  |

<a id="unwind"></a>

#### unwind

聚合阶段。使用指定的数组字段中的每个元素，对文档进行拆分。拆分后，文档会从一个变为一个或多个，分别对应数组的每个元素。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/aggregate/Aggregate.unwind.html)

```tsx
(value: string | object) => Aggregate
```

| 参数 | 类型 |
| --- | --- |
| value | `string |

<a id="api-支持度-80"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.unwind | ✔️ |  |  |  |  |  |  |  |

<a id="api-支持度-81"></a>

#### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Aggregate.addFields | ✔️ |  |  |  |  |  |  |  |
| Aggregate.bucket | ✔️ |  |  |  |  |  |  |  |
| Aggregate.bucketAuto | ✔️ |  |  |  |  |  |  |  |
| Aggregate.count | ✔️ |  |  |  |  |  |  |  |
| Aggregate.end | ✔️ |  |  |  |  |  |  |  |
| Aggregate.geoNear | ✔️ |  |  |  |  |  |  |  |
| Aggregate.group | ✔️ |  |  |  |  |  |  |  |
| Aggregate.limit | ✔️ |  |  |  |  |  |  |  |
| Aggregate.lookup | ✔️ |  |  |  |  |  |  |  |
| Aggregate.match | ✔️ |  |  |  |  |  |  |  |
| Aggregate.project | ✔️ |  |  |  |  |  |  |  |
| Aggregate.replaceRoot | ✔️ |  |  |  |  |  |  |  |
| Aggregate.sample | ✔️ |  |  |  |  |  |  |  |
| Aggregate.skip | ✔️ |  |  |  |  |  |  |  |
| Aggregate.sort | ✔️ |  |  |  |  |  |  |  |
| Aggregate.sortByCount | ✔️ |  |  |  |  |  |  |  |
| Aggregate.unwind | ✔️ |  |  |  |  |  |  |  |

<a id="igeo"></a>

### IGeo

数据库地理位置结构集

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/Geo.html)

<a id="point"></a>

#### Point

构造一个地理位置 ”点“。方法接受两个必填参数，第一个是经度（longitude），第二个是纬度（latitude），务必注意顺序。

如存储地理位置信息的字段有被查询的需求，务必对字段建立地理位置索引

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/geo/Geo.Point.html)

```tsx
(longitude: number, latitide: number) => GeoPoint
```

| 参数 | 类型 |
| --- | --- |
| longitude | `number` |
| latitide | `number` |

<a id="示例代码-25"></a>

##### 示例代码

<a id="示例-1-9"></a>

###### 示例 1

```tsx
db.collection('todos').add({
  data: {
    description: 'eat an apple',
    location: db.Geo.Point(113, 23)
  }
}).then(console.log).catch(console.error)
```

<a id="示例-2-9"></a>

###### 示例 2

除了使用接口构造一个点外，也可以使用等价的 GeoJSON 的 点 (Point) 的 JSON 表示，其格式如下：

```json
{
  "type": "Point",
  "coordinates": [longitude, latitude] // 数字数组：[经度, 纬度]
}
```

```tsx
db.collection('todos').add({
  data: {
    description: 'eat an apple',
    location: {
      type: 'Point',
      coordinates: [113, 23]
    }
  }
}).then(console.log).catch(console.error)
```

<a id="api-支持度-82"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| IGeo.Point | ✔️ |  |  |  |  |  |  |  |

<a id="linestring"></a>

#### LineString

构造一个地理位置的 ”线“。一个线由两个或更多的点有序连接组成。

如存储地理位置信息的字段有被查询的需求，务必对字段建立地理位置索引

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/geo/Geo.LineString.html)

```tsx
(points: JSONMultiPoint | GeoPoint[]) => GeoMultiPoint
```

| 参数 | 类型 |
| --- | --- |
| points | `JSONMultiPoint |

<a id="示例代码-26"></a>

##### 示例代码

<a id="示例-1-10"></a>

###### 示例 1

```tsx
db.collection('todos').add({
  data: {
    description: 'eat an apple',
    location: db.Geo.LineString([
      db.Geo.Point(113, 23),
      db.Geo.Point(120, 50),
      // ... 可选更多点
    ])
  }
}).then(console.log).catch(console.error)
```

<a id="示例-2-10"></a>

###### 示例 2

除了使用接口构造一条 LineString 外，也可以使用等价的 GeoJSON 的 线 (LineString) 的 JSON 表示，其格式如下：

```json
{
  "type": "LineString",
  "coordinates": [
    [p1_lng, p1_lat],
    [p2_lng, p2_lng]
    // ... 可选更多点
  ]
}
```

```tsx
db.collection('todos').add({
  data: {
    description: 'eat an apple',
    location: {
      type: 'LineString',
      coordinates: [
        [113, 23],
        [120, 50]
      ]
    }
  }
}).then(console.log).catch(console.error)
```

<a id="api-支持度-83"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| IGeo.LineString | ✔️ |  |  |  |  |  |  |  |

<a id="polygon"></a>

#### Polygon

构造一个地理位置 ”多边形“

如存储地理位置信息的字段有被查询的需求，务必对字段建立地理位置索引

**说明**

一个多边形由一个或多个线性环（Linear Ring）组成，一个线性环即一个闭合的线段。一个闭合线段至少由四个点组成，其中最后一个点和第一个点的坐标必须相同，以此表示环的起点和终点。如果一个多边形由多个线性环组成，则第一个线性环表示外环（外边界），接下来的所有线性环表示内环（即外环中的洞，不计在此多边形中的区域）。如果一个多边形只有一个线性环组成，则这个环就是外环。

多边形构造规则：

1. 第一个线性环必须是外环
2. 外环不能自交
3. 所有内环必须完全在外环内
4. 各个内环间不能相交或重叠，也不能有共同的边
5. 外环应为逆时针，内环应为顺时针

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/geo/Geo.Polygon.html)

```tsx
(lineStrings: JSONPolygon | GeoLineString[]) => GeoPolygon
```

| 参数 | 类型 |
| --- | --- |
| lineStrings | `JSONPolygon |

<a id="示例代码-27"></a>

##### 示例代码

<a id="示例-1-11"></a>

###### 示例 1

单环多边形

```tsx
const { Polygon, LineString, Point } = db.Geo
db.collection('todos').add({
  data: {
    description: 'eat an apple',
    location: Polygon([
      LineString([
        Point(0, 0),
        Point(3, 2),
        Point(2, 3),
        Point(0, 0)
      ])
    ])
  }
}).then(console.log).catch(console.error)
```

<a id="示例-2-11"></a>

###### 示例 2

含一个外环和一个内环的多边形

```tsx
const { Polygon, LineString, Point } = db.Geo
db.collection('todos').add({
  data: {
    description: 'eat an apple',
    location: Polygon([
      // 外环
      LineString([ Point(0, 0), Point(30, 20), Point(20, 30), Point(0, 0) ]),
      // 内环
      LineString([ Point(10, 10), Point(16, 14), Point(14, 16), Point(10, 10) ])
    ])
  }
}).then(console.log).catch(console.error)
```

<a id="示例-3-1"></a>

###### 示例 3

除了使用接口构造一个 Polygon 外，也可以使用等价的 GeoJSON 的 多边形 (Polygon) 的 JSON 表示，其格式如下：

```json
{
  "type": "Polygon",
  "coordinates": [
    [ [lng, lat], [lng, lat], [lng, lat], ..., [lng, lat] ], // 外环
    [ [lng, lat], [lng, lat], [lng, lat], ..., [lng, lat] ], // 可选内环 1
    ...
    [ [lng, lat], [lng, lat], [lng, lat], ..., [lng, lat] ], // 可选内环 n
  ]
}
```

```tsx
db.collection('todos').add({
  data: {
    description: 'eat an apple',
    location: {
      type: 'Polygon',
      coordinates: [
        [ [0, 0], [30, 20], [20, 30], [0, 0] ],
        [ [10, 10], [16, 14], [14, 16], [10, 10]]
      ]
    }
  }
}).then(console.log).catch(console.error)
```

<a id="api-支持度-84"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| IGeo.Polygon | ✔️ |  |  |  |  |  |  |  |

<a id="multipoint"></a>

#### MultiPoint

构造一个地理位置的 ”点“ 的集合。一个点集合由一个或更多的点组成。

如存储地理位置信息的字段有被查询的需求，务必对字段建立地理位置索引

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/geo/Geo.MultiPoint.html)

```tsx
(polygons: JSONMultiPolygon | GeoPolygon[]) => GeoMultiPolygon
```

| 参数 | 类型 |
| --- | --- |
| polygons | `JSONMultiPolygon |

<a id="示例代码-28"></a>

##### 示例代码

<a id="示例-1-12"></a>

###### 示例 1

```tsx
db.collection('todos').add({
  data: {
    description: 'eat an apple',
    location: db.Geo.MultiPoint([
      db.Geo.Point(113, 23),
      db.Geo.Point(120, 50),
      // ... 可选更多点
    ])
  }
}).then(console.log).catch(console.error)
```

<a id="示例-2-12"></a>

###### 示例 2

除了使用接口构造 MultiPoint 外，也可以使用等价的 GeoJSON 的 点集合 (MultiPoint) 的 JSON 表示，其格式如下：

```json
{
  "type": "MultiPoint",
  "coordinates": [
    [p1_lng, p1_lat],
    [p2_lng, p2_lng]
    // ... 可选更多点
  ]
}
```

```tsx
db.collection('todos').add({
  data: {
    description: 'eat an apple',
    location: {
      type: 'MultiPoint',
      coordinates: [
        [113, 23],
        [120, 50]
      ]
    }
  }
}).then(console.log).catch(console.error)
```

<a id="api-支持度-85"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| IGeo.MultiPoint | ✔️ |  |  |  |  |  |  |  |

<a id="multilinestring"></a>

#### MultiLineString

构造一个地理位置 ”线“ 集合。一个线集合由多条线组成。

如存储地理位置信息的字段有被查询的需求，务必对字段建立地理位置索引

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/geo/Geo.MultiLineString.html)

```tsx
(lineStrings: JSONMultiLineString | GeoLineString[]) => GeoMultiLineString
```

| 参数 | 类型 |
| --- | --- |
| lineStrings | `JSONMultiLineString |

<a id="示例代码-29"></a>

##### 示例代码

<a id="示例-1-13"></a>

###### 示例 1

```tsx
const { LineString, MultiLineString, Point } = db.Geo
db.collection('todos').add({
  data: {
    description: 'eat an apple',
    location: MultiLineString([
      LineString([ Point(0, 0), Point(30, 20), Point(20, 30), Point(0, 0) ]),
      LineString([ Point(10, 10), Point(16, 14), Point(14, 16), Point(10, 10) ])
    ])
  }
}).then(console.log).catch(console.error)
```

<a id="示例-2-13"></a>

###### 示例 2

除了使用接口构造一个 MultiLineString 外，也可以使用等价的 GeoJSON 的 线集合 (MultiLineString) 的 JSON 表示，其格式如下：

```json
{
  "type": "MultiLineString",
  "coordinates": [
    [ [lng, lat], [lng, lat], [lng, lat], ..., [lng, lat] ],
    [ [lng, lat], [lng, lat], [lng, lat], ..., [lng, lat] ],
    ...
    [ [lng, lat], [lng, lat], [lng, lat], ..., [lng, lat] ]
  ]
}
```

```tsx
db.collection('todos').add({
  data: {
    description: 'eat an apple',
    location: {
      type: 'MultiLineString',
      coordinates: [
        [ [0, 0], [3, 3] ],
        [ [5, 10], [20, 30] ]
      ]
    }
  }
}).then(console.log).catch(console.error)
```

<a id="api-支持度-86"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| IGeo.MultiLineString | ✔️ |  |  |  |  |  |  |  |

<a id="multipolygon"></a>

#### MultiPolygon

构造一个地理位置 ”多边形“ 集合。一个多边形集合由多个多边形组成。

如存储地理位置信息的字段有被查询的需求，务必对字段建立地理位置索引

**说明**

一个多边形由一个或多个线性环（Linear Ring）组成，一个线性环即一个闭合的线段。一个闭合线段至少由四个点组成，其中最后一个点和第一个点的坐标必须相同，以此表示环的起点和终点。如果一个多边形由多个线性环组成，则第一个线性环表示外环（外边界），接下来的所有线性环表示内环（即外环中的洞，不计在此多边形中的区域）。如果一个多边形只有一个线性环组成，则这个环就是外环。

多边形构造规则：

1. 第一个线性环必须是外环
2. 外环不能自交
3. 所有内环必须完全在外环内
4. 各个内环间不能相交或重叠，也不能有共同的边
5. 外环应为逆时针，内环应为顺时针

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/geo/Geo.MultiPolygon.html)

```tsx
(polygons: JSONMultiPolygon | GeoPolygon[]) => GeoMultiPolygon
```

| 参数 | 类型 |
| --- | --- |
| polygons | `JSONMultiPolygon |

<a id="示例代码-30"></a>

##### 示例代码

<a id="示例-1-14"></a>

###### 示例 1

```tsx
const { MultiPolygon, Polygon, LineString, Point } = db.Geo
db.collection('todos').add({
  data: {
    description: 'eat an apple',
    location: MultiPolygon([
      Polygon([
        LineString([ Point(50, 50), Point(60, 80), Point(80, 60), Point(50, 50) ]),
      ]),
      Polygon([
        LineString([ Point(0, 0), Point(30, 20), Point(20, 30), Point(0, 0) ]),
        LineString([ Point(10, 10), Point(16, 14), Point(14, 16), Point(10, 10) ])
      ]),
    ])
  }
}).then(console.log).catch(console.error)
```

<a id="示例-2-14"></a>

###### 示例 2

除了使用接口构造一个 MultiPolygon 外，也可以使用等价的 GeoJSON 的 多边形 (MultiPolygon) 的 JSON 表示，其格式如下：

```json
{
  "type": "MultiPolygon",
  "coordinates": [
    // polygon 1
    [
      [ [lng, lat], [lng, lat], [lng, lat], ..., [lng, lat] ],
      [ [lng, lat], [lng, lat], [lng, lat], ..., [lng, lat] ],
      ...
      [ [lng, lat], [lng, lat], [lng, lat], ..., [lng, lat] ]
    ],
    ...
    // polygon n
    [
      [ [lng, lat], [lng, lat], [lng, lat], ..., [lng, lat] ],
      [ [lng, lat], [lng, lat], [lng, lat], ..., [lng, lat] ],
      ...
      [ [lng, lat], [lng, lat], [lng, lat], ..., [lng, lat] ]
    ],
  ]
}
```

```tsx
db.collection('todos').add({
  data: {
    description: 'eat an apple',
    location: {
      type: 'MultiPolygon',
      coordinates: [
        [
          [ [50, 50], [60, 80], [80, 60], [50, 50] ]
        ],
        [
          [ [0, 0], [30, 20], [20, 30], [0, 0] ],
          [ [10, 10], [16, 14], [14, 16], [10, 10]]
        ]
      ]
    }
  }
}).then(console.log).catch(console.error)
```

<a id="api-支持度-87"></a>

##### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| IGeo.MultiPolygon | ✔️ |  |  |  |  |  |  |  |

<a id="geopoint"></a>

#### GeoPoint

地理位置 “点”

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/geo/GeoPoint.html)

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| longitude | `number` | 经度 |
| latitude | `number` | 纬度 |

<a id="tojson"></a>

##### toJSON

格式化为 JSON 结构

```tsx
() => object
```

<a id="tostring"></a>

##### toString

格式化为字符串

```tsx
() => string
```

<a id="geolinestring"></a>

#### GeoLineString

地理位置的 ”线“。一个线由两个或更多的点有序连接组成。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/geo/GeoLineString.html)

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| points | `GeoPoint[]` | 点集合 |

<a id="tojson-1"></a>

##### toJSON

格式化为 JSON 结构

```tsx
() => JSONLineString
```

<a id="tostring-1"></a>

##### toString

格式化为字符串

```tsx
() => string
```

<a id="geopolygon"></a>

#### GeoPolygon

地理位置 ”多边形“

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/geo/GeoPolygon.html)

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| lines | `GeoLineString[]` | 线集合 |

<a id="tojson-2"></a>

##### toJSON

格式化为 JSON 结构

```tsx
() => JSONPolygon
```

<a id="tostring-2"></a>

##### toString

格式化为字符串

```tsx
() => string
```

<a id="geomultipoint"></a>

#### GeoMultiPoint

地理位置的 ”点“ 的集合。一个点集合由一个或更多的点组成。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/geo/GeoMultiPoint.html)

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| points | `GeoPoint[]` | 点集合 |

<a id="tojson-3"></a>

##### toJSON

格式化为 JSON 结构

```tsx
() => JSONMultiPoint
```

<a id="tostring-3"></a>

##### toString

格式化为字符串

```tsx
() => string
```

<a id="geomultilinestring"></a>

#### GeoMultiLineString

地理位置 ”线“ 集合。一个线集合由多条线组成。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/geo/GeoMultiLineString.html)

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| lines | `GeoLineString[]` | 线集合 |

<a id="tojson-4"></a>

##### toJSON

格式化为 JSON 结构

```tsx
() => JSONMultiLineString
```

<a id="tostring-4"></a>

##### toString

格式化为字符串

```tsx
() => string
```

<a id="geomultipolygon"></a>

#### GeoMultiPolygon

地理位置 ”多边形“ 集合。一个多边形集合由多个多边形组成。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/reference-sdk-api/database/geo/GeoMultiPolygon.html)

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| polygons | `GeoPolygon[]` | 多边形集合 |

<a id="tojson-5"></a>

##### toJSON

格式化为 JSON 结构

```tsx
() => JSONMultiPolygon
```

<a id="tostring-5"></a>

##### toString

格式化为字符串

```tsx
() => string
```

<a id="jsonpoint"></a>

#### JSONPoint

地理位置 “点” 的 JSON 结构

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| type | `"Point"` | 类型 |
| coordinates | `[number, number]` | 坐标 |

<a id="jsonlinestring"></a>

#### JSONLineString

地理位置 ”线“ 的 JSON 结构

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| type | `"LineString"` | 类型 |
| coordinates | `[number, number][]` | 坐标 |

<a id="jsonpolygon"></a>

#### JSONPolygon

地理位置 ”多边形“ 的 JSON 结构

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| type | `"Polygon"` | 类型 |
| coordinates | `[number, number][][]` | 坐标 |

<a id="jsonmultipoint"></a>

#### JSONMultiPoint

地理位置的 ”点“ 集合的 JSON 结构

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| type | `"MultiPoint"` | 类型 |
| coordinates | `[number, number][]` | 坐标 |

<a id="jsonmultilinestring"></a>

#### JSONMultiLineString

地理位置 ”线“ 集合的 JSON 结构

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| type | `"MultiLineString"` | 类型 |
| coordinates | `[number, number][][]` | 坐标 |

<a id="jsonmultipolygon"></a>

#### JSONMultiPolygon

地理位置 ”多边形“ 集合的 JSON 结构

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| type | `"MultiPolygon"` | 类型 |
| coordinates | `[number, number][][][]` | 坐标 |

<a id="api-支持度-88"></a>

#### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | H5 | React Native | 快应用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| IGeo.Point | ✔️ |  |  |  |  |  |  |  |
| IGeo.LineString | ✔️ |  |  |  |  |  |  |  |
| IGeo.Polygon | ✔️ |  |  |  |  |  |  |  |
| IGeo.MultiPoint | ✔️ |  |  |  |  |  |  |  |
| IGeo.MultiLineString | ✔️ |  |  |  |  |  |  |  |
| IGeo.MultiPolygon | ✔️ |  |  |  |  |  |  |  |
