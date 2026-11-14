# ControlTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ControlTemplate

Kotlin| [Java](../android/service/controls/templates/ControlTemplate.md) 
| --- | --- |

```
abstract class ControlTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.controls.templates.ControlTemplate](../android/service/controls/templates/ControlTemplate.md) |

| Known Direct Subclasses [RangeTemplate](../android/service/controls/templates/RangeTemplate.md), [StatelessTemplate](../android/service/controls/templates/StatelessTemplate.md), [TemperatureControlTemplate](../android/service/controls/templates/TemperatureControlTemplate.md), [ThumbnailTemplate](../android/service/controls/templates/ThumbnailTemplate.md), [ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md), [ToggleTemplate](../android/service/controls/templates/ToggleTemplate.md) |--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RangeTemplate](../android/service/controls/templates/RangeTemplate.md) | A template for a [Control](../android/service/controls/Control.md) with inputs in a "continuous" range of values. | | [StatelessTemplate](../android/service/controls/templates/StatelessTemplate.md) | A template for a [Control](../android/service/controls/Control.md) which has no state. | | [TemperatureControlTemplate](../android/service/controls/templates/TemperatureControlTemplate.md) | A template for a temperature related [Control](../android/service/controls/Control.md) that supports multiple modes. | | [ThumbnailTemplate](../android/service/controls/templates/ThumbnailTemplate.md) | A template for a [Control](../android/service/controls/Control.md) that displays an image. | | [ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md) | A template for a [Control](../android/service/controls/Control.md) supporting toggling and a range. | | [ToggleTemplate](../android/service/controls/templates/ToggleTemplate.md) | A template for a [Control](../android/service/controls/Control.md) with a single button that can be toggled between two states. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An abstract input template for a [Control](../android/service/controls/Control.md). Specifies what layout is presented to the user for a given [Control](../android/service/controls/Control.md).

Some instances of [Control](../android/service/controls/Control.md) can originate actions (via user interaction) to modify its associated state. The actions available to a given [Control](../android/service/controls/Control.md) are determined by its [ControlTemplate](../android/service/controls/templates/ControlTemplate.md).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md) Type identifier of the template returned by [getErrorTemplate()](../android/service/controls/templates/ControlTemplate.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md) Type identifier of [ControlTemplate.getNoTemplateObject](../android/service/controls/templates/ControlTemplate.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md) Type identifier of [RangeTemplate](../android/service/controls/templates/RangeTemplate.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) Type identifier of [StatelessTemplate](../android/service/controls/templates/StatelessTemplate.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md) Type identifier of [TemperatureControlTemplate](../android/service/controls/templates/TemperatureControlTemplate.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md) Type identifier of [ThumbnailTemplate](../android/service/controls/templates/ThumbnailTemplate.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md) Type identifier of [ToggleTemplate](../android/service/controls/templates/ToggleTemplate.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md) Type identifier of [ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md). |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) | [getErrorTemplate](../android/service/controls/templates/ControlTemplate.md))`()` <br /> |
| openstatic [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) | [getNoTemplateObject](../android/service/controls/templates/ControlTemplate.md))`()` Get a singleton [ControlTemplate](../android/service/controls/templates/ControlTemplate.md), which supports no direct user input. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](../android/service/controls/templates/ControlTemplate.md))`()` <br /> |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTemplateType](../android/service/controls/templates/ControlTemplate.md))`()` The template type associated with this class. |

## Constants

### TYPE_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ERROR: Int
```

Type identifier of the template returned by [getErrorTemplate()](../android/service/controls/templates/ControlTemplate.md)). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) 

 Value: -1

### TYPE_NO_TEMPLATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NO_TEMPLATE: Int
```

Type identifier of [ControlTemplate.getNoTemplateObject](../android/service/controls/templates/ControlTemplate.md)). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) 

 Value: 0

### TYPE_RANGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_RANGE: Int
```

Type identifier of [RangeTemplate](../android/service/controls/templates/RangeTemplate.md). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) 

 Value: 2

### TYPE_STATELESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_STATELESS: Int
```

Type identifier of [StatelessTemplate](../android/service/controls/templates/StatelessTemplate.md). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) 

 Value: 8

### TYPE_TEMPERATURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEMPERATURE: Int
```

Type identifier of [TemperatureControlTemplate](../android/service/controls/templates/TemperatureControlTemplate.md). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) 

 Value: 7

### TYPE_THUMBNAIL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_THUMBNAIL: Int
```

Type identifier of [ThumbnailTemplate](../android/service/controls/templates/ThumbnailTemplate.md). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) 

 Value: 3

### TYPE_TOGGLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TOGGLE: Int
```

Type identifier of [ToggleTemplate](../android/service/controls/templates/ToggleTemplate.md). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) 

 Value: 1

### TYPE_TOGGLE_RANGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TOGGLE_RANGE: Int
```

Type identifier of [ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) 

 Value: 6

## Public methods

### getErrorTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getErrorTemplate(): ControlTemplate
```

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) | a singleton [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) used for indicating an error in unparceling. This value cannot be`null`. |

### getNoTemplateObject

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNoTemplateObject(): ControlTemplate
```

Get a singleton [ControlTemplate](../android/service/controls/templates/ControlTemplate.md), which supports no direct user input. Used by [Control.StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md) when there is no known state. Can also be used in [Control.StatefulBuilder](../android/service/controls/Control.StatefulBuilder.md) for conveying information to a user about the [Control](../android/service/controls/Control.md) but direct user interaction is not desired. Since this template has no corresponding [ControlAction](../android/service/controls/actions/ControlAction.md), any user interaction will launch the [Control.getAppIntent()](../android/service/controls/Control.md)).

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) | a singleton [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) to indicate no specific template is used by this [Control](../android/service/controls/Control.md) This value cannot be`null`. |

### getTemplateId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTemplateId(): String
```

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the identifier for this object. This value cannot be`null`. |

### getTemplateType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTemplateType(): Int
```

The template type associated with this class.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](../android/service/controls/templates/ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](../android/service/controls/templates/ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](../android/service/controls/templates/ControlTemplate.md) |
