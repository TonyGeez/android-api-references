# ToggleRangeTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ToggleRangeTemplate

Kotlin| [Java](ToggleRangeTemplate.md) 
| --- | --- |

```
class ToggleRangeTemplate : ControlTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.service.controls.templates.ControlTemplate](ControlTemplate.md) ||
| | ↳ | [android.service.controls.templates.ToggleRangeTemplate](ToggleRangeTemplate.md) |

A template for a [Control](../android.service.controls/Control.md) supporting toggling and a range.

## Summary

| Inherited constants ||
|---|---|
| From class [ControlTemplate](ControlTemplate.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](ControlTemplate.md) <br /> Type identifier of the template returned by [getErrorTemplate()](ControlTemplate.md)). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NO_TEMPLATE](ControlTemplate.md) <br /> Type identifier of [ControlTemplate.getNoTemplateObject](ControlTemplate.md)). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RANGE](ControlTemplate.md) <br /> Type identifier of [RangeTemplate](RangeTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STATELESS](ControlTemplate.md) <br /> Type identifier of [StatelessTemplate](StatelessTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEMPERATURE](ControlTemplate.md) <br /> Type identifier of [TemperatureControlTemplate](TemperatureControlTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_THUMBNAIL](ControlTemplate.md) <br /> Type identifier of [ThumbnailTemplate](ThumbnailTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE](ControlTemplate.md) <br /> Type identifier of [ToggleTemplate](ToggleTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE_RANGE](ControlTemplate.md) <br /> Type identifier of [ToggleRangeTemplate](ToggleRangeTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ToggleRangeTemplate](ToggleRangeTemplate.md))`(`templateId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `button:` ` [ControlButton](ControlButton.md)`, `range:` ` [RangeTemplate](RangeTemplate.md)`)` Constructs a new [ToggleRangeTemplate](ToggleRangeTemplate.md). |
| [ToggleRangeTemplate](ToggleRangeTemplate.md))`(`templateId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `checked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `actionDescription:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `range:` ` [RangeTemplate](RangeTemplate.md)`)` Constructs a new [ToggleRangeTemplate](ToggleRangeTemplate.md). |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getActionDescription](ToggleRangeTemplate.md))`()` <br /> |
| [RangeTemplate](RangeTemplate.md) | [getRange](ToggleRangeTemplate.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTemplateType](ToggleRangeTemplate.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChecked](ToggleRangeTemplate.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [ControlTemplate](ControlTemplate.md) |----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ControlTemplate](ControlTemplate.md) | [getErrorTemplate](ControlTemplate.md))`()` <br /> | | [ControlTemplate](ControlTemplate.md) | [getNoTemplateObject](ControlTemplate.md))`()` <br /> Get a singleton [ControlTemplate](ControlTemplate.md), which supports no direct user input. Used by [Control.StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md) when there is no known state. Can also be used in [Control.StatefulBuilder](../android/service/controls/Control.StatefulBuilder.md) for conveying information to a user about the [Control](../android.service.controls/Control.md) but direct user interaction is not desired. Since this template has no corresponding [ControlAction](../android.service.controls.actions/ControlAction.md), any user interaction will launch the [Control.getAppIntent()](../android.service.controls/Control.md)). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](ControlTemplate.md))`()` <br /> | ||

## Public constructors

### ToggleRangeTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ToggleRangeTemplate(
    templateId: String, 
    button: ControlButton, 
    range: RangeTemplate)
```

Constructs a new [ToggleRangeTemplate](ToggleRangeTemplate.md).

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `templateId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the identifier for this template. This value cannot be`null`. |
| `button` | [ControlButton](ControlButton.md):a [ControlButton](ControlButton.md) to use for the toggle interface This value cannot be`null`. |
| `range` | [RangeTemplate](RangeTemplate.md):a [RangeTemplate](RangeTemplate.md) to use for the range interface This value cannot be`null`. |
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

Constructs a new [ToggleRangeTemplate](ToggleRangeTemplate.md).

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `templateId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the identifier for this template. This value cannot be`null`. |
| `checked` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the toggle should be rendered as active. |
| `actionDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):action description for the button. This value cannot be`null`. |
| --- | --- |
| `range` | [RangeTemplate](RangeTemplate.md): [RangeTemplate](RangeTemplate.md) to use for the range interface This value cannot be`null`. |

**See Also**

- [android.service.controls.templates.ControlButton](ControlButton.md)

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
| [RangeTemplate](RangeTemplate.md) | This value cannot be`null`. |

### getTemplateType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTemplateType(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ControlTemplate.TYPE_TOGGLE_RANGE](ControlTemplate.md) |

### isChecked

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isChecked(): Boolean
```
