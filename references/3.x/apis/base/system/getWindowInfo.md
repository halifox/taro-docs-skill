# Taro.getWindowInfo()

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/3.x/apis/base/system/getWindowInfo)

获取窗口信息

支持情况：微信小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> H5: 不支持 statusBarHeight、safeArea

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/base/system/wx.getWindowInfo.html)

<a id="类型"></a>

## 类型

```tsx
() => Result
```

<a id="参数"></a>

## 参数

<a id="result"></a>

### Result

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| pixelRatio | `number` | 是 | 设备像素比 |
| screenWidth | `number` | 是 | 屏幕宽度，单位px |
| screenHeight | `number` | 是 | 屏幕高度，单位px |
| windowWidth | `number` | 是 | 可使用窗口宽度，单位px |
| windowHeight | `number` | 是 | 可使用窗口高度，单位px |
| statusBarHeight | `number` | 否 | 状态栏的高度，单位px |
| safeArea | `TaroGeneral.SafeAreaResult` | 否 | 在竖屏正方向下的安全区域 |

<a id="示例代码"></a>

## 示例代码

```tsx
const windowInfo = Taro.getWindowInfo()

console.log(windowInfo.pixelRatio)
console.log(windowInfo.screenWidth)
console.log(windowInfo.screenHeight)
console.log(windowInfo.windowWidth)
console.log(windowInfo.windowHeight)
console.log(windowInfo.statusBarHeight)
console.log(windowInfo.safeArea)
console.log(windowInfo.screenTop)
```
