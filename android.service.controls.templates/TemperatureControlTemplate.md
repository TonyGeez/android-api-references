# TemperatureControlTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TemperatureControlTemplate

Kotlin| [Java](TemperatureControlTemplate.md) 
| --- | --- |

```
class TemperatureControlTemplate : ControlTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.service.controls.templates.ControlTemplate](ControlTemplate.md) ||
| | ↳ | [android.service.controls.templates.TemperatureControlTemplate](TemperatureControlTemplate.md) |

A template for a temperature related [Control](../android.service.controls/Control.md) that supports multiple modes. Both the current mode and the active mode for the control can be specified. The combination of the [Control.getDeviceType](../android.service.controls/Control.md))and the current and active mode will determine colors and transitions for the UI element.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_MODE_COOL](TemperatureControlTemplate.md) Flag to indicate that the device supports cool mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_MODE_ECO](TemperatureControlTemplate.md) Flag to indicate that the device supports eco mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_MODE_HEAT](TemperatureControlTemplate.md) Flag to indicate that the device supports heat mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_MODE_HEAT_COOL](TemperatureControlTemplate.md) Flag to indicate that the device supports heat-cool mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_MODE_OFF](TemperatureControlTemplate.md) Flag to indicate that the device supports off mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_COOL](TemperatureControlTemplate.md) Indicates that the current or active mode of the device is set to cool. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_ECO](TemperatureControlTemplate.md) Indicates that the current or active mode of the device is set to eco. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_HEAT](TemperatureControlTemplate.md) Indicates that the current or active mode of the device is set to heat. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_HEAT_COOL](TemperatureControlTemplate.md) Indicates that the current or active mode of the device is set to heat-cool. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_OFF](TemperatureControlTemplate.md) Indicates that the current or active mode of the device is off. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_UNKNOWN](TemperatureControlTemplate.md) Use when the current or active mode of the device is not known Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](TemperatureControlTemplate.md), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](TemperatureControlTemplate.md) |

| Inherited constants ||
|---|---|
| From class [ControlTemplate](ControlTemplate.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](ControlTemplate.md) <br /> Type identifier of the template returned by [getErrorTemplate()](ControlTemplate.md)). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NO_TEMPLATE](ControlTemplate.md) <br /> Type identifier of [ControlTemplate.getNoTemplateObject](ControlTemplate.md)). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RANGE](ControlTemplate.md) <br /> Type identifier of [RangeTemplate](RangeTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STATELESS](ControlTemplate.md) <br /> Type identifier of [StatelessTemplate](StatelessTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEMPERATURE](ControlTemplate.md) <br /> Type identifier of [TemperatureControlTemplate](TemperatureControlTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_THUMBNAIL](ControlTemplate.md) <br /> Type identifier of [ThumbnailTemplate](ThumbnailTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE](ControlTemplate.md) <br /> Type identifier of [ToggleTemplate](ToggleTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE_RANGE](ControlTemplate.md) <br /> Type identifier of [ToggleRangeTemplate](ToggleRangeTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TemperatureControlTemplate](TemperatureControlTemplate.md))`(`templateId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `controlTemplate:` ` [ControlTemplate](ControlTemplate.md)`, `currentMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `currentActiveMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `modesFlag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct a new [TemperatureControlTemplate](TemperatureControlTemplate.md). |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentActiveMode](TemperatureControlTemplate.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentMode](TemperatureControlTemplate.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getModes](TemperatureControlTemplate.md))`()` <br /> |
| --- | --- |
| [ControlTemplate](ControlTemplate.md) | [getTemplate](TemperatureControlTemplate.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTemplateType](TemperatureControlTemplate.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [ControlTemplate](ControlTemplate.md) |----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ControlTemplate](ControlTemplate.md) | [getErrorTemplate](ControlTemplate.md))`()` <br /> | | [ControlTemplate](ControlTemplate.md) | [getNoTemplateObject](ControlTemplate.md))`()` <br /> Get a singleton [ControlTemplate](ControlTemplate.md), which supports no direct user input. Used by [Control.StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md) when there is no known state. Can also be used in [Control.StatefulBuilder](../android/service/controls/Control.StatefulBuilder.md) for conveying information to a user about the [Control](../android.service.controls/Control.md) but direct user interaction is not desired. Since this template has no corresponding [ControlAction](../android.service.controls.actions/ControlAction.md), any user interaction will launch the [Control.getAppIntent()](../android.service.controls/Control.md)). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](ControlTemplate.md))`()` <br /> | ||

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
Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](TemperatureControlTemplate.md), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](TemperatureControlTemplate.md) 

 Value: 3

### MODE_ECO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_ECO: Int
```

Indicates that the current or active mode of the device is set to eco. 
Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](TemperatureControlTemplate.md), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](TemperatureControlTemplate.md) 

 Value: 5

### MODE_HEAT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_HEAT: Int
```

Indicates that the current or active mode of the device is set to heat. 
Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](TemperatureControlTemplate.md), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](TemperatureControlTemplate.md) 

 Value: 2

### MODE_HEAT_COOL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_HEAT_COOL: Int
```

Indicates that the current or active mode of the device is set to heat-cool. 
Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](TemperatureControlTemplate.md), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](TemperatureControlTemplate.md) 

 Value: 4

### MODE_OFF

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_OFF: Int
```

Indicates that the current or active mode of the device is off. 
Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](TemperatureControlTemplate.md), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](TemperatureControlTemplate.md) 

 Value: 1

### MODE_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_UNKNOWN: Int
```

Use when the current or active mode of the device is not known 
Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](TemperatureControlTemplate.md), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](TemperatureControlTemplate.md) 

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

Construct a new [TemperatureControlTemplate](TemperatureControlTemplate.md). The current and active mode have to be among the ones supported by the flags.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `templateId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the identifier for this template object This value cannot be`null`. |
| `controlTemplate` | [ControlTemplate](ControlTemplate.md):a template to use for interaction with the user This value cannot be`null`. |
| `currentMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current mode for the [Control](../android.service.controls/Control.md) Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](TemperatureControlTemplate.md), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](TemperatureControlTemplate.md) |
| --- | --- |
| `currentActiveMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current active mode for the [Control](../android.service.controls/Control.md) Value is [android.service.controls.templates.TemperatureControlTemplate#MODE_UNKNOWN](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_OFF](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_COOL](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#MODE_HEAT_COOL](TemperatureControlTemplate.md), or [android.service.controls.templates.TemperatureControlTemplate#MODE_ECO](TemperatureControlTemplate.md) |
| `modesFlag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a flag representing the available modes for the [Control](../android.service.controls/Control.md) Value is either`0`or a combination of [android.service.controls.templates.TemperatureControlTemplate#FLAG_MODE_OFF](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#FLAG_MODE_HEAT](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#FLAG_MODE_COOL](TemperatureControlTemplate.md), [android.service.controls.templates.TemperatureControlTemplate#FLAG_MODE_HEAT_COOL](TemperatureControlTemplate.md), and [android.service.controls.templates.TemperatureControlTemplate#FLAG_MODE_ECO](TemperatureControlTemplate.md) |

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
| [ControlTemplate](ControlTemplate.md) | This value cannot be`null`. |

### getTemplateType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTemplateType(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ControlTemplate.TYPE_TEMPERATURE](ControlTemplate.md) |
