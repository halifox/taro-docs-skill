# MapContext

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/apis/media/map/MapContext)

`MapContext` 实例，可通过 [Taro.createMapContext](createMapContext.md) 获取。
`MapContext` 通过 id 跟一个 map 组件绑定，操作对应的 map 组件。

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.html)

<a id="方法"></a>

## 方法

<a id="getcenterlocation"></a>

### getCenterLocation

获取当前地图中心的经纬度。返回的是 gcj02 坐标系，可以用于 [Taro.openLocation()](../../location/openLocation.md)

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.getCenterLocation.html)

```tsx
(option?: GetCenterLocationOption) => Promise<GetCenterLocationSuccessCallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `GetCenterLocationOption` |

<a id="setlocmarkericon"></a>

### setLocMarkerIcon

设置定位点图标，支持网络路径、本地路径、代码包路径

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.setLocMarkerIcon.html)

```tsx
(option?: SetLocMarkerIconOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `SetLocMarkerIconOption` |

<a id="movetolocation"></a>

### moveToLocation

将地图中心移置当前定位点，此时需设置地图组件 show-location 为true。

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.moveToLocation.html)

```tsx
(option: MoveToLocationOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `MoveToLocationOption` |

<a id="translatemarker"></a>

### translateMarker

平移marker，带动画

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.translateMarker.html)

```tsx
(option: TranslateMarkerOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `TranslateMarkerOption` |

<a id="movealong"></a>

### moveAlong

沿指定路径移动 marker，用于轨迹回放等场景。动画完成时触发回调事件，若动画进行中，对同一 marker 再次调用 moveAlong 方法，前一次的动画将被打断。

```tsx
(object: any) => any
```

<a id="includepoints"></a>

### includePoints

缩放视野展示所有经纬度

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.includePoints.html)

```tsx
(option: IncludePointsOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `IncludePointsOption` |

<a id="getregion"></a>

### getRegion

获取当前地图的视野范围

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.getRegion.html)

```tsx
(option?: GetRegionOption) => Promise<GetRegionSuccessCallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `GetRegionOption` |

<a id="getrotate"></a>

### getRotate

获取当前地图的旋转角

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.getRotate.html)

```tsx
(option?: GetRotateOption) => Promise<GetRotateSuccessCallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `GetRotateOption` |

<a id="getskew"></a>

### getSkew

获取当前地图的倾斜角

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.getSkew.html)

```tsx
(option?: GetSkewOption) => Promise<GetSkewSuccessCallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `GetSkewOption` |

<a id="getscale"></a>

### getScale

获取当前地图的缩放级别

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.getScale.html)

```tsx
(option?: GetScaleOption) => Promise<GetScaleSuccessCallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `GetScaleOption` |

<a id="setcenteroffset"></a>

### setCenterOffset

设置地图中心点偏移，向后向下为增长，屏幕比例范围(0.25~0.75)，默认偏移为[0.5, 0.5]

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.setCenterOffset.html)

```tsx
(option: SetCenterOffsetOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `SetCenterOffsetOption` |

<a id="removecustomlayer"></a>

### removeCustomLayer

移除个性化图层。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.removeCustomLayer.html)

```tsx
(option: RemoveCustomLayerOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `RemoveCustomLayerOption` |

<a id="addcustomlayer"></a>

### addCustomLayer

添加个性化图层。图层创建参考文档

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.addCustomLayer.html)

```tsx
(option: AddCustomLayerOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `AddCustomLayerOption` |

<a id="addgroundoverlay"></a>

### addGroundOverlay

创建自定义图片图层，图片会随着地图缩放而缩放。

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.addGroundOverlay.html)

```tsx
(option: AddGroundLayerOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `AddGroundLayerOption` |

<a id="addvisuallayer"></a>

### addVisualLayer

添加可视化图层。需要刷新时，interval 可设置的最小值为 15 s。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.addVisualLayer.html)

```tsx
(option: AddVisualLayerOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `AddVisualLayerOption` |

<a id="removevisuallayer"></a>

### removeVisualLayer

移除可视化图层。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.removeVisualLayer.html)

```tsx
(option: RemoveVisualLayerOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `RemoveVisualLayerOption` |

<a id="addarc"></a>

### addArc

添加弧线，途经点与夹角必须设置一个。途经点必须在起终点有效坐标范围内，否则不能生成正确的弧线，同时设置夹角角度时，以夹角角度为准。夹角定义为起点到终点，与起点外切线逆时针旋转的角度。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.addArc.html)

```tsx
(option: AddArcOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `AddArcOption` |

<a id="removearc"></a>

### removeArc

删除弧线。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.removeArc.html)

