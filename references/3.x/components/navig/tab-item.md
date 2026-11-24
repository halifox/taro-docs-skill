# TabItem

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/navig/tab-item)

标签栏子项

支持情况：微信小程序 百度小程序 H5 React Native Harmony

> [参考文档](https://smartprogram.baidu.com/docs/develop/component/tab-item/)

<a id="类型"></a>

## 类型

```tsx
ComponentType<TabItemProps>
```

<a id="tabitemprops"></a>

## TabItemProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| label | `string` | `无` | 否 | tab-item 内显示的文字 |
| name | `string` | `无` | 否 | tab-item 对应的 name 值 |
| badgeType | `string` | `无` | 否 | 徽标类型 badge-type 分为圆点“dot”和文本“text”，不设置 badge-type 则不显示徽标 |
| badgeText | `string` | `无` | 否 | badge-type 为 text 的时候，徽标内的数字，为空时badge-type="text"不生效 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- | --- |
| TabItemProps.label |  | ✔️ |  |  |  |
| TabItemProps.name |  | ✔️ |  |  |  |
| TabItemProps.badgeType |  | ✔️ |  |  |  |
| TabItemProps.badgeText |  | ✔️ |  |  |  |
