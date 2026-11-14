Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AmbientBacklightMetadata

Kotlin | [Java](https://developer.android.com/reference/android/media/quality/AmbientBacklightMetadata "View this page in Java")

```
class AmbientBacklightMetadata : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.quality.AmbientBacklightMetadata](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#) |

Metadata of ambient backlight.

A metadata instance is sent from ambient backlight hardware in a `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent` with `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE:kotlin.Int`.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#ALGORITHM_NONE:kotlin.Int` The compress algorithm is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#ALGORITHM_RLE:kotlin.Int` The compress algorithm is run length encoding (RLE). |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#AmbientBacklightMetadata(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.IntArray)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, compressAlgorithm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, colorFormat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, horizontalZonesNumber: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, verticalZonesNumber: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, zonesColors: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Constructs AmbientBacklightMetadata. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#getColorFormat()()` Gets color format. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#getCompressionAlgorithm()()` Gets compress algorithm. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#getHorizontalZonesCount()()` Gets the number of horizontal color zones. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#getPackageName()()` Gets package name of the metadata. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#getSource()()` Gets source of ambient backlight detection. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#getVerticalZonesCount()()` Gets the number of vertical color zones. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#getZoneColors()()` Gets color data of all available color zones. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AmbientBacklightMetadata](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#)!\> | `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### ALGORITHM_NONE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALGORITHM_NONE: Int
```

The compress algorithm is disabled.

 Value: 0

### ALGORITHM_RLE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALGORITHM_RLE: Int
```

The compress algorithm is run length encoding (RLE).

 Value: 1

## Public constructors

### AmbientBacklightMetadata

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AmbientBacklightMetadata(
    packageName: String, 
    compressAlgorithm: Int, 
    source: Int, 
    colorFormat: Int, 
    horizontalZonesNumber: Int, 
    verticalZonesNumber: Int, 
    zonesColors: IntArray)
```

Constructs AmbientBacklightMetadata.

| Parameters ||
|---|---|
| `compressAlgorithm` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#ALGORITHM_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#ALGORITHM_RLE:kotlin.Int` |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightSettings#SOURCE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightSettings#SOURCE_AUDIO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightSettings#SOURCE_VIDEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightSettings#SOURCE_AUDIO_VIDEO:kotlin.Int` |
| `colorFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_F16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_1010102:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_565:kotlin.Int` |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getColorFormat

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColorFormat(): Int
```

Gets color format.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_F16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_1010102:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_565:kotlin.Int` |

### getCompressionAlgorithm

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCompressionAlgorithm(): Int
```

Gets compress algorithm.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#ALGORITHM_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#ALGORITHM_RLE:kotlin.Int` |

### getHorizontalZonesCount

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHorizontalZonesCount(): Int
```

Gets the number of horizontal color zones.

A color zone is represented by one single aggregated color. The number should not be larger than 128.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between 0 and 128 inclusive |

### getPackageName

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageName(): String
```

Gets package name of the metadata.

### getSource

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSource(): Int
```

Gets source of ambient backlight detection.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightSettings#SOURCE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightSettings#SOURCE_AUDIO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightSettings#SOURCE_VIDEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightSettings#SOURCE_AUDIO_VIDEO:kotlin.Int` |

### getVerticalZonesCount

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVerticalZonesCount(): Int
```

Gets the number of vertical color zones.

A color zone is represented by one single aggregated color. The number should not be larger than 80.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between 0 and 80 inclusive |

### getZoneColors

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getZoneColors(): IntArray
```

Gets color data of all available color zones.

The format of the color data can be found at `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#getColorFormat()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | an array of color data, in row by row (left-to-right then top-to-bottom) order of the color zones. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#getHorizontalZonesCount()`
- `https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata#getVerticalZonesCount()`

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AmbientBacklightMetadata!>
```
