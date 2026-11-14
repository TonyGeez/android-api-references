# MagnificationConfig

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MagnificationConfig

Kotlin | [Java](https://developer.android.com/reference/android/accessibilityservice/MagnificationConfig "View this page in Java") 
| --- | --- |

```
class MagnificationConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.accessibilityservice.MagnificationConfig](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#) |

This class describes the magnification config for [AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService) to control the magnification.

When the magnification config uses [MAGNIFICATION_MODE_DEFAULT](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#MAGNIFICATION_MODE_DEFAULT:kotlin.Int), [AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService) will be able to control the activated magnifier on the display. If there is no magnifier activated, it controls the last-activated magnification mode. If there is no magnifier activated before, it controls full-screen magnifier by default.

When the magnification config uses [MAGNIFICATION_MODE_FULLSCREEN](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#MAGNIFICATION_MODE_FULLSCREEN:kotlin.Int). [AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService) will be able to control full-screen magnifier on the display.

When the magnification config uses [MAGNIFICATION_MODE_WINDOW](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#MAGNIFICATION_MODE_WINDOW:kotlin.Int) and the platform supports [android.content.pm.PackageManager#FEATURE_WINDOW_MAGNIFICATION](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_WINDOW_MAGNIFICATION:kotlin.String) feature. [AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService) will be able to control window magnifier on the display.

If the other magnification configs, scale centerX and centerY, are not set by the [Builder](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig.Builder), the configs should be current values or default values. And the center position ordinarily is the center of the screen.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig.Builder) Builder for creating [MagnificationConfig](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#) objects. |

| Constants ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAGNIFICATION_MODE_DEFAULT](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#MAGNIFICATION_MODE_DEFAULT:kotlin.Int) The controlling magnification mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAGNIFICATION_MODE_FULLSCREEN](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#MAGNIFICATION_MODE_FULLSCREEN:kotlin.Int) The controlling magnification mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAGNIFICATION_MODE_WINDOW](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#MAGNIFICATION_MODE_WINDOW:kotlin.Int) The controlling magnification mode. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#describeContents())`()` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCenterX](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#getCenterX())`()` Returns the screen-relative X coordinate of the center of the magnification viewport. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCenterY](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#getCenterY())`()` Returns the screen-relative Y coordinate of the center of the magnification viewport. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMode](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#getMode())`()` Returns the magnification mode that is the current activated mode or the controlling mode of the config. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getScale](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#getScale())`()` Returns the magnification scale of the controlling magnifier |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isActivated](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#isActivated())`()` Returns the activated state of the controlling magnifier. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#toString())`()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [MagnificationConfig](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#CREATOR:android.os.Parcelable.Creator) <br /> |

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

The controlling magnification mode. It is valid if the platform supports [android.content.pm.PackageManager#FEATURE_WINDOW_MAGNIFICATION](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_WINDOW_MAGNIFICATION:kotlin.String) feature. 

 Value: 2

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

Returns the activated state of the controlling magnifier. The controlling magnifier can be activated even if the scale returned by [MagnificationConfig.getScale()](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig#getScale()) equals to 1.0.

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `parcel` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<MagnificationConfig!>
```  
**See Also**

- [android.os.Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)
