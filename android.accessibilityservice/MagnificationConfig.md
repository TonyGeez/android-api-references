# MagnificationConfig

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MagnificationConfig

Kotlin | [Java](MagnificationConfig.md) 
| --- | --- |

```
class MagnificationConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.accessibilityservice.MagnificationConfig](MagnificationConfig.md) |

This class describes the magnification config for [AccessibilityService](AccessibilityService.md) to control the magnification.

When the magnification config uses [MAGNIFICATION_MODE_DEFAULT](MagnificationConfig.md), [AccessibilityService](AccessibilityService.md) will be able to control the activated magnifier on the display. If there is no magnifier activated, it controls the last-activated magnification mode. If there is no magnifier activated before, it controls full-screen magnifier by default.

When the magnification config uses [MAGNIFICATION_MODE_FULLSCREEN](MagnificationConfig.md). [AccessibilityService](AccessibilityService.md) will be able to control full-screen magnifier on the display.

When the magnification config uses [MAGNIFICATION_MODE_WINDOW](MagnificationConfig.md) and the platform supports [android.content.pm.PackageManager#FEATURE_WINDOW_MAGNIFICATION](../android.content.pm/PackageManager.md) feature. [AccessibilityService](AccessibilityService.md) will be able to control window magnifier on the display.

If the other magnification configs, scale centerX and centerY, are not set by the [Builder](../android/accessibilityservice/MagnificationConfig.Builder.md), the configs should be current values or default values. And the center position ordinarily is the center of the screen.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/accessibilityservice/MagnificationConfig.Builder.md) Builder for creating [MagnificationConfig](MagnificationConfig.md) objects. |

| Constants ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAGNIFICATION_MODE_DEFAULT](MagnificationConfig.md) The controlling magnification mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAGNIFICATION_MODE_FULLSCREEN](MagnificationConfig.md) The controlling magnification mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAGNIFICATION_MODE_WINDOW](MagnificationConfig.md) The controlling magnification mode. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](MagnificationConfig.md))`()` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCenterX](MagnificationConfig.md))`()` Returns the screen-relative X coordinate of the center of the magnification viewport. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCenterY](MagnificationConfig.md))`()` Returns the screen-relative Y coordinate of the center of the magnification viewport. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMode](MagnificationConfig.md))`()` Returns the magnification mode that is the current activated mode or the controlling mode of the config. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getScale](MagnificationConfig.md))`()` Returns the magnification scale of the controlling magnifier |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isActivated](MagnificationConfig.md))`()` Returns the activated state of the controlling magnifier. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](MagnificationConfig.md))`()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](MagnificationConfig.md))`(`parcel:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [MagnificationConfig](MagnificationConfig.md)!\> | [CREATOR](MagnificationConfig.md) <br /> |

## Constants

### MAGNIFICATION_MODE_DEFAULT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAGNIFICATION_MODE_DEFAULT: Int
```

The controlling magnification mode. It controls the activated magnifier. 

 Value: 0

### MAGNIFICATION_MODE_FULLSCREEN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAGNIFICATION_MODE_FULLSCREEN: Int
```

The controlling magnification mode. It controls full-screen magnifier. 

 Value: 1

### MAGNIFICATION_MODE_WINDOW

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAGNIFICATION_MODE_WINDOW: Int
```

The controlling magnification mode. It is valid if the platform supports [android.content.pm.PackageManager#FEATURE_WINDOW_MAGNIFICATION](../android.content.pm/PackageManager.md) feature. 

 Value: 2

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getCenterX

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCenterX(): Float
```

Returns the screen-relative X coordinate of the center of the magnification viewport.

| Return ||
|--------------------------------------------------------------------------------|------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The X coordinate |

### getCenterY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCenterY(): Float
```

Returns the screen-relative Y coordinate of the center of the magnification viewport.

| Return ||
|--------------------------------------------------------------------------------|------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The Y coordinate |

### getMode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMode(): Int
```

Returns the magnification mode that is the current activated mode or the controlling mode of the config.

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The magnification mode |

### getScale

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getScale(): Float
```

Returns the magnification scale of the controlling magnifier

| Return ||
|--------------------------------------------------------------------------------|-------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The magnification scale |

### isActivated

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isActivated(): Boolean
```

Returns the activated state of the controlling magnifier. The controlling magnifier can be activated even if the scale returned by [MagnificationConfig.getScale()](MagnificationConfig.md)) equals to 1.0.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the magnifier is activated and showing on screen, `false` otherwise. |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be `null`. |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `parcel` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<MagnificationConfig!>
```  
**See Also**

- [android.os.Parcelable.Creator](../android/os/Parcelable.Creator.md)
