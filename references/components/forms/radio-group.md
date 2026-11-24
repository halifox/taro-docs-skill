# RadioGroup

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/forms/radio-group)

单项选择器，内部由多个 Radio 组成。

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 QQ 小程序 京东小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/radio-group.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<RadioGroupProps>
```

<a id="radiogroupprops"></a>

## RadioGroupProps

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| name | `string` | 否 | 组件名字，用于表单提交获取数据。 |
| onChange | `CommonEventFunction` | 否 | RadioGroup 中选中项发生改变时触发 change 事件，detail = {value:[选中的radio的value的数组]} |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | 支付宝小程序 | 抖音小程序 | QQ 小程序 | 京东小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| RadioGroupProps.name |  |  | ✔️ | ✔️ |  |  |  |  | ✔️ |  |  |
| RadioGroupProps.onChange | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |  |  | ✔️ | ✔️ |

<a id="onchangeeventdetail"></a>

### onChangeEventDetail

| 参数 | 类型 |
| --- | --- |
| value | `string[]` |
