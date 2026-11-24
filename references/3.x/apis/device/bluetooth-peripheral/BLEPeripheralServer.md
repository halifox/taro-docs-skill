# BLEPeripheralServer

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/device/bluetooth-peripheral/BLEPeripheralServer)

外围设备的服务端

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.html)

<a id="方法"></a>

## 方法

<a id="addservice"></a>

### addService

添加服务

支持情况：微信小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.addService.html)

```tsx
(option: Option) => Promise<TaroGeneral.BluetoothError>
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="close"></a>

### close

关闭当前服务端

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.close.html)

```tsx
(option: Option) => Promise<TaroGeneral.BluetoothError>
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="offcharacteristicreadrequest"></a>

### offCharacteristicReadRequest

取消监听已连接的设备请求读当前外围设备的特征值事件

支持情况：微信小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.offCharacteristicReadRequest.html)

```tsx
(callback?: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 已连接的设备请求读当前外围设备的特征值事件的回调函数 |

<a id="offcharacteristicsubscribed"></a>

### offCharacteristicSubscribed

取消监听特征订阅事件

支持情况：微信小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.offCharacteristicSubscribed.html)

```tsx
(callback?: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 特征订阅事件的回调函数 |

<a id="offcharacteristicunsubscribed"></a>

### offCharacteristicUnsubscribed

取消监听取消特征订阅事件

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.offCharacteristicUnsubscribed.html)

```tsx
(callback?: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 取消特征订阅事件的回调函数 |

<a id="offcharacteristicwriterequest"></a>

### offCharacteristicWriteRequest

取消监听已连接的设备请求写当前外围设备的特征值事件

支持情况：微信小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.offCharacteristicWriteRequest.html)

```tsx
(callback?: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 已连接的设备请求写当前外围设备的特征值事件的回调函数 |

<a id="oncharacteristicreadrequest"></a>

### onCharacteristicReadRequest

监听已连接的设备请求读当前外围设备的特征值事件

收到该消息后需要立刻调用 [writeCharacteristicValue](../../../../apis/device/bluetooth-peripheral/BLEPeripheralServer.md#writecharacteristicvalue) 写回数据，否则主机不会收到响应。

支持情况：微信小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.onCharacteristicReadRequest.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 已连接的设备请求读当前外围设备的特征值事件的回调函数 |

<a id="oncharacteristicsubscribed"></a>

### onCharacteristicSubscribed

监听特征订阅事件，仅 iOS 支持

支持情况：微信小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.onCharacteristicSubscribed.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 特征订阅事件的回调函数 |

<a id="oncharacteristicunsubscribed"></a>

### onCharacteristicUnsubscribed

监听取消特征订阅事件，仅 iOS 支持

支持情况：微信小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.onCharacteristicUnsubscribed.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 取消特征订阅事件的回调函数 |

<a id="oncharacteristicwriterequest"></a>

### onCharacteristicWriteRequest

监听已连接的设备请求写当前外围设备的特征值事件

支持情况：微信小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.onCharacteristicWriteRequest.html)

```tsx
(callback: Callback) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| callback | `Callback` | 已连接的设备请求写当前外围设备的特征值事件的回调函数 |

<a id="removeservice"></a>

### removeService

移除服务

支持情况：微信小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.removeService.html)

```tsx
(option: Option) => Promise<TaroGeneral.BluetoothError>
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="startadvertising"></a>

### startAdvertising

开始广播本地创建的外围设备

支持情况：微信小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.startAdvertising.html)

```tsx
(option: Option) => Promise<TaroGeneral.BluetoothError>
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="stopadvertising"></a>

### stopAdvertising

停止广播

支持情况：微信小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.stopAdvertising.html)

```tsx
(option: Option) => Promise<TaroGeneral.BluetoothError>
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="writecharacteristicvalue"></a>

### writeCharacteristicValue

往指定特征写入二进制数据值，并通知已连接的主机，从机的特征值已发生变化，该接口会处理是走回包还是走订阅

支持情况：微信小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth-peripheral/BLEPeripheralServer.writeCharacteristicValue.html)

```tsx
(option: Option) => Promise<TaroGeneral.BluetoothError>
```

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="参数"></a>

## 参数

<a id="addservice-1"></a>

### addService

<a id="option"></a>

#### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| service | `service` | 是 | 描述 service 的 Object |
| complete | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用成功的回调函数 |

<a id="service"></a>

#### service

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| uuid | `string` | 蓝牙服务的 UUID |
| characteristics | `characteristic[]` | characteristics 列表 |

<a id="characteristic"></a>

#### characteristic

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| uuid | `string` | 是 | characteristic 的 UUID |
| properties | `properties` | 否 | 特征支持的操作 |
| permission | `characteristicPermission` | 否 | 特征权限 |
| value | `ArrayBuffer` | 否 | 特征对应的二进制值 |
| descriptors | `descriptor[]` | 否 | 描述符数据 |

<a id="properties"></a>

#### properties

特征支持的操作

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| write | `boolean` | `false` | 否 | 写 |
| writeNoResponse | `boolean` | `false` | 否 | 无回复写 |
| read | `boolean` | `false` | 否 | 读 |
| notify | `boolean` | `false` | 否 | 订阅 |
| indicate | `boolean` | `false` | 否 | 回包 |

<a id="characteristicpermission"></a>

#### characteristicPermission

特征权限

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| readable | `boolean` | `false` | 否 | 可读 |
| writeable | `boolean` | `false` | 否 | 可写 |
| readEncryptionRequired | `boolean` | `false` | 否 | 加密读请求 |
| writeEncryptionRequired | `boolean` | `false` | 否 | 加密写请求 |

<a id="descriptor"></a>

#### descriptor

描述符数据

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| uuid | `string` | 是 | Descriptor 的 UUID |
| permission | `descriptorPermission` | 否 | 描述符的权限 |
| value | `ArrayBuffer` | 是 | 描述符数据 |

<a id="descriptorpermission"></a>

#### descriptorPermission

描述符的权限

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| write | `boolean` | `false` | 否 | 写 |
| read | `boolean` | `false` | 否 | 读 |

<a id="close-1"></a>

### close

<a id="option-1"></a>

#### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用成功的回调函数 |

<a id="oncharacteristicreadrequest-1"></a>

### onCharacteristicReadRequest

<a id="callback"></a>

#### Callback

已连接的设备请求读当前外围设备的特征值事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="callbackresult"></a>

#### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| serviceId | `string` | 蓝牙特征对应服务的 UUID |
| characteristicId | `string` | 蓝牙特征的 UUID |
| callbackId | `number` | 唯一标识码，调用 [writeCharacteristicValue](../../../../apis/device/bluetooth-peripheral/BLEPeripheralServer.md#writecharacteristicvalue) 时使用 |

<a id="oncharacteristicsubscribed-1"></a>

### onCharacteristicSubscribed

<a id="callback-1"></a>

#### Callback

特征订阅事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="callbackresult-1"></a>

#### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| serviceId | `string` | 蓝牙特征对应服务的 UUID |
| characteristicId | `string` | 蓝牙特征的 UUID |

<a id="oncharacteristicunsubscribed-1"></a>

### onCharacteristicUnsubscribed

<a id="callback-2"></a>

#### Callback

取消特征订阅事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="callbackresult-2"></a>

#### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| serviceId | `string` | 蓝牙特征对应服务的 UUID |
| characteristicId | `string` | 蓝牙特征的 UUID |

<a id="oncharacteristicwriterequest-1"></a>

### onCharacteristicWriteRequest

<a id="callback-3"></a>

#### Callback

已连接的设备请求写当前外围设备的特征值事件的回调函数

```tsx
(result: CallbackResult) => void
```

| 参数 | 类型 |
| --- | --- |
| result | `CallbackResult` |

<a id="callbackresult-3"></a>

#### CallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| serviceId | `string` | 蓝牙特征对应服务的 UUID |
| characteristicId | `string` | 蓝牙特征的 UUID |
| callbackId | `number` | 唯一标识码，调用 [writeCharacteristicValue](../../../../apis/device/bluetooth-peripheral/BLEPeripheralServer.md#writecharacteristicvalue) 时使用 |
| value | `ArrayBuffer` | 请求写入特征的二进制数据值 |

<a id="removeservice-1"></a>

### removeService

<a id="option-2"></a>

#### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| serviceId | `string` | 是 | service 的 UUID |
| complete | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用成功的回调函数 |

<a id="startadvertising-1"></a>

### startAdvertising

<a id="option-3"></a>

#### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| advertiseRequest | `advertiseRequest` |  | 是 | 广播自定义参数 |
| powerLevel | `keyof PowerLevel` | `"medium"` | 否 | 广播功率 |
| complete | `(res: TaroGeneral.BluetoothError) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.BluetoothError) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.BluetoothError) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="advertiserequest"></a>

#### advertiseRequest

广播自定义参数

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| connectable | `boolean` | `true` | 否 | 当前设备是否可连接 |
| deviceName | `string` | `""` | 否 | 广播中 deviceName 字段，默认为空 |
| serviceUuids | `string[]` |  | 否 | 要广播的服务 UUID 列表。使用 16/32 位 UUID 时请参考注意事项。 |
| manufacturerData | `manufacturerData[]` |  | 否 | 广播的制造商信息。仅安卓支持，iOS 因系统限制无法定制。 |
| beacon | `beacon` |  | 否 | 以 beacon 设备形式广播的参数。 |

<a id="manufacturerdata"></a>

#### manufacturerData

广播的制造商信息。仅安卓支持，iOS 因系统限制无法定制。

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| manufacturerId | `string` | 是 | 制造商ID，0x 开头的十六进制 |
| manufacturerSpecificData | `ArrayBuffer` | 否 | 制造商信息 |

<a id="beacon"></a>

#### beacon

以 beacon 设备形式广播的参数。

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| uuid | `string` | 是 | Beacon 设备广播的 UUID |
| major | `number` | 是 | Beacon 设备的主 ID |
| minor | `number` | 是 | Beacon 设备的次 ID |
| measuredPower | `number` | 否 | 用于判断距离设备 1 米时 RSSI 大小的参考值 |

<a id="powerlevel"></a>

#### PowerLevel

广播功率合法值

| 参数 | 说明 |
| --- | --- |
| low | 功率低 |
| medium | 功率适中 |
| high | 功率高 |

<a id="stopadvertising-1"></a>

### stopAdvertising

<a id="option-4"></a>

#### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用成功的回调函数 |

<a id="writecharacteristicvalue-1"></a>

### writeCharacteristicValue

<a id="option-5"></a>

#### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| serviceId | `string` | 是 | 蓝牙特征对应服务的 UUID |
| characteristicId | `string` | 是 | 蓝牙特征的 UUID |
| value | `ArrayBuffer` | 是 | characteristic 对应的二进制值 |
| needNotify | `boolean` | 是 | 是否需要通知主机 value 已更新 |
| callbackId | `number` | 否 | 可选，处理回包时使用 |
| complete | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用成功的回调函数 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | 京东小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| BLEPeripheralServer | ✔️ |  |  |  |  |  |
| BLEPeripheralServer.addService | ✔️ | ✔️ |  |  |  |  |
| BLEPeripheralServer.close | ✔️ |  |  |  |  |  |
| BLEPeripheralServer.offCharacteristicReadRequest | ✔️ | ✔️ |  |  |  |  |
| BLEPeripheralServer.offCharacteristicSubscribed | ✔️ | ✔️ |  |  |  |  |
| BLEPeripheralServer.offCharacteristicUnsubscribed | ✔️ |  |  |  |  |  |
| BLEPeripheralServer.offCharacteristicWriteRequest | ✔️ | ✔️ |  |  |  |  |
| BLEPeripheralServer.onCharacteristicReadRequest | ✔️ | ✔️ |  |  |  |  |
| BLEPeripheralServer.onCharacteristicSubscribed | ✔️ | ✔️ |  |  |  |  |
| BLEPeripheralServer.onCharacteristicUnsubscribed | ✔️ | ✔️ |  |  |  |  |
| BLEPeripheralServer.onCharacteristicWriteRequest | ✔️ | ✔️ |  |  |  |  |
| BLEPeripheralServer.removeService | ✔️ | ✔️ |  |  |  |  |
| BLEPeripheralServer.startAdvertising | ✔️ | ✔️ |  |  |  |  |
| BLEPeripheralServer.stopAdvertising | ✔️ | ✔️ |  |  |  |  |
| BLEPeripheralServer.writeCharacteristicValue | ✔️ | ✔️ |  |  |  |  |
