# VoipRoom

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/media/voip-room)

多人音视频对话

需用户授权 `scope.camera`、`scope.record`。相关接口： [Taro.joinVoIPChat](../../apis/media/voip/joinVoIPChat.md)
开通该组件权限后，开发者可在 joinVoIPChat 成功后，获取房间成员的 openid，传递给 voip-room 组件，以显示成员画面。

支持情况：微信小程序 H5 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/voip-room.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<VoipRoomProps>
```

<a id="示例代码"></a>

## 示例代码

```tsx
export default class PageView extends Component {
  constructor() {
    super(...arguments)
  }

  render() {
    return (
      <VoipRoom
        openId="{{item}}"
        mode="{{selfOpenId === item ? 'camera' : 'video'}}">
      </VoipRoom>
    )
  }
}
```

<a id="voiproomprops"></a>

## VoipRoomProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| mode | `keyof Mode` | `camera` | 否 | 对话窗口类型，自身传入 camera，其它用户传入 video |
| devicePosition | `keyof DevicePosition` | `front` | 否 | 仅在 mode 为 camera 时有效，前置或后置，值为front, back |
| openId | `string` | `"none"` | 否 | 进入房间用户的 openid |
| objectFit | "fill" or "contain" or "cover" | `"fill"` | 否 | 画面与容器比例不一致时，画面的表现形式 |
| onError | `CommonEventFunction` |  | 否 | 创建对话窗口失败时触发 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native | Harmony |
| --- | --- | --- | --- | --- |
| VoipRoomProps.mode | ✔️ |  |  |  |
| VoipRoomProps.devicePosition | ✔️ |  |  |  |
| VoipRoomProps.openId | ✔️ |  |  |  |
| VoipRoomProps.objectFit | ✔️ |  |  |  |
| VoipRoomProps.onError | ✔️ |  |  |  |

<a id="mode"></a>

### Mode

对话窗口类型

<a id="deviceposition"></a>

### DevicePosition

摄像头类型
