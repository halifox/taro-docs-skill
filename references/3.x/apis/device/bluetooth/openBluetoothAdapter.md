# Taro.openBluetoothAdapter(option)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/device/bluetooth/openBluetoothAdapter)

初始化蓝牙模块

**注意**

- 其他蓝牙相关 API 必须在 Taro.openBluetoothAdapter 调用之后使用。否则 API 会返回错误（errCode=10000）。
- 在用户蓝牙开关未开启或者手机不支持蓝牙功能的情况下，调用 Taro.openBluetoothAdapter 监听手机蓝牙状态的改变，也可以调用蓝牙模块的所有API。

支持情况：微信小程序 支付宝小程序 京东小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/bluetooth/wx.openBluetoothAdapter.html)

<a id="类型"></a>

## 类型

```tsx
(option?: Option) => Promise<TaroGeneral.CallbackResult>
```

<a id="参数"></a>

## 参数

| 参数 | 类型 |
| --- | --- |
| option | `Option` |

<a id="option"></a>

### Option

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| mode | `keyof Mode` | 否 | 蓝牙模式，可作为主/从设备，仅 iOS 需要。 |
| complete | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.BluetoothError) => void` | 否 | 接口调用成功的回调函数 |

<a id="mode"></a>

### Mode

| 参数 | 说明 |
| --- | --- |
| central | 主机模式 |
| peripheral | 从机（外围设备）模式 |

<a id="state"></a>

### state

object.fail 回调函数返回的 state 参数（仅 iOS）

| 参数 | 说明 |
| --- | --- |
| 0 | 未知 |
| 1 | 重置中 |
| 2 | 不支持 |
| 3 | 未授权 |
| 4 | 未开启 |

<a id="示例代码"></a>

## 示例代码

```tsx
Taro.openBluetoothAdapter({
  success: function (res) {
    console.log(res)
  }
})
```
