# AmbientBacklightSettings

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AmbientBacklightSettings

Kotlin| [Java](AmbientBacklightSettings.md) 
| --- | --- |

```
class AmbientBacklightSettings : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.quality.AmbientBacklightSettings](AmbientBacklightSettings.md) |

Settings to configure ambient backlight hardware.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_AUDIO](AmbientBacklightSettings.md) The detection is enabled for audio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_AUDIO_VIDEO](AmbientBacklightSettings.md) The detection is enabled for audio and video. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_NONE](AmbientBacklightSettings.md) The detection is disabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_VIDEO](AmbientBacklightSettings.md) The detection is enabled for video. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AmbientBacklightSettings](AmbientBacklightSettings.md))`(`source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxFps:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `colorFormat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `horizontalZonesNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `verticalZonesNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isLetterboxOmitted:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `threshold:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs AmbientBacklightSettings. |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](AmbientBacklightSettings.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColorFormat](AmbientBacklightSettings.md))`()` Gets color format. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHorizontalZonesCount](AmbientBacklightSettings.md))`()` Gets the number of horizontal color zones. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxFps](AmbientBacklightSettings.md))`()` Gets max frames per second. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSource](AmbientBacklightSettings.md))`()` Gets source of ambient backlight detection. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getThreshold](AmbientBacklightSettings.md))`()` Gets the detection threshold of the ambient light. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVerticalZonesCount](AmbientBacklightSettings.md))`()` Gets the number of vertical color zones. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLetterboxOmitted](AmbientBacklightSettings.md))`()` Returns`true`if the black portion of the screen in letter box mode is omitted;`false`otherwise. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AmbientBacklightSettings.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](AmbientBacklightSettings.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AmbientBacklightSettings](AmbientBacklightSettings.md)!\> | [CREATOR](AmbientBacklightSettings.md) <br /> |

## Constants

### SOURCE_AUDIO

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_AUDIO: Int
```

The detection is enabled for audio. 

 Value: 1

### SOURCE_AUDIO_VIDEO

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_AUDIO_VIDEO: Int
```

The detection is enabled for audio and video. 

 Value: 3

### SOURCE_NONE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_NONE: Int
```

The detection is disabled. 

 Value: 0

### SOURCE_VIDEO

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_VIDEO: Int
```

The detection is enabled for video. 

 Value: 2

## Public constructors

### AmbientBacklightSettings

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AmbientBacklightSettings(
    source: Int, 
    maxFps: Int, 
    colorFormat: Int, 
    horizontalZonesNumber: Int, 
    verticalZonesNumber: Int, 
    isLetterboxOmitted: Boolean, 
    threshold: Int)
```

Constructs AmbientBacklightSettings.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.quality.AmbientBacklightSettings#SOURCE_NONE](AmbientBacklightSettings.md), [android.media.quality.AmbientBacklightSettings#SOURCE_AUDIO](AmbientBacklightSettings.md), [android.media.quality.AmbientBacklightSettings#SOURCE_VIDEO](AmbientBacklightSettings.md), or [android.media.quality.AmbientBacklightSettings#SOURCE_AUDIO_VIDEO](AmbientBacklightSettings.md) |
| `colorFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.graphics.PixelFormat#RGBA_8888](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#RGBX_8888](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#RGBA_F16](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#RGBA_1010102](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#RGB_888](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#RGB_565](../android.graphics/PixelFormat.md), or android.graphics.PixelFormat.R_8 |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getColorFormat

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getColorFormat(): Int
```

Gets color format.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.graphics.PixelFormat#RGBA_8888](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#RGBX_8888](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#RGBA_F16](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#RGBA_1010102](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#RGB_888](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#RGB_565](../android.graphics/PixelFormat.md), or android.graphics.PixelFormat.R_8 |

### getHorizontalZonesCount

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHorizontalZonesCount(): Int
```

Gets the number of horizontal color zones.

A color zone is a group of lights that always display the same color.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

### getMaxFps

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxFps(): Int
```

Gets max frames per second.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 1 or greater |

### getSource

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSource(): Int
```

Gets source of ambient backlight detection.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.quality.AmbientBacklightSettings#SOURCE_NONE](AmbientBacklightSettings.md), [android.media.quality.AmbientBacklightSettings#SOURCE_AUDIO](AmbientBacklightSettings.md), [android.media.quality.AmbientBacklightSettings#SOURCE_VIDEO](AmbientBacklightSettings.md), or [android.media.quality.AmbientBacklightSettings#SOURCE_AUDIO_VIDEO](AmbientBacklightSettings.md) |

### getThreshold

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getThreshold(): Int
```

Gets the detection threshold of the ambient light.

If the color of a color zone is changed but the difference is smaller than the threshold, the change is ignored. 

### getVerticalZonesCount

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVerticalZonesCount(): Int
```

Gets the number of vertical color zones.

A color zone is a group of lights that always display the same color.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

### isLetterboxOmitted

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLetterboxOmitted(): Boolean
```

Returns`true`if the black portion of the screen in letter box mode is omitted;`false`otherwise.

Letter-box is a technique to keep the original aspect ratio when displayed on a screen with different aspect ratio. Black bars are added to the top and bottom. 

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AmbientBacklightSettings!>
```
