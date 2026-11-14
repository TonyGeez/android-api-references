# ThumbnailTemplate

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThumbnailTemplate

Kotlin| [Java](../android/service/controls/templates/ThumbnailTemplate.md) 
| --- | --- |

```
class ThumbnailTemplate : ControlTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.service.controls.templates.ControlTemplate](../android/service/controls/templates/ControlTemplate.md) ||
| | ↳ | [android.service.controls.templates.ThumbnailTemplate](../android/service/controls/templates/ThumbnailTemplate.md) |

A template for a [Control](../android/service/controls/Control.md) that displays an image.

## Summary

| Inherited constants ||
|---|---|
| From class [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of the template returned by [getErrorTemplate()](../android/service/controls/templates/ControlTemplate.md)). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [ControlTemplate.getNoTemplateObject](../android/service/controls/templates/ControlTemplate.md)). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [RangeTemplate](../android/service/controls/templates/RangeTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [StatelessTemplate](../android/service/controls/templates/StatelessTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [TemperatureControlTemplate](../android/service/controls/templates/TemperatureControlTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [ThumbnailTemplate](../android/service/controls/templates/ThumbnailTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [ToggleTemplate](../android/service/controls/templates/ToggleTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md) <br /> Type identifier of [ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md). Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ThumbnailTemplate](../android/service/controls/templates/ThumbnailTemplate.md))`(`templateId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `active:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `thumbnail:` ` [Icon](../android/graphics/drawable/Icon.md)`, `contentDescription:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getContentDescription](../android/service/controls/templates/ThumbnailTemplate.md))`()` The description of the image returned by [ThumbnailTemplate.getThumbnail()](../android/service/controls/templates/ThumbnailTemplate.md)) |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTemplateType](../android/service/controls/templates/ThumbnailTemplate.md))`()` <br /> |
| [Icon](../android/graphics/drawable/Icon.md) | [getThumbnail](../android/service/controls/templates/ThumbnailTemplate.md))`()` The [Icon](../android/graphics/drawable/Icon.md)(image) displayed by this template. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isActive](../android/service/controls/templates/ThumbnailTemplate.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) |----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) | [getErrorTemplate](../android/service/controls/templates/ControlTemplate.md))`()` <br /> | | [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) | [getNoTemplateObject](../android/service/controls/templates/ControlTemplate.md))`()` <br /> Get a singleton [ControlTemplate](../android/service/controls/templates/ControlTemplate.md), which supports no direct user input. Used by [Control.StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md) when there is no known state. Can also be used in [Control.StatefulBuilder](../android/service/controls/Control.StatefulBuilder.md) for conveying information to a user about the [Control](../android/service/controls/Control.md) but direct user interaction is not desired. Since this template has no corresponding [ControlAction](../android/service/controls/actions/ControlAction.md), any user interaction will launch the [Control.getAppIntent()](../android/service/controls/Control.md)). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](../android/service/controls/templates/ControlTemplate.md))`()` <br /> | ||

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
| `thumbnail` | [Icon](../android/graphics/drawable/Icon.md):an image to display on the [Control](../android/service/controls/Control.md) This value cannot be`null`. |
| --- | --- |
| `contentDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):a description of the image for accessibility. This value cannot be`null`. |

## Public methods

### getContentDescription

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContentDescription(): CharSequence
```

The description of the image returned by [ThumbnailTemplate.getThumbnail()](../android/service/controls/templates/ThumbnailTemplate.md))

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ControlTemplate.TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md) |

### getThumbnail

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getThumbnail(): Icon
```

The [Icon](../android/graphics/drawable/Icon.md)(image) displayed by this template.

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------|
| [Icon](../android/graphics/drawable/Icon.md) | This value cannot be`null`. |

### isActive

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isActive(): Boolean
```
