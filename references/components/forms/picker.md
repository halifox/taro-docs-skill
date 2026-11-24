# Picker

[原始页面](https://taro-docs-7g1t02tzaeb163c4-1252004765.tcloudbaseapp.com/docs/components/forms/picker)

从底部弹起的滚动选择器

支持情况：微信小程序 百度小程序 支付宝小程序 抖音小程序 H5 ASCF元服务 React Native Harmony Harmony hybrid

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/picker.html)

<a id="类型"></a>

## 类型

```tsx
ComponentType<PickerSelectorProps | PickerMultiSelectorProps | PickerTimeProps | PickerDateProps | PickerRegionProps>
```

<a id="示例代码"></a>

## 示例代码

**React**

```tsx
export default class PagePicker extends Component {
  state = {
    selector: ['美国', '中国', '巴西', '日本'],
    selectorChecked: '美国',
    timeSel: '12:01',
    dateSel: '2018-04-22'
  }

  onChange = e => {
    this.setState({
      selectorChecked: this.state.selector[e.detail.value]
    })
  }

  onTimeChange = e => {
    this.setState({
      timeSel: e.detail.value
    })
  }
  onDateChange = e => {
    this.setState({
      dateSel: e.detail.value
    })
  }

  render () {
    return (
      <View className='container'>
        <View className='page-body'>
          <View className='page-section'>
            <Text>地区选择器</Text>
            <View>
              <Picker mode='selector' range={this.state.selector} onChange={this.onChange}>
                <View className='picker'>
                  当前选择：{this.state.selectorChecked}
                </View>
              </Picker>
            </View>
          </View>
          <View className='page-section'>
            <Text>时间选择器</Text>
            <View>
              <Picker mode='time' onChange={this.onTimeChange}>
                <View className='picker'>
                  当前选择：{this.state.timeSel}
                </View>
              </Picker>
            </View>
          </View>
          <View className='page-section'>
            <Text>日期选择器</Text>
            <View>
              <Picker mode='date' onChange={this.onDateChange}>
                <View className='picker'>
                  当前选择：{this.state.dateSel}
                </View>
              </Picker>
            </View>
          </View>
        </View>
      </View>
    )
  }
}
```

**Vue**

```html
<template>
  <view class="page-body">
    <view class="page-section">
      <text>地区选择器</text>
      <view>
        <picker mode="selector" :range="selector" @change="onChange">
          <view class="picker">
            当前选择：{{selectorChecked}}
          </view>
        </picker>
      </view>
    </view>
    <view class="page-section">
      <text>时间选择器</text>
      <view>
        <picker mode="time" @change="onTimeChange">
          <view class="picker">
            当前选择：{{timeSel}}
          </view>
        </picker>
      </view>
    </view>
    <view class="page-section">
      <text>日期选择器</text>
      <view>
        <picker mode="date" @change="onDateChange">
          <view class="picker">
            当前选择：{{dateSel}}
          </view>
        </picker>
      </view>
    </view>
  </view>
</template>

<script>
  export default {
    data() {
      return {
        selector: ['美国', '中国', '巴西', '日本'],
        selectorChecked: '美国',
        timeSel: '12:01',
        dateSel: '2018-04-22'
      }
    },
    methods: {
      onChange: function(e) {
        this.selectorChecked = this.selector[e.detail.value]
      },

      onTimeChange: function(e) {
        this.timeSel = e.detail.value
      },

      onDateChange: function(e) {
        this.dateSel = e.detail.value
      }
    }
  }
</script>
```

<a id="pickerstandardprops"></a>

## PickerStandardProps

选择器通用参数

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| headerText | `string` |  | 否 | 选择器的标题，微信小程序中仅安卓可用 |
| mode | `keyof Mode` | `"selector"` | 否 | 选择器类型，默认是普通选择器 |
| disabled | `boolean` | `false` | 否 | 是否禁用 |
| onCancel | `CommonEventFunction` |  | 否 | 取消选择或点遮罩层收起 picker 时触发 |
| textProps | `PickerText` |  | 否 | 用于替换组件内部文本 |

<a id="api-支持度"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| PickerStandardProps.headerText | ✔️ |  |  |  |  |  |
| PickerStandardProps.mode | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerStandardProps.disabled | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| PickerStandardProps.onCancel | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerStandardProps.textProps |  | ✔️ |  | ✔️ | ✔️ |  |

<a id="mode"></a>

### Mode

选择器类型

