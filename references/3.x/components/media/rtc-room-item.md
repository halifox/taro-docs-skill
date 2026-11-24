# RtcRoomItem

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/components/media/rtc-room-item)

实时音视频通话画面

支持情况：微信小程序 百度小程序 H5 React Native Harmony

> [参考文档](https://smartprogram.baidu.com/docs/develop/component/media_rtc-room-item/)

<a id="类型"></a>

## 类型

```tsx
ComponentType<RtcRoomItemProps>
```

<a id="rtcroomitemprops"></a>

## RtcRoomItemProps

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| id | `string` | 否 | rtc-room-item 组件的唯一标识符 |
| type | `string` | 否 | 指定 item 展示本地 / 远端画面，有效值：local、remote ，不可动态变更 |
| userId | `number` | 否 | item 展示画面的用户 id |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | 百度小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- | --- |
| RtcRoomItemProps.id |  | ✔️ |  |  |  |
| RtcRoomItemProps.type |  | ✔️ |  |  |  |
| RtcRoomItemProps.userId |  | ✔️ |  |  |  |
