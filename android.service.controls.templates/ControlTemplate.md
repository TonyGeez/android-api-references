# ControlTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ControlTemplate

Kotlin| [Java](https://developer.android.com/reference/android/service/controls/templates/ControlTemplate "View this page in Java") 
| --- | --- |

```
abstract class ControlTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.controls.templates.ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#) |

| Known Direct Subclasses [RangeTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/RangeTemplate), [StatelessTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/StatelessTemplate), [TemperatureControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate), [ThumbnailTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ThumbnailTemplate), [ToggleRangeTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ToggleRangeTemplate), [ToggleTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ToggleTemplate) |--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RangeTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/RangeTemplate) | A template for a [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) with inputs in a "continuous" range of values. | | [StatelessTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/StatelessTemplate) | A template for a [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) which has no state. | | [TemperatureControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate) | A template for a temperature related [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) that supports multiple modes. | | [ThumbnailTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ThumbnailTemplate) | A template for a [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) that displays an image. | | [ToggleRangeTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ToggleRangeTemplate) | A template for a [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) supporting toggling and a range. | | [ToggleTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ToggleTemplate) | A template for a [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) with a single button that can be toggled between two states. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An abstract input template for a [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#). Specifies what layout is presented to the user for a given [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#).

Some instances of [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) can originate actions (via user interaction) to modify its associated state. The actions available to a given [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) are determined by its [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int) Type identifier of the template returned by [getErrorTemplate()](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#getErrorTemplate()). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int) Type identifier of [ControlTemplate.getNoTemplateObject](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#getNoTemplateObject()). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int) Type identifier of [RangeTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/RangeTemplate). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) Type identifier of [StatelessTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/StatelessTemplate). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int) Type identifier of [TemperatureControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int) Type identifier of [ThumbnailTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ThumbnailTemplate). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int) Type identifier of [ToggleTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ToggleTemplate). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int) Type identifier of [ToggleRangeTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ToggleRangeTemplate). |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#) | [getErrorTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#getErrorTemplate())`()` <br /> |
| openstatic [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#) | [getNoTemplateObject](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#getNoTemplateObject())`()` Get a singleton [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#), which supports no direct user input. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#getTemplateId())`()` <br /> |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTemplateType](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#getTemplateType())`()` The template type associated with this class. |

## Constants

### TYPE_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ERROR: Int
```

Type identifier of the template returned by [getErrorTemplate()](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#getErrorTemplate()). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) 

 Value: -1

### TYPE_NO_TEMPLATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NO_TEMPLATE: Int
```

Type identifier of [ControlTemplate.getNoTemplateObject](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#getNoTemplateObject()). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) 

 Value: 0

### TYPE_RANGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_RANGE: Int
```

Type identifier of [RangeTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/RangeTemplate). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) 

 Value: 2

### TYPE_STATELESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_STATELESS: Int
```

Type identifier of [StatelessTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/StatelessTemplate). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) 

 Value: 8

### TYPE_TEMPERATURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEMPERATURE: Int
```

Type identifier of [TemperatureControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/TemperatureControlTemplate). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) 

 Value: 7

### TYPE_THUMBNAIL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_THUMBNAIL: Int
```

Type identifier of [ThumbnailTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ThumbnailTemplate). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) 

 Value: 3

### TYPE_TOGGLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TOGGLE: Int
```

Type identifier of [ToggleTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ToggleTemplate). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) 

 Value: 1

### TYPE_TOGGLE_RANGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TOGGLE_RANGE: Int
```

Type identifier of [ToggleRangeTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ToggleRangeTemplate). 
Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) 

 Value: 6

## Public methods

### getErrorTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getErrorTemplate(): ControlTemplate
```

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#) | a singleton [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#) used for indicating an error in unparceling. This value cannot be`null`. |

### getNoTemplateObject

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNoTemplateObject(): ControlTemplate
```

Get a singleton [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#), which supports no direct user input. Used by [Control.StatelessBuilder](https://developer.android.com/reference/kotlin/android/service/controls/Control.StatelessBuilder.html#) when there is no known state. Can also be used in [Control.StatefulBuilder](https://developer.android.com/reference/kotlin/android/service/controls/Control.StatefulBuilder.html#) for conveying information to a user about the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) but direct user interaction is not desired. Since this template has no corresponding [ControlAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction.html#), any user interaction will launch the [Control.getAppIntent()](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#getAppIntent()).

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#) | a singleton [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#) to indicate no specific template is used by this [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) This value cannot be`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.controls.templates.ControlTemplate#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_ERROR:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_NO_TEMPLATE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_NO_TEMPLATE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_THUMBNAIL](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_THUMBNAIL:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TOGGLE_RANGE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TOGGLE_RANGE:kotlin.Int), [android.service.controls.templates.ControlTemplate#TYPE_TEMPERATURE](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_TEMPERATURE:kotlin.Int), or [android.service.controls.templates.ControlTemplate#TYPE_STATELESS](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate#TYPE_STATELESS:kotlin.Int) |