| 参数 | 说明 |
| --- | --- |
| selector | 普通选择器 |
| multiSelector | 多列选择器 |
| time | 时间选择器 |
| date | 日期选择器 |
| region | 省市区选择器 |

<a id="pickertext"></a>

### PickerText

| 参数 | 类型 | 必填 |
| --- | --- | --- |
| okText | `string` | 否 |
| cancelText | `string` | 否 |

<a id="pickerselectorprops"></a>

## PickerSelectorProps

普通选择器：mode = selector

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| mode | `"selector"` |  | 否 | 选择器类型 |
| range | string[] or number[] or Record<string, any>[] | `[]` | 是 | mode为 selector 或 multiSelector 时，range 有效 |
| rangeKey | `string` |  | 否 | 当 range 是一个 Object Array 时，通过 rangeKey 来指定 Object 中 key 的值作为选择器显示内容 |
| value | `number` | `0` | 否 | 表示选择了 range 中的第几个（下标从 0 开始） |
| defaultValue | `number` |  | 否 | 设置 React 非受控状态下的初始取值 |
| itemStyle | `StyleProp<TextStyle>` | `{}` | 否 | mode为 selector 或 multiSelector 时 itemStyle 有效 |
| indicatorStyle | `StyleProp<ViewStyle>` | `{}` | 否 | mode为 selector 或 multiSelector 时 indicatorStyle 有效 |
| onChange | `CommonEventFunction<ChangeEventDetail>` |  | 否 | value 改变时触发 change 事件 |

<a id="api-支持度-1"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| PickerSelectorProps.range | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerSelectorProps.rangeKey | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerSelectorProps.value | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerSelectorProps.defaultValue | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| PickerSelectorProps.itemStyle |  |  | ✔️ |  |  |  |
| PickerSelectorProps.indicatorStyle |  |  | ✔️ |  |  |  |
| PickerSelectorProps.onChange | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |

<a id="changeeventdetail"></a>

### ChangeEventDetail

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| value | string or number | 表示变更值的下标 |

<a id="pickermultiselectorprops"></a>

## PickerMultiSelectorProps

多列选择器：mode = multiSelector

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| mode | `"multiSelector"` |  | 是 | 选择器类型 |
| range | string[][] or number[][] or Record<string, any>[][] | `[]` | 是 | mode为 selector 或 multiSelector 时，range 有效 |
| rangeKey | `string` |  | 否 | 当 range 是一个 Object Array 时，通过 rangeKey 来指定 Object 中 key 的值作为选择器显示内容 |
| value | string[] or number[] or Record<string, any>[] | `[]` | 是 | 表示选择了 range 中的第几个（下标从 0 开始） |
| itemStyle | `StyleProp<TextStyle>` | `{}` | 否 | mode为 selector 或 multiSelector 时 itemStyle 有效 |
| indicatorStyle | `StyleProp<ViewStyle>` | `{}` | 否 | mode为 selector 或 multiSelector 时 indicatorStyle 有效 |
| onChange | `CommonEventFunction<ChangeEventDetail>` |  | 是 | 当 value 改变时触发 change 事件 |
| onColumnChange | `CommonEventFunction<ColumnChangeEventDetail>` |  | 否 | 列改变时触发 |

<a id="api-支持度-2"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| PickerMultiSelectorProps.range | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerMultiSelectorProps.rangeKey | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerMultiSelectorProps.value | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerMultiSelectorProps.itemStyle |  |  | ✔️ |  |  |  |
| PickerMultiSelectorProps.indicatorStyle |  |  | ✔️ |  |  |  |
| PickerMultiSelectorProps.onChange | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerMultiSelectorProps.onColumnChange | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |

<a id="changeeventdetail-1"></a>

### ChangeEventDetail

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| value | `number[]` | 表示变更值的下标 |

<a id="columnchangeeventdetail"></a>

### ColumnChangeEventDetail

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| column | `number` | 表示改变了第几列（下标从0开始） |
| value | `number` | 表示变更值的下标 |

<a id="pickertimeprops"></a>

## PickerTimeProps

时间选择器：mode = time

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| mode | `"time"` | 是 | 选择器类型 |
| value | `string` | 否 | value 的值表示选择了 range 中的第几个（下标从 0 开始） |
| defaultValue | `string` | 否 | 设置 React 非受控状态下的初始取值 |
| start | `string` | 否 | 仅当 mode 为 "time" 或 "date" 时有效，表示有效时间范围的开始，字符串格式为"hh:mm" |
| end | `string` | 否 | 仅当 mode 为 "time" 或 "date" 时有效，表示有效时间范围的结束，字符串格式为"hh:mm" |
| onChange | `CommonEventFunction<ChangeEventDetail>` | 是 | value 改变时触发 change 事件 |

