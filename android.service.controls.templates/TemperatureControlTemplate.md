# TemperatureControlTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TemperatureControlTemplate

Kotlin| [Java](https://developer.android.com/reference/android/service/controls/templates/TemperatureControlTemplate "View this page in Java") 
| --- | --- |

```
class TemperatureControlTemplate : ControlTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.service.controls.templates.ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate) ||
| | ↳ | [android.service.controls.templates.TemperatureControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#) |

A template for a temperature related [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) that supports multiple modes. Both the current mode and the active mode for the control can be specified. The combination of the [Control.getDeviceType](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#getDeviceType())and the current and active mode will determine colors and transitions for the UI element.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_MODE_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#FLAG_MODE_COOL:kotlin.Int) Flag to indicate that the device supports cool mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_MODE_ECO](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#FLAG_MODE_ECO:kotlin.Int) Flag to indicate that the device supports eco mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_MODE_HEAT](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#FLAG_MODE_HEAT:kotlin.Int) Flag to indicate that the device supports heat mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_MODE_HEAT_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#FLAG_MODE_HEAT_COOL:kotlin.Int) Flag to indicate that the device supports heat-cool mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_MODE_OFF](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#FLAG_MODE_OFF:kotlin.Int) Flag to indicate that the device supports off mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_COOL:kotlin.Int) Indicates that the current or active mode of the device is set to cool. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_ECO](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_ECO:kotlin.Int) Indicates that the current or active mode of the device is set to eco. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_HEAT](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT:kotlin.Int) Indicates that the current or active mode of the device is set to heat. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_HEAT_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT_COOL:kotlin.Int) Indicates that the current or active mode of the device is set to heat-cool. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_OFF](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_OFF:kotlin.Int) Indicates that the current or active mode of the device is off. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_UNKNOWN:kotlin.Int) Use when the current or active mode of the device is not known Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_UNKNOWN:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_OFF:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_COOL:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT_COOL:kotlin.Int), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_ECO:kotlin.Int) |

| Inherited constants ||
|---|---|
| From class [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int) <br /> Type identifier of the template returned by [getErrorTemplate()](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#getErrorTemplate()). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int) <br /> Type identifier of [ControlTemplate.getNoTemplateObject](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#getNoTemplateObject()). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int) <br /> Type identifier of [RangeTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/RangeTemplate). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) <br /> Type identifier of [StatelessTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/StatelessTemplate). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int) <br /> Type identifier of [TemperatureControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int) <br /> Type identifier of [ThumbnailTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ThumbnailTemplate). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int) <br /> Type identifier of [ToggleTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ToggleTemplate). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int) <br /> Type identifier of [ToggleRangeTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ToggleRangeTemplate). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TemperatureControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#TemperatureControlTemplate(kotlin.String,%20android.service.controls.templates.ControlTemplate,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`templateId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `controlTemplate:` ` [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate)`, `currentMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `currentActiveMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `modesFlag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct a new [TemperatureControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#). |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentActiveMode](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#getCurrentActiveMode())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentMode](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#getCurrentMode())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getModes](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#getModes())`()` <br /> |
| --- | --- |
| [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate) | [getTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#getTemplate())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTemplateType](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#getTemplateType())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate) |----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate) | [getErrorTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#getErrorTemplate())`()` <br /> | | [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate) | [getNoTemplateObject](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#getNoTemplateObject())`()` <br /> Get a singleton [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate), which supports no direct user input. Used by [Control.StatelessBuilder](https://developer.android.com/reference/kotlin/android/service/controls/Control.StatelessBuilder.html#) when there is no known state. Can also be used in [Control.StatefulBuilder](https://developer.android.com/reference/kotlin/android/service/controls/Control.StatefulBuilder.html#) for conveying information to a user about the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) but direct user interaction is not desired. Since this template has no corresponding [ControlAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction.html#), any user interaction will launch the [Control.getAppIntent()](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#getAppIntent()). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#getTemplateId())`()` <br /> | ||

## Constants

### FLAG_MODE_COOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_MODE_COOL: Int
```

Flag to indicate that the device supports cool mode. 

 Value: 8

### FLAG_MODE_ECO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_MODE_ECO: Int
```

Flag to indicate that the device supports eco mode. 

 Value: 32

### FLAG_MODE_HEAT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_MODE_HEAT: Int
```

Flag to indicate that the device supports heat mode. 

 Value: 4

### FLAG_MODE_HEAT_COOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_MODE_HEAT_COOL: Int
```

Flag to indicate that the device supports heat-cool mode. 

 Value: 16

### FLAG_MODE_OFF

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_MODE_OFF: Int
```

Flag to indicate that the device supports off mode. 

 Value: 2

### MODE_COOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_COOL: Int
```

Indicates that the current or active mode of the device is set to cool. 
Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_UNKNOWN:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_OFF:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_COOL:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT_COOL:kotlin.Int), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_ECO:kotlin.Int) 

 Value: 3

### MODE_ECO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_ECO: Int
```

Indicates that the current or active mode of the device is set to eco. 
Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_UNKNOWN:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_OFF:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_COOL:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT_COOL:kotlin.Int), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_ECO:kotlin.Int) 

 Value: 5

