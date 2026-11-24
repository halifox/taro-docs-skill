# Taro.chooseLocation(param)

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/1.x/apis/location/chooseLocation)

打开地图选择位置。

使用方式同 [`wx.chooseLocation`](https://developers.weixin.qq.com/miniprogram/dev/api/wx.chooseLocation.html)，支持 `Promise` 化使用。

<a id="使用前注意"></a>

## 使用前注意

`chooseLocation` api功能是依赖于腾讯位置服务，所以需要使用 api 密钥。如果您没有，可以前往腾讯位置服务[开发者控制台](https://lbs.qq.com/console/mykey.html?console=mykey)进行申请。

获得 api 密钥后，您需要将它填入项目的常量配置`defineConstants.LOCATION_APIKEY`中：

```javascript
// config/index.js

const config = {
  defineConstants: {
    LOCATION_APIKEY: JSON.stringify('XXXXX-XXXXX-XXXXX-XXXXX-XXXXX-XXXXX')
  },
  // ...
}
```

<a id="参数"></a>

## 参数

<a id="object-param"></a>

### object param

| Property | Type | Description |
| --- | --- | --- |
| [success] | [`function`](#successobj) | 接口调用成功的回调函数 |
| [fail] | `function` | 接口调用失败的回调函数 |
| [complete] | `function` | 接口调用结束的回调函数（调用成功、失败都会执行） |

<a id="参数-1"></a>

#### 参数

<a id="successobj"></a>

##### success(obj)

| Name | Type | Description |
| --- | --- | --- |
| name | `string` | 位置名称 |
| address | `string` | 详细地址 |
| latitude | `string` | 纬度，浮点数，范围为-90~90，负数表示南纬。使用 gcj02 国测局坐标系 |
| longitude | `string` | 经度，浮点数，范围为-180~180，负数表示西经。使用 gcj02 国测局坐标系 |

<a id="示例代码"></a>

## 示例代码

```jsx
import Taro from '@tarojs/taro'

Taro.chooseLocation(params).then(...)
```

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | H5 | React Native |
| --- | --- | --- | --- |
| Taro.chooseLocation | ✔️ | ✔️ |  |