<a id="api-支持度-3"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| PickerTimeProps.value | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerTimeProps.defaultValue | ✔️ | ✔️ | ✔️ |  |  | ✔️ |
| PickerTimeProps.start | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerTimeProps.end | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerTimeProps.onChange | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |

<a id="changeeventdetail-2"></a>

### ChangeEventDetail

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| value | `string` | 表示选中的时间 |

<a id="pickerdateprops"></a>

## PickerDateProps

日期选择器：mode = date

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| mode | `"date"` |  | 是 | 选择器类型 |
| value | `string` | `0` | 是 | 表示选中的日期，格式为"YYYY-MM-DD" |
| defaultValue | `string` |  | 否 | 设置 React 非受控状态下的初始取值 |
| start | `string` |  | 否 | 仅当 mode 为 "time" 或 "date" 时有效，表示有效时间范围的开始，字符串格式为"YYYY-MM-DD" |
| end | `string` |  | 否 | 仅当 mode 为 "time" 或 "date" 时有效，表示有效时间范围的结束，字符串格式为"YYYY-MM-DD" |
| fields | `keyof Fields` | `"day"` | 否 | 有效值 year, month, day，表示选择器的粒度 |
| onChange | `CommonEventFunction<ChangeEventDetail>` |  | 是 | value 改变时触发 change 事件 |

<a id="api-支持度-4"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| PickerDateProps.value | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerDateProps.defaultValue | ✔️ | ✔️ | ✔️ |  |  | ✔️ |
| PickerDateProps.start | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerDateProps.end | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| PickerDateProps.fields | ✔️ | ✔️ | ✔️ |  | ✔️ |  |
| PickerDateProps.onChange | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |

<a id="fields"></a>

### Fields

| 参数 | 说明 |
| --- | --- |
| year | 选择器粒度为年 |
| month | 选择器粒度为月份 |
| day | 选择器粒度为天 |

<a id="changeeventdetail-3"></a>

### ChangeEventDetail

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| value | `string` | 表示选中的日期 |

<a id="pickerregionprops"></a>

## PickerRegionProps

省市区选择器：mode = region

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | --- | --- | --- |
| mode | `"region"` |  | 是 | 选择器类型 |
| value | `string[]` | `[]` | 否 | 表示选中的省市区，默认选中每一列的第一个值 |
| defaultValue | `string[]` |  | 否 | 设置 React 非受控状态下的初始取值 |
| customItem | `string` |  | 否 | 可为每一列的顶部添加一个自定义的项 |
| level | `keyof Level` | `"region"` | 否 | 选择器层级 |
| regionData | `RegionData[]` |  | 否 | 自定义省市区数据 |
| onChange | `CommonEventFunction<ChangeEventDetail>` |  | 是 | value 改变时触发 change 事件 |

<a id="api-支持度-5"></a>

### API 支持度

| API | 微信小程序 | H5 | React Native | Harmony | Harmony hybrid | ASCF元服务 |
| --- | --- | --- | --- | --- | --- | --- |
| PickerRegionProps.value | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |
| PickerRegionProps.defaultValue | ✔️ | ✔️ | ✔️ |  |  | ✔️ |
| PickerRegionProps.customItem | ✔️ | ✔️ | ✔️ |  | ✔️ |  |
| PickerRegionProps.level | ✔️ |  |  |  |  |  |
| PickerRegionProps.regionData |  |  | ✔️ |  |  |  |
| PickerRegionProps.onChange | ✔️ | ✔️ | ✔️ |  | ✔️ | ✔️ |

<a id="changeeventdetail-4"></a>

### ChangeEventDetail

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| value | `string[]` | 是 | 表示选中的省市区 |
| code | `string[]` | 是 | 统计用区划代码 |
| postcode | `string` | 否 | 邮政编码 |

<a id="regiondata"></a>

### RegionData

| 参数 | 类型 | 必填 |
| --- | --- | --- |
| value | `string` | 是 |
| code | `string` | 是 |
| postcode | `string` | 否 |
| children | `RegionData[]` | 否 |

<a id="level"></a>

### Level

| 参数 | 说明 |
| --- | --- |
| province | 省级选择器 |
| city | 市级选择器 |
| region | 区级选择器 |
| sub-district | 街道选择器 |
