# Lifestyle

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/open/lifestyle)

关注生活号

支持情况：微信小程序 支付宝小程序 H5 React Native Harmony

> [参考文档](https://opendocs.alipay.com/mini/component/lifestyle)

<a id="类型"></a>

## 类型

```tsx
ComponentType<LifestyleProps>
```

<a id="lifestyleprops"></a>

## LifestyleProps

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| publicId | `string` | 否 | 必填，生活号 ID（即生活号 APPID），必须是当前小程序同账号主体且已关联的生活号。 |
| memo | `string` | 否 | 文案。支持商家自定义，最多展示一行。 |
| onFollow | `CommonEventFunction` | 否 | 当用户关注生活号成功后执行。 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 支付宝小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- | --- |
| LifestyleProps.publicId |  | ✔️ |  |  |  |
| LifestyleProps.memo |  | ✔️ |  |  |  |
| LifestyleProps.onFollow |  | ✔️ |  |  |  |
