# ToggleTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ToggleTemplate

Kotlin| [Java](ToggleTemplate.md) 
| --- | --- |

```
class ToggleTemplate : ControlTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.service.controls.templates.ControlTemplate](ControlTemplate.md) ||
| | ↳ | [android.service.controls.templates.ToggleTemplate](ToggleTemplate.md) |

A template for a [Control](../android.service.controls/Control.md) with a single button that can be toggled between two states. The states for the toggle correspond to the states in [ControlButton.isChecked()](ControlButton.md)). An action on this template will originate a [BooleanAction](../android.service.controls.actions/BooleanAction.md) to change that state.

## Summary

| Inherited constants ||
|---|---|
| From class [ControlTemplate](ControlTemplate.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](ControlTemplate.md) <br /> Type identifier of the template returned by [getErrorTemplate()](ControlTemplate.md)). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NO_TEMPLATE](ControlTemplate.md) <br /> Type identifier of [ControlTemplate.getNoTemplateObject](ControlTemplate.md)). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RANGE](ControlTemplate.md) <br /> Type identifier of [RangeTemplate](RangeTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STATELESS](ControlTemplate.md) <br /> Type identifier of [StatelessTemplate](StatelessTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEMPERATURE](ControlTemplate.md) <br /> Type identifier of [TemperatureControlTemplate](TemperatureControlTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_THUMBNAIL](ControlTemplate.md) <br /> Type identifier of [ThumbnailTemplate](ThumbnailTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE](ControlTemplate.md) <br /> Type identifier of [ToggleTemplate](ToggleTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE_RANGE](ControlTemplate.md) <br /> Type identifier of [ToggleRangeTemplate](ToggleRangeTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ToggleTemplate](ToggleTemplate.md))`(`templateId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `button:` ` [ControlButton](ControlButton.md)`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getContentDescription](ToggleTemplate.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTemplateType](ToggleTemplate.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChecked](ToggleTemplate.md))`()` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [ControlTemplate](ControlTemplate.md) |----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ControlTemplate](ControlTemplate.md) | [getErrorTemplate](ControlTemplate.md))`()` <br /> | | [ControlTemplate](ControlTemplate.md) | [getNoTemplateObject](ControlTemplate.md))`()` <br /> Get a singleton [ControlTemplate](ControlTemplate.md), which supports no direct user input. Used by [Control.StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md) when there is no known state. Can also be used in [Control.StatefulBuilder](../android/service/controls/Control.StatefulBuilder.md) for conveying information to a user about the [Control](../android.service.controls/Control.md) but direct user interaction is not desired. Since this template has no corresponding [ControlAction](../android.service.controls.actions/ControlAction.md), any user interaction will launch the [Control.getAppIntent()](../android.service.controls/Control.md)). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](ControlTemplate.md))`()` <br /> | ||

## Public constructors

### ToggleTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ToggleTemplate(
    templateId: String, 
    button: ControlButton)
```

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `templateId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the identifier for this template object This value cannot be`null`. |
| `button` | [ControlButton](ControlButton.md):a [ControlButton](ControlButton.md) that can show the current state and toggle it This value cannot be`null`. |

## Public methods

### getContentDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContentDescription(): CharSequence
```

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | This value cannot be`null`. |

### getTemplateType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTemplateType(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ControlTemplate.TYPE_TOGGLE](ControlTemplate.md) |

### isChecked

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isChecked(): Boolean
```