```tsx
(option: RemoveArcOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `RemoveArcOption` |

<a id="setboundary"></a>

### setBoundary

限制地图的显示范围。此接口同时会限制地图的最小缩放整数级别。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.setBoundary.html)

```tsx
(option: SetBoundaryOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `SetBoundaryOption` |

<a id="updategroundoverlay"></a>

### updateGroundOverlay

更新自定义图片图层。

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.updateGroundOverlay.html)

```tsx
(option: UpdateGroundOverlayOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `UpdateGroundOverlayOption` |

<a id="removegroundoverlay"></a>

### removeGroundOverlay

移除自定义图片图层。

支持情况：微信小程序 抖音小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.removeGroundOverlay.html)

```tsx
(option: RemoveGroundOverlayOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `RemoveGroundOverlayOption` |

<a id="toscreenlocation"></a>

### toScreenLocation

获取经纬度对应的屏幕坐标，坐标原点为地图左上角。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.toScreenLocation.html)

```tsx
(option: ToScreenLocationOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `ToScreenLocationOption` |

<a id="fromscreenlocation"></a>

### fromScreenLocation

获取屏幕上的点对应的经纬度，坐标原点为地图左上角。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.fromScreenLocation.html)

```tsx
(option: FromScreenLocationOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `FromScreenLocationOption` |

<a id="openmapapp"></a>

### openMapApp

拉起地图APP选择导航。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.openMapApp.html)

```tsx
(option: OpenMapAppOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `OpenMapAppOption` |

<a id="addmarkers"></a>

### addMarkers

添加 marker。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.addMarkers.html)

```tsx
(option: AddMarkersOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `AddMarkersOption` |

<a id="removemarkers"></a>

### removeMarkers

移除 marker。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.removeMarkers.html)

