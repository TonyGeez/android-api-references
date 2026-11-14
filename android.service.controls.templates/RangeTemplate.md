# RangeTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RangeTemplate

Kotlin| [Java](../android/service/controls/templates/RangeTemplate.md) 
| --- | --- |

```
class RangeTemplate : ControlTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.service.controls.templates.ControlTemplate](../android/service/controls/templates/ControlTemplate.md) ||
| | ↳ | [android.service.controls.templates.RangeTemplate](../android/service/controls/templates/RangeTemplate.md) |

A template for a [Control](../android/service/controls/Control.md) with inputs in a "continuous" range of values.

## Summary

| Inherited constants ||
|---|---|
| From class [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of the template returned by [getErrorTemplate()](../android/service/controls/templates/ControlTemplate.md)). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [ControlTemplate.getNoTemplateObject](../android/service/controls/templates/ControlTemplate.md)). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [RangeTemplate](../android/service/controls/templates/RangeTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [StatelessTemplate](../android/service/controls/templates/StatelessTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [TemperatureControlTemplate](../android/service/controls/templates/TemperatureControlTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [ThumbnailTemplate](../android/service/controls/templates/ThumbnailTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [ToggleTemplate](../android/service/controls/templates/ToggleTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RangeTemplate](../android/service/controls/templates/RangeTemplate.md))`(`templateId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `minValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `maxValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `currentValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `stepValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `formatString:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Construct a new [RangeTemplate](../android/service/controls/templates/RangeTemplate.md). |

| Public methods ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCurrentValue](../android/service/controls/templates/RangeTemplate.md))`()` The current value for this range. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getFormatString](../android/service/controls/templates/RangeTemplate.md))`()` Formatter for generating a user visible [String](../java/lang/String.md) representing the value returned by [RangeTemplate.getCurrentValue](../android/service/controls/templates/RangeTemplate.md)). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMaxValue](../android/service/controls/templates/RangeTemplate.md))`()` The maximum value for this range. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMinValue](../android/service/controls/templates/RangeTemplate.md))`()` The minimum value for this range. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getStepValue](../android/service/controls/templates/RangeTemplate.md))`()` The value of the smallest increment or decrement that can be performed on this range. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTemplateType](../android/service/controls/templates/RangeTemplate.md))`()` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) |----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) | [getErrorTemplate](../android/service/controls/templates/ControlTemplate.md))`()` <br /> | | [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) | [getNoTemplateObject](../android/service/controls/templates/ControlTemplate.md))`()` <br /> Get a singleton [ControlTemplate](../android/service/controls/templates/ControlTemplate.md), which supports no direct user input. Used by [Control.StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md) when there is no known state. Can also be used in [Control.StatefulBuilder](../android/service/controls/Control.StatefulBuilder.md) for conveying information to a user about the [Control](../android/service/controls/Control.md) but direct user interaction is not desired. Since this template has no corresponding [ControlAction](../android/service/controls/actions/ControlAction.md), any user interaction will launch the [Control.getAppIntent()](../android/service/controls/Control.md)). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](../android/service/controls/templates/ControlTemplate.md))`()` <br /> | ||

## Public constructors

### RangeTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RangeTemplate(
    templateId: String, 
    minValue: Float, 
    maxValue: Float, 
    currentValue: Float, 
    stepValue: Float, 
    formatString: CharSequence?)
```

Construct a new [RangeTemplate](../android/service/controls/templates/RangeTemplate.md). The range must be valid, meaning:

- `minValue`\<`maxValue`
- `minValue`\<`currentValue`
- `currentValue`\<`maxValue`
- 0 \<`stepValue`

<br />

The current value of the Control will be formatted accordingly.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `templateId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the identifier for this template object This value cannot be`null`. |
| `minValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum value for the input |
| `maxValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):maximum value for the input |
| --- | --- |
| `currentValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the current value of the [Control](../android/service/controls/Control.md) containing this object. |
| `stepValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum value of increments/decrements when interacting with this control. |
| `formatString` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:a formatting string as per java.lang.String#format used to display the`currentValue`. If`null`is passed, the "%.1f" is used. |
| --- | --- |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the parameters passed do not make a valid range. |

## Public methods

### getCurrentValue

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCurrentValue(): Float
```

The current value for this range. 

### getFormatString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFormatString(): CharSequence
```

Formatter for generating a user visible [String](../java/lang/String.md) representing the value returned by [RangeTemplate.getCurrentValue](../android/service/controls/templates/RangeTemplate.md)).

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | a formatting string as specified in java.lang.String#format This value cannot be`null`. |

### getMaxValue

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxValue(): Float
```

The maximum value for this range. 

### getMinValue

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMinValue(): Float
```

The minimum value for this range. 

### getStepValue

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStepValue(): Float
```

The value of the smallest increment or decrement that can be performed on this range. 

### getTemplateType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTemplateType(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ControlTemplate.TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md) |
