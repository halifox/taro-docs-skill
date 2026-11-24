# AuthSetting

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/open-api/settings/AuthSetting)

用户授权设置信息，详情参考[权限](https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/authorize.html)

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/authorize.html)

<a id="方法"></a>

## 方法

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| scope.userInfo | `boolean` | 否 | 是否授权用户信息，对应接口 [Taro.getUserInfo](../user-info/getUserInfo.md) |
| scope.userLocation | `boolean` | 否 | 是否授权地理位置，对应接口 [Taro.getLocation](../../location/getLocation.md), [Taro.chooseLocation](../../location/chooseLocation.md) |
| scope.address | `boolean` | 否 | 是否授权通讯地址，对应接口 [Taro.chooseAddress](../address/chooseAddress.md) |
| scope.invoiceTitle | `boolean` | 否 | 是否授权发票抬头，对应接口 [Taro.chooseInvoiceTitle](../invoice/chooseInvoiceTitle.md) |
| scope.invoice | `boolean` | 否 | 是否授权获取发票，对应接口 [Taro.chooseInvoice](../invoice/chooseInvoice.md) |
| scope.werun | `boolean` | 否 | 是否授权微信运动步数，对应接口 [Taro.getWeRunData](../werun/getWeRunData.md) |
| scope.record | `boolean` | 否 | 是否授权录音功能，对应接口 [Taro.startRecord](../../media/recorder/startRecord.md) |
| scope.writePhotosAlbum | `boolean` | 否 | 是否授权保存到相册 [Taro.saveImageToPhotosAlbum](../../media/image/saveImageToPhotosAlbum.md), [Taro.saveVideoToPhotosAlbum](../../media/video/saveVideoToPhotosAlbum.md) |
| scope.camera | `boolean` | 否 | 是否授权摄像头，对应 [camera](../../../components/media/camera.md) 组件 |
| scope.bluetoothBackground | `boolean` | 否 | 是否授权小程序在后台运行蓝牙，对应接口 [Taro.openBluetoothAdapterBackground](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/setting/%28wx.openBluetoothAdapterBackground%29.html) |
