# UserInfo

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/apis/open-api/user-info/UserInfo)

用户信息

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/user-info/UserInfo.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| avatarUrl | `string` | 用户头像图片的 URL。URL 最后一个数值代表正方形头像大小（有 0、46、64、96、132 数值可选，0 代表 640x640 的正方形头像，46 表示 46x46 的正方形头像，剩余数值以此类推。默认132），用户没有头像时该项为空。若用户更换头像，原有头像 URL 将失效。 |
| city | `string` | 用户所在城市 |
| country | `string` | 用户所在国家 |
| gender | `0 \| 1 \| 2` | 用户性别 |
| language | `"en" \| "zh_CN" \| "zh_TW"` | 显示 country，province，city 所用的语言 |
| nickName | `string` | 用户昵称 |
| province | `string` | 用户所在省份 |

<a id="参数"></a>

## 参数

<a id="language"></a>

### language

| 参数 | 类型 |
| --- | --- |
| en | `"英文"` |
| zh\_CN | `"简体中文"` |
| zh\_TW | `"繁体中文"` |

<a id="gender"></a>

### gender

| 参数 | 类型 |
| --- | --- |
| 0 | `"未知"` |
| 1 | `"男性"` |
| 2 | `"女性"` |
