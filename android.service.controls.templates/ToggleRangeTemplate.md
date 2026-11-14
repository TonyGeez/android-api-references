# ToggleRangeTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ToggleRangeTemplate

Kotlin| [Java](../android/service/controls/templates/ToggleRangeTemplate.md) 
| --- | --- |

```
class ToggleRangeTemplate : ControlTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.service.controls.templates.ControlTemplate](../android/service/controls/templates/ControlTemplate.md) ||
| | ↳ | [android.service.controls.templates.ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md) |

A template for a [Control](../android/service/controls/Control.md) supporting toggling and a range.

## Summary

| Inherited constants ||
|---|---|
| From class [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of the template returned by [getErrorTemplate()](../android/service/controls/templates/ControlTemplate.md)). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [ControlTemplate.getNoTemplateObject](../android/service/controls/templates/ControlTemplate.md)). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [RangeTemplate](../android/service/controls/templates/RangeTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [StatelessTemplate](../android/service/controls/templates/StatelessTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [TemperatureControlTemplate](../android/service/controls/templates/TemperatureControlTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [ThumbnailTemplate](../android/service/controls/templates/ThumbnailTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [ToggleTemplate](../android/service/controls/templates/ToggleTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md))`(`templateId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `button:` ` [ControlButton](../android/service/controls/templates/ControlButton.md)`, `range:` ` [RangeTemplate](../android/service/controls/templates/RangeTemplate.md)`)` Constructs a new [ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md). |
| [ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md))`(`templateId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `checked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `actionDescription:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `range:` ` [RangeTemplate](../android/service/controls/templates/RangeTemplate.md)`)` Constructs a new [ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md). |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getActionDescription](../android/service/controls/templates/ToggleRangeTemplate.md))`()` <br /> |
| [RangeTemplate](../android/service/controls/templates/RangeTemplate.md) | [getRange](../android/service/controls/templates/ToggleRangeTemplate.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTemplateType](../android/service/controls/templates/ToggleRangeTemplate.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChecked](../android/service/controls/templates/ToggleRangeTemplate.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) |----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) | [getErrorTemplate](../android/service/controls/templates/ControlTemplate.md))`()` <br /> | | [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) | [getNoTemplateObject](../android/service/controls/templates/ControlTemplate.md))`()` <br /> Get a singleton [ControlTemplate](../android/service/controls/templates/ControlTemplate.md), which supports no direct user input. Used by [Control.StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md) when there is no known state. Can also be used in [Control.StatefulBuilder](../android/service/controls/Control.StatefulBuilder.md) for conveying information to a user about the [Control](../android/service/controls/Control.md) but direct user interaction is not desired. Since this template has no corresponding [ControlAction](../android/service/controls/actions/ControlAction.md), any user interaction will launch the [Control.getAppIntent()](../android/service/controls/Control.md)). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](../android/service/controls/templates/ControlTemplate.md))`()` <br /> | ||

## Public constructors

### ToggleRangeTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ToggleRangeTemplate(
    templateId: String, 
    button: ControlButton, 
    range: RangeTemplate)
```

Constructs a new [ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md).

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `templateId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the identifier for this template. This value cannot be`null`. |
| `button` | [ControlButton](../android/service/controls/templates/ControlButton.md):a [ControlButton](../android/service/controls/templates/ControlButton.md) to use for the toggle interface This value cannot be`null`. |
| `range` | [RangeTemplate](../android/service/controls/templates/RangeTemplate.md):a [RangeTemplate](../android/service/controls/templates/RangeTemplate.md) to use for the range interface This value cannot be`null`. |
| --- | --- |

### ToggleRangeTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ToggleRangeTemplate(
    templateId: String, 
    checked: Boolean, 
    actionDescription: CharSequence, 
    range: RangeTemplate)
```

Constructs a new [ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md).

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `templateId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the identifier for this template. This value cannot be`null`. |
| `checked` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the toggle should be rendered as active. |
| `actionDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):action description for the button. This value cannot be`null`. |
| --- | --- |
| `range` | [RangeTemplate](../android/service/controls/templates/RangeTemplate.md): [RangeTemplate](../android/service/controls/templates/RangeTemplate.md) to use for the range interface This value cannot be`null`. |

**See Also**

- [android.service.controls.templates.ControlButton](../android/service/controls/templates/ControlButton.md)

## Public methods

### getActionDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActionDescription(): CharSequence
```

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | This value cannot be`null`. |

### getRange

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRange(): RangeTemplate
```

| Return ||
|------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [RangeTemplate](../android/service/controls/templates/RangeTemplate.md) | This value cannot be`null`. |

### getTemplateType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTemplateType(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ControlTemplate.TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md) |

### isChecked

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isChecked(): Boolean
```