### MODE_HEAT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_HEAT: Int
```

Indicates that the current or active mode of the device is set to heat. 
Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_UNKNOWN:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_OFF:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_COOL:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT_COOL:kotlin.Int), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_ECO:kotlin.Int) 

 Value: 2

### MODE_HEAT_COOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_HEAT_COOL: Int
```

Indicates that the current or active mode of the device is set to heat-cool. 
Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_UNKNOWN:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_OFF:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_COOL:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT_COOL:kotlin.Int), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_ECO:kotlin.Int) 

 Value: 4

### MODE_OFF

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_OFF: Int
```

Indicates that the current or active mode of the device is off. 
Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_UNKNOWN:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_OFF:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_COOL:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT_COOL:kotlin.Int), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_ECO:kotlin.Int) 

 Value: 1

### MODE_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_UNKNOWN: Int
```

Use when the current or active mode of the device is not known 
Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_UNKNOWN:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_OFF:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_COOL:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT_COOL:kotlin.Int), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_ECO:kotlin.Int) 

 Value: 0

## Public constructors

### TemperatureControlTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TemperatureControlTemplate(
    templateId: String, 
    controlTemplate: ControlTemplate, 
    currentMode: Int, 
    currentActiveMode: Int, 
    modesFlag: Int)
```

Construct a new [TemperatureControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#). The current and active mode have to be among the ones supported by the flags.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `templateId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the identifier for this template object This value cannot be`null`. |
| `controlTemplate` | [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate):a template to use for interaction with the user This value cannot be`null`. |
| `currentMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current mode for the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_UNKNOWN:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_OFF:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_COOL:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT_COOL:kotlin.Int), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_ECO:kotlin.Int) |
| --- | --- |
| `currentActiveMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current active mode for the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_UNKNOWN:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_OFF:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_COOL:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_HEAT_COOL:kotlin.Int), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#MODE_ECO:kotlin.Int) |
| `modesFlag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a flag representing the available modes for the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) Value is either`0`or a combination of [android.service.controls.templates.TemperatureControlTemplate#FLAG_MODE_OFF](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#FLAG_MODE_OFF:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#FLAG_MODE_HEAT](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#FLAG_MODE_HEAT:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#FLAG_MODE_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#FLAG_MODE_COOL:kotlin.Int), [android.service.controls.templates.TemperatureControlTemplate#FLAG_MODE_HEAT_COOL](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#FLAG_MODE_HEAT_COOL:kotlin.Int), and [android.service.controls.templates.TemperatureControlTemplate#FLAG_MODE_ECO](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate#FLAG_MODE_ECO:kotlin.Int) |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the parameters passed do not make a valid template. |

## Public methods

### getCurrentActiveMode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCurrentActiveMode(): Int
```  

### getCurrentMode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCurrentMode(): Int
```  

### getModes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getModes(): Int
```  

### getTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTemplate(): ControlTemplate
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate) | This value cannot be`null`. |

### getTemplateType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTemplateType(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ControlTemplate.TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int) |