```tsx
(option: RemoveMarkersOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `RemoveMarkersOption` |

<a id="initmarkercluster"></a>

### initMarkerCluster

初始化点聚合的配置，未调用时采用默认配置。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.initMarkerCluster.html)

```tsx
(option?: InitMarkerClusterOption) => Promise<TaroGeneral.CallbackResult>
```

| 参数 | 类型 |
| --- | --- |
| option | `InitMarkerClusterOption` |

<a id="on"></a>

### on

监听地图事件。

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/media/map/MapContext.on.html)

```tsx
(event: keyof MapEvent, callback: (res: MapEventMarkerClusterCreate | MapEventMarkerClusterClick) => void) => void
```

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| event | `keyof MapEvent` | 事件名 |
| callback | (res: MapEventMarkerClusterCreate or MapEventMarkerClusterClick) => void | 事件的回调函数 |

<a id="示例代码"></a>

#### 示例代码

```tsx
MapContext.on('markerClusterCreate', (res) => {})
MapContext.on('markerClusterClick', (res) => {})
```

<a id="参数"></a>

## 参数

<a id="getcenterlocationoption"></a>

### GetCenterLocationOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: GetCenterLocationSuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="getcenterlocationsuccesscallbackresult"></a>

### GetCenterLocationSuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| latitude | `number` | 纬度 |
| longitude | `number` | 经度 |
| errMsg | `string` | 调用结果 |

<a id="setlocmarkericonoption"></a>

### SetLocMarkerIconOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| iconPath | `string` | 是 | 图标路径，支持网络路径、本地路径、代码包路径 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="getregionoption"></a>

### GetRegionOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: GetRegionSuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="getregionsuccesscallbackresult"></a>

### GetRegionSuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| northeast | `MapPosition` | 东北角经纬度 |
| southwest | `MapPosition` | 西南角经纬度 |

<a id="getrotateoption"></a>

### GetRotateOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: GetRotateSuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="getrotatesuccesscallbackresult"></a>

### GetRotateSuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| rotate | `number` | 旋转角 |
| errMsg | `string` | 调用结果 |

<a id="getscaleoption"></a>

### GetScaleOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: GetScaleSuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="getscalesuccesscallbackresult"></a>

### GetScaleSuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| scale | `number` | 缩放值 |
| errMsg | `string` | 调用结果 |

<a id="getskewoption"></a>

### GetSkewOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(result: GetSkewSuccessCallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="getskewsuccesscallbackresult"></a>

### GetSkewSuccessCallbackResult

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| skew | `number` | 倾斜角 |
| errMsg | `string` | 调用结果 |

<a id="includepointsoption"></a>

### IncludePointsOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| points | `MapPosition[]` | 是 | 要显示在可视区域内的坐标点列表 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| padding | `number[]` | 否 | 坐标点形成的矩形边缘到地图边缘的距离，单位像素。格式为[上,右,下,左]，安卓上只能识别数组第一项，上下左右的padding一致。开发者工具暂不支持padding参数。 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="mapposition"></a>

### MapPosition

坐标点

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| latitude | `number` | 纬度 |
| longitude | `number` | 经度 |

<a id="mapboundary"></a>

### MapBoundary

经纬度范围

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| southwest | `MapPosition` | 西南角经纬度 |
| northeast | `MapPosition` | 东北角经纬度 |

<a id="movetolocationoption"></a>

### MoveToLocationOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| latitude | `number` | 否 | 纬度 |
| longitude | `number` | 否 | 经度 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="translatemarkeroption"></a>

### TranslateMarkerOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| autoRotate | `boolean` | 是 | 移动过程中是否自动旋转 marker |
| destination | `MapPosition` | 是 | 指定 marker 移动到的目标点 |
| markerId | `number` | 是 | 指定 marker |
| rotate | `number` | 是 | marker 的旋转角度 |
| animationEnd | `(...args: any[]) => any` | 否 | 动画结束回调函数 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| duration | `number` | 否 | 动画持续时长，平移与旋转分别计算 |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="setcenteroffsetoption"></a>

### SetCenterOffsetOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| offset | `number[]` | 是 | 偏移量，两位数组 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="removecustomlayeroption"></a>

### RemoveCustomLayerOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| layerId | `number` | 是 | 个性化图层id |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="addcustomlayeroption"></a>

### AddCustomLayerOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| layerId | `number` | 是 | 个性化图层id |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="addgroundlayeroption"></a>

### AddGroundLayerOption

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| id | `number` |  | 是 | 图片图层 id |
| src | `string` |  | 是 | 图片路径，支持网络图片、临时路径、代码包路径 |
| bounds | `MapBoundary` |  | 是 | 图片覆盖的经纬度范围 |
| visible | `boolean` | `true` | 否 | 是否可见 |
| zIndex | `number` | `1` | 否 | 图层绘制顺序 |
| opacity | `number` | `1` | 否 | 图层透明度 |
| complete | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="addvisuallayeroption"></a>

### AddVisualLayerOption

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| layerId | `number` |  | 是 | 个性化图层id（[创建图层指引](https://lbs.qq.com/dev/console/layers/layerEdit)) |
| interval | `number` | `0` | 否 | 刷新周期，单位秒 |
| zIndex | `number` | `1` | 否 | 图层绘制顺序 |
| opacity | `number` | `1` | 否 | 图层透明度 |
| complete | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="removevisuallayeroption"></a>

### RemoveVisualLayerOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| layerId | `number` | 是 | 可视化图层 id |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="addarcoption"></a>

### AddArcOption

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| id | `number` |  | 是 | 圆弧 id |
| start | `MapPosition` |  | 是 | 起始点 |
| end | `MapPosition` |  | 是 | 终点 |
| pass | `MapPosition` |  | 否 | 途经点 |
| angle | `number` | `0` | 否 | 夹角角度 |
| width | `number` | `5` | 否 | 线宽 |
| color | `string` | `"#000000"` | 否 | 线的颜色 |
| complete | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="removearcoption"></a>

### RemoveArcOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| id | `number` | 是 | 圆弧 id |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="setboundaryoption"></a>

### SetBoundaryOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| southwest | `MapPosition` | 是 | 西南角经纬度 |
| northeast | `MapPosition` | 是 | 东北角经纬度 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="updategroundoverlayoption"></a>

### UpdateGroundOverlayOption

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| id | `number` |  | 是 | 图片图层 id |
| src | `string` |  | 是 | 图片路径，支持网络图片、临时路径、代码包路径 |
| bounds | `MapBoundary` |  | 是 | 图片覆盖的经纬度范围 |
| visible | `boolean` | `true` | 否 | 是否可见 |
| zIndex | `number` | `1` | 否 | 图层绘制顺序 |
| opacity | `number` | `1` | 否 | 图层透明度 |
| complete | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="removegroundoverlayoption"></a>

### RemoveGroundOverlayOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| id | `number` | 是 | 图片图层 id |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="toscreenlocationoption"></a>

### ToScreenLocationOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| latitude | `number` | 是 | 纬度 |
| longitude | `number` | 是 | 经度 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="fromscreenlocationoption"></a>

### FromScreenLocationOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| x | `number` | 是 | x 坐标值 |
| y | `number` | 是 | y 坐标值 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="openmapappoption"></a>

### OpenMapAppOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| longitude | `number` | 是 | 目的地经度 |
| latitude | `number` | 是 | 目的地纬度 |
| destination | `string` | 是 | 目的地名称 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="addmarkersoption"></a>

### AddMarkersOption

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| markers | `MapProps.marker[]` |  | 是 | 同传入 map 组件的 marker 属性 |
| clear | `boolean` | `false` | 否 | 是否先清空地图上所有 marker |
| complete | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="removemarkersoption"></a>

### RemoveMarkersOption

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| markerIds | `string[]` | 是 | marker 的 id 集合。 |
| complete | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` | 否 | 接口调用成功的回调函数 |

