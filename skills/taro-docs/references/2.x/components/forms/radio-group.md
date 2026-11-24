# RadioGroup

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/2.x/components/forms/radio-group)

单项选择器，内部由多个 Radio 组成。

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
| onChange | `BaseEventOrigFunction<any>` | 否 | RadioGroup 中选中项发生改变时触发 change 事件，detail = {value:[选中的radio的value的数组]} |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RadioGroupProps.onChange | ✔️ | ✔️ |  |

<a id="onchangeeventdetail"></a>

### onChangeEventDetail

| 参数 | 类型 |
| --- | --- |
| value | `string[]` |

<a id="api-支持度-1"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| RadioGroup | ✔️ | ✔️ | ✔️ |
