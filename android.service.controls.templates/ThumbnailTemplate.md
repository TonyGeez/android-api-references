# ThumbnailTemplate

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThumbnailTemplate

Kotlin| [Java](ThumbnailTemplate.md) 
| --- | --- |

```
class ThumbnailTemplate : ControlTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.service.controls.templates.ControlTemplate](ControlTemplate.md) ||
| | ↳ | [android.service.controls.templates.ThumbnailTemplate](ThumbnailTemplate.md) |

A template for a [Control](../android.service.controls/Control.md) that displays an image.

## Summary

| Inherited constants ||
|---|---|
| From class [ControlTemplate](ControlTemplate.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](ControlTemplate.md) <br /> Type identifier of the template returned by [getErrorTemplate()](ControlTemplate.md)). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NO_TEMPLATE](ControlTemplate.md) <br /> Type identifier of [ControlTemplate.getNoTemplateObject](ControlTemplate.md)). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RANGE](ControlTemplate.md) <br /> Type identifier of [RangeTemplate](RangeTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STATELESS](ControlTemplate.md) <br /> Type identifier of [StatelessTemplate](StatelessTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEMPERATURE](ControlTemplate.md) <br /> Type identifier of [TemperatureControlTemplate](TemperatureControlTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_THUMBNAIL](ControlTemplate.md) <br /> Type identifier of [ThumbnailTemplate](ThumbnailTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE](ControlTemplate.md) <br /> Type identifier of [ToggleTemplate](ToggleTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE_RANGE](ControlTemplate.md) <br /> Type identifier of [ToggleRangeTemplate](ToggleRangeTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ThumbnailTemplate](ThumbnailTemplate.md))`(`templateId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `active:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `thumbnail:` ` [Icon](../android.graphics.drawable/Icon.md)`, `contentDescription:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getContentDescription](ThumbnailTemplate.md))`()` The description of the image returned by [ThumbnailTemplate.getThumbnail()](ThumbnailTemplate.md)) |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTemplateType](ThumbnailTemplate.md))`()` <br /> |
| [Icon](../android.graphics.drawable/Icon.md) | [getThumbnail](ThumbnailTemplate.md))`()` The [Icon](../android.graphics.drawable/Icon.md)(image) displayed by this template. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isActive](ThumbnailTemplate.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [ControlTemplate](ControlTemplate.md) |----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ControlTemplate](ControlTemplate.md) | [getErrorTemplate](ControlTemplate.md))`()` <br /> | | [ControlTemplate](ControlTemplate.md) | [getNoTemplateObject](ControlTemplate.md))`()` <br /> Get a singleton [ControlTemplate](ControlTemplate.md), which supports no direct user input. Used by [Control.StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md) when there is no known state. Can also be used in [Control.StatefulBuilder](../android/service/controls/Control.StatefulBuilder.md) for conveying information to a user about the [Control](../android.service.controls/Control.md) but direct user interaction is not desired. Since this template has no corresponding [ControlAction](../android.service.controls.actions/ControlAction.md), any user interaction will launch the [Control.getAppIntent()](../android.service.controls/Control.md)). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](ControlTemplate.md))`()` <br /> | ||

## Public constructors

### ThumbnailTemplate

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ThumbnailTemplate(
    templateId: String, 
    active: Boolean, 
    thumbnail: Icon, 
    contentDescription: CharSequence)
```

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `templateId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the identifier for this template object This value cannot be`null`. |
| `active` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the image corresponds to an active (live) stream. |
| `thumbnail` | [Icon](../android.graphics.drawable/Icon.md):an image to display on the [Control](../android.service.controls/Control.md) This value cannot be`null`. |
| --- | --- |
| `contentDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):a description of the image for accessibility. This value cannot be`null`. |

## Public methods

### getContentDescription

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContentDescription(): CharSequence
```

The description of the image returned by [ThumbnailTemplate.getThumbnail()](ThumbnailTemplate.md))

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | This value cannot be`null`. |

### getTemplateType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTemplateType(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ControlTemplate.TYPE_THUMBNAIL](ControlTemplate.md) |

### getThumbnail

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getThumbnail(): Icon
```

The [Icon](../android.graphics.drawable/Icon.md)(image) displayed by this template.

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------|
| [Icon](../android.graphics.drawable/Icon.md) | This value cannot be`null`. |

### isActive

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isActive(): Boolean
```