<a id="initmarkerclusteroption"></a>

### InitMarkerClusterOption

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| enableDefaultStyle | `boolean` | `true` | 否 | 启用默认的聚合样式 |
| zoomOnClick | `boolean` | `true` | 否 | 点击已经聚合的标记点时是否实现聚合分离 |
| gridSize | `number` | `60` | 否 | 聚合算法的可聚合距离，即距离小于该值的点会聚合至一起，以像素为单位 |
| complete | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(res: TaroGeneral.CallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |

<a id="mapevent"></a>

### MapEvent

event 的合法值

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| markerClusterCreate | `MapEventMarkerClusterCreate` | 缩放或拖动导致新的聚合簇产生时触发，仅返回新创建的聚合簇信息 |
| markerClusterClick | `MapEventMarkerClusterClick` | 聚合簇的点击事件 |

<a id="mapeventmarkerclustercreate"></a>

### MapEventMarkerClusterCreate

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| clusters | `ClusterInfo[]` | 聚合簇数据 |

<a id="mapeventmarkerclusterclick"></a>

### MapEventMarkerClusterClick

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| cluster | `ClusterInfo` | 聚合簇 |

<a id="clusterinfo"></a>

### ClusterInfo

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| clusterId | `number` | 聚合簇的 id |
| center | `LatLng` | 聚合簇的坐标 |
| markerIds | `string[]` | 该聚合簇内的点标记数据数组 |

<a id="latlng"></a>

### LatLng

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| lat | `number` | 纬度值 |
| lng | `number` | 经度值 |

<a id="api-支持度"></a>

## API 支持度

| API | 微信小程序 | 抖音小程序 | H5 | React Native | Harmony | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| MapContext | ✔️ | ✔️ |  |  |  | ✔️ |
| MapContext.getCenterLocation | ✔️ | ✔️ |  |  |  | ✔️ |
| MapContext.setLocMarkerIcon | ✔️ | ✔️ |  |  |  |  |
| MapContext.moveToLocation | ✔️ | ✔️ |  |  |  | ✔️ |
| MapContext.translateMarker | ✔️ | ✔️ |  |  |  | ✔️ |
| MapContext.includePoints | ✔️ | ✔️ |  |  |  | ✔️ |
| MapContext.getRegion | ✔️ | ✔️ |  |  |  | ✔️ |
| MapContext.getRotate | ✔️ | ✔️ |  |  |  | ✔️ |
| MapContext.getSkew | ✔️ | ✔️ |  |  |  | ✔️ |
| MapContext.getScale | ✔️ | ✔️ |  |  |  | ✔️ |
| MapContext.setCenterOffset | ✔️ | ✔️ |  |  |  |  |
| MapContext.removeCustomLayer | ✔️ |  |  |  |  |  |
| MapContext.addCustomLayer | ✔️ |  |  |  |  |  |
| MapContext.addGroundOverlay | ✔️ | ✔️ |  |  |  |  |
| MapContext.addVisualLayer | ✔️ |  |  |  |  |  |
| MapContext.removeVisualLayer | ✔️ |  |  |  |  |  |
| MapContext.addArc | ✔️ |  |  |  |  |  |
| MapContext.removeArc | ✔️ |  |  |  |  |  |
| MapContext.setBoundary | ✔️ |  |  |  |  |  |
| MapContext.updateGroundOverlay | ✔️ | ✔️ |  |  |  |  |
| MapContext.removeGroundOverlay | ✔️ | ✔️ |  |  |  |  |
| MapContext.toScreenLocation | ✔️ |  |  |  |  |  |
| MapContext.fromScreenLocation | ✔️ |  |  |  |  |  |
| MapContext.openMapApp | ✔️ |  |  |  |  |  |
| MapContext.addMarkers | ✔️ |  |  |  |  |  |
| MapContext.removeMarkers | ✔️ |  |  |  |  |  |
| MapContext.initMarkerCluster | ✔️ |  |  |  |  |  |
| MapContext.on | ✔️ |  |  |  |  |  |
