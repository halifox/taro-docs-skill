# Like

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/open/like)

点赞

支持情况：微信小程序 百度小程序 H5 React Native Harmony

> [参考文档](https://smartprogram.baidu.com/docs/develop/extended/component-content/like/)

<a id="类型"></a>

## 类型

```tsx
ComponentType<LikeProps>
```

<a id="likeprops"></a>

## LikeProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| isLiked | `boolean` | `false` | 否 | 是否已被点赞 |
| mode | `string` | `"icon"` | 否 | 按钮模式。icon：表示仅有图标；mixture：表示图标文字结合 |
| iconType | `string` | `"hand"` | 否 | 图标类型。hand：表示手形；heart：表示心形 |
| likeText | `string` | `"赞"` | 否 | 点赞按钮上的文案。默认为赞，仅在 mode 属性值为'mixture'时有效 |
| likeNum | `number` | `0` | 否 | 点赞数量 |
| likeType | `number` | `0` | 否 | 被点赞的对象类型。0：表示对文章内容进行点赞；1：表示对评论内容进行点赞 |
| animationType | `number` | `1` | 否 | 点赞动效形式。0：无动效；1：轻动效；2：强动效 |
| isShowToast | `boolean` | `false` | 否 | 点赞后是否弹出 toast 提示 |
| toastText | `string[]` | `['已点赞', '已取消']` | 否 | toast 文案，默认为已点赞、已取消 |
| likeParam | `ILikeParam` |  | 是 | 点赞服务需要的必要参数 |
| onError | `CommonEventFunction` |  | 否 | 使用 npm 方式引入点赞组件时，点击按钮时在用户未登录状态下会触发此事件；使用动态库方式引入点赞组件时，点击按钮时在用户未登录状态下不会触发此事件 |
| onSuccess | `CommonEventFunction` |  | 否 | 点击点赞按钮，在点赞服务成功后将状态返回给使用组件者 |
| onFail | `CommonEventFunction` |  | 否 | 点击点赞按钮，在点赞服务失败后将状态返回给使用组件者 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- | --- |
| LikeProps.isLiked |  | ✔️ |  |  |  |
| LikeProps.mode |  | ✔️ |  |  |  |
| LikeProps.iconType |  | ✔️ |  |  |  |
| LikeProps.likeText |  | ✔️ |  |  |  |
| LikeProps.likeNum |  | ✔️ |  |  |  |
| LikeProps.likeType |  | ✔️ |  |  |  |
| LikeProps.animationType |  | ✔️ |  |  |  |
| LikeProps.isShowToast |  | ✔️ |  |  |  |
| LikeProps.toastText |  | ✔️ |  |  |  |
| LikeProps.likeParam |  | ✔️ |  |  |  |
| LikeProps.onError |  | ✔️ |  |  |  |
| LikeProps.onSuccess |  | ✔️ |  |  |  |
| LikeProps.onFail |  | ✔️ |  |  |  |

<a id="ilikeparam"></a>

### ILikeParam

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| openid | `string` | 是 | 用户身份唯一标识 |
| snid | `string` | 是 | 被点赞的文章的 id，与 path 参数一一对应<br>example: "20200101" |
| spid | `string` | 否 | 被点赞的评论 id |
| title | `string` | 是 | 文章标题 |
| path | `string` | 是 | 智能小程序内页链接，最长不能超过 194 字符<br>example: "/pages/index/index" |
