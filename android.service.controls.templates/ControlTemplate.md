# ControlTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ControlTemplate

Kotlin| [Java](ControlTemplate.md) 
| --- | --- |

```
abstract class ControlTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.controls.templates.ControlTemplate](ControlTemplate.md) |

| Known Direct Subclasses [RangeTemplate](RangeTemplate.md), [StatelessTemplate](StatelessTemplate.md), [TemperatureControlTemplate](TemperatureControlTemplate.md), [ThumbnailTemplate](ThumbnailTemplate.md), [ToggleRangeTemplate](ToggleRangeTemplate.md), [ToggleTemplate](ToggleTemplate.md) |--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RangeTemplate](RangeTemplate.md) | A template for a [Control](../android.service.controls/Control.md) with inputs in a "continuous" range of values. | | [StatelessTemplate](StatelessTemplate.md) | A template for a [Control](../android.service.controls/Control.md) which has no state. | | [TemperatureControlTemplate](TemperatureControlTemplate.md) | A template for a temperature related [Control](../android.service.controls/Control.md) that supports multiple modes. | | [ThumbnailTemplate](ThumbnailTemplate.md) | A template for a [Control](../android.service.controls/Control.md) that displays an image. | | [ToggleRangeTemplate](ToggleRangeTemplate.md) | A template for a [Control](../android.service.controls/Control.md) supporting toggling and a range. | | [ToggleTemplate](ToggleTemplate.md) | A template for a [Control](../android.service.controls/Control.md) with a single button that can be toggled between two states. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An abstract input template for a [Control](../android.service.controls/Control.md). Specifies what layout is presented to the user for a given [Control](../android.service.controls/Control.md).

Some instances of [Control](../android.service.controls/Control.md) can originate actions (via user interaction) to modify its associated state. The actions available to a given [Control](../android.service.controls/Control.md) are determined by its [ControlTemplate](ControlTemplate.md).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](ControlTemplate.md) Type identifier of the template returned by [getErrorTemplate()](ControlTemplate.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NO_TEMPLATE](ControlTemplate.md) Type identifier of [ControlTemplate.getNoTemplateObject](ControlTemplate.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RANGE](ControlTemplate.md) Type identifier of [RangeTemplate](RangeTemplate.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STATELESS](ControlTemplate.md) Type identifier of [StatelessTemplate](StatelessTemplate.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEMPERATURE](ControlTemplate.md) Type identifier of [TemperatureControlTemplate](TemperatureControlTemplate.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_THUMBNAIL](ControlTemplate.md) Type identifier of [ThumbnailTemplate](ThumbnailTemplate.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE](ControlTemplate.md) Type identifier of [ToggleTemplate](ToggleTemplate.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE_RANGE](ControlTemplate.md) Type identifier of [ToggleRangeTemplate](ToggleRangeTemplate.md). |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ControlTemplate](ControlTemplate.md) | [getErrorTemplate](ControlTemplate.md))`()` <br /> |
| openstatic [ControlTemplate](ControlTemplate.md) | [getNoTemplateObject](ControlTemplate.md))`()` Get a singleton [ControlTemplate](ControlTemplate.md), which supports no direct user input. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](ControlTemplate.md))`()` <br /> |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTemplateType](ControlTemplate.md))`()` The template type associated with this class. |

## Constants

### TYPE_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ERROR: Int
```

Type identifier of the template returned by [getErrorTemplate()](ControlTemplate.md)). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) 

 Value: -1

### TYPE_NO_TEMPLATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NO_TEMPLATE: Int
```

Type identifier of [ControlTemplate.getNoTemplateObject](ControlTemplate.md)). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) 

 Value: 0

### TYPE_RANGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_RANGE: Int
```

Type identifier of [RangeTemplate](RangeTemplate.md). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) 

 Value: 2

### TYPE_STATELESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_STATELESS: Int
```

Type identifier of [StatelessTemplate](StatelessTemplate.md). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) 

 Value: 8

### TYPE_TEMPERATURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEMPERATURE: Int
```

Type identifier of [TemperatureControlTemplate](TemperatureControlTemplate.md). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) 

 Value: 7

### TYPE_THUMBNAIL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_THUMBNAIL: Int
```

Type identifier of [ThumbnailTemplate](ThumbnailTemplate.md). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) 

 Value: 3

### TYPE_TOGGLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TOGGLE: Int
```

Type identifier of [ToggleTemplate](ToggleTemplate.md). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) 

 Value: 1

### TYPE_TOGGLE_RANGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TOGGLE_RANGE: Int
```

Type identifier of [ToggleRangeTemplate](ToggleRangeTemplate.md). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) 

 Value: 6

## Public methods

### getErrorTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getErrorTemplate(): ControlTemplate
```

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ControlTemplate](ControlTemplate.md) | a singleton [ControlTemplate](ControlTemplate.md) used for indicating an error in unparceling. This value cannot be`null`. |

### getNoTemplateObject

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNoTemplateObject(): ControlTemplate
```

Get a singleton [ControlTemplate](ControlTemplate.md), which supports no direct user input. Used by [Control.StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md) when there is no known state. Can also be used in [Control.StatefulBuilder](../android/service/controls/Control.StatefulBuilder.md) for conveying information to a user about the [Control](../android.service.controls/Control.md) but direct user interaction is not desired. Since this template has no corresponding [ControlAction](../android.service.controls.actions/ControlAction.md), any user interaction will launch the [Control.getAppIntent()](../android.service.controls/Control.md)).

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ControlTemplate](ControlTemplate.md) | a singleton [ControlTemplate](ControlTemplate.md) to indicate no specific template is used by this [Control](../android.service.controls/Control.md) This value cannot be`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](ControlTemplate.md), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](ControlTemplate.md), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](ControlTemplate.md) |
