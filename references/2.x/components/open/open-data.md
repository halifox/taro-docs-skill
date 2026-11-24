# OpenData

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/components/open/open-data)

用于展示微信开放的数据

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/open-data.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<OpenDataProps>
```

<a id="示例代码"></a>

## 示例代码

```tsx
class App extends Component {
  render () {
    return (
      <OpenData type='userAvatarUrl'/>
    )
  }
}
```

<a id="opendataprops"></a>

## OpenDataProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| type | `"groupName" \| "userNickName" \| "userAvatarUrl" \| "userGender" \| "userCity" \| "userProvince" \| "userCountry" \| "userLanguage"` |  | 是 | 开放数据类型 |
| openGid | `string` |  | 否 | 当 type="groupName" 时生效, 群id |
| lang | `"en" \| "zh_CN" \| "zh_TW"` | `"en"` | 否 | 当 type="user\*" 时生效，以哪种语言展示 userInfo |
| defaultText | `string` |  | 否 | 数据为空时的默认文案 |
| defaultAvatar | `string` |  | 否 | 用户头像为空时的默认图片，支持相对路径和网络图片路径 |
| onError | `BaseEventOrigFunction<any>` |  | 否 | 群名称或用户信息为空时触发 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| OpenDataProps.type | ✔️ |  |  |
| OpenDataProps.openGid | ✔️ |  |  |
| OpenDataProps.lang | ✔️ |  |  |
| OpenDataProps.defaultText | ✔️ |  |  |
| OpenDataProps.defaultAvatar | ✔️ |  |  |
| OpenDataProps.onError | ✔️ |  |  |

<a id="type"></a>

### type

type 的合法值

| 参数 | 说明 |
| --- | --- |
| groupName | 拉取群名称 |
| userNickName | 用户昵称 |
| userAvatarUrl | 用户头像 |
| userGender | 用户性别 |
| userCity | 用户所在城市 |
| userProvince | 用户所在省份 |
| userCountry | 用户所在国家 |
| userLanguage | 用户的语言 |

<a id="lang"></a>

### lang

lang 的合法值

| 参数 | 说明 |
| --- | --- |
| en | 英文 |
| zh\_CN | 简体中文 |
| zh\_TW | 繁体中文 |

<a id="api-支持度-1"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| OpenData | ✔️ |  |  |
