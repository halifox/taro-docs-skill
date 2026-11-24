# ContactButton

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/open/contact-button)

智能客服

支持情况：微信小程序 支付宝小程序 H5 React Native Harmony

> [参考文档](https://opendocs.alipay.com/mini/component/contact-button)

<a id="类型"></a>

## 类型

```tsx
ComponentType<ContactButtonProps>
```

<a id="contactbuttonprops"></a>

## ContactButtonProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| tntInstId | `string` |  | 是 | 必填。企业唯一编码，一个企业支付宝账号对应一个编码。 |
| scene | `string` |  | 是 | 必填。聊天窗编码，每个聊天窗的唯一编码。 |
| size | string or number | `25` | 否 | 选填。咨询按钮大小，正方形设置边长（如25\*25 px）。 |
| color | `string` | `"#00A3FF"` | 否 | 选填。咨询按钮颜色，默认白底蓝色。 |
| icon | `string` |  | 否 | 选填。咨询按钮头像。 |
| alipayCardNo | `string` |  | 否 | 选填。支付宝访客用户ID（2088开头）。<br>说明： 客服回答问题时，如客户已离开咨询窗口，则通过推送消息到支付宝 card 中提醒客户。 |
| extInfo | `string` |  | 否 | 选填。该属性主要用于传递一些扩展信息给组件，以实现一些高级功能。该属性值的生成方式为：encodeURIComponent({"字段名":"字段值"})， 其中，字段名和字段值要根据实际使用的功能进行替换。<br>目前通过传入扩展信息可支持的 3 个功能：<br>1.访客名片。需传 cinfo 和 key 两个扩展字段，代码形如在云客服中进入 设置 > 服务窗配置 > 聊天窗 URL。点击操作栏中的 聊天窗 URL ，获取 tntInstId（企业编码）和 scene（聊天窗编码）。encodeURIComponent({"cinfo":"生成的 cinfo","key":"生成的key"})，cinfo 和 key 的值说明 支付宝小程序接入访客名片；<br>2.聊天窗默认带出用户的小程序订单数据。需传 appId 字段，代码形如encodeURIComponent({"appId":"商户小程序appid"})<br>3.未读客服消息同步至"我的小程序-我的"。同样需传 appId 字段，代码形如 encodeURIComponent({"appId":"商户小程序appid"})。 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 支付宝小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- | --- |
| ContactButtonProps.tntInstId |  | ✔️ |  |  |  |
| ContactButtonProps.scene |  | ✔️ |  |  |  |
| ContactButtonProps.size |  | ✔️ |  |  |  |
| ContactButtonProps.color |  | ✔️ |  |  |  |
| ContactButtonProps.icon |  | ✔️ |  |  |  |
| ContactButtonProps.alipayCardNo |  | ✔️ |  |  |  |
| ContactButtonProps.extInfo |  | ✔️ |  |  |  |
