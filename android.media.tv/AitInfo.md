# AitInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AitInfo

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/AitInfo "View this page in Java") 

```
class AitInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.tv.AitInfo](https://developer.android.com/reference/kotlin/android/media/tv/AitInfo#) |

AIT (Application Information Table) info.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AitInfo](https://developer.android.com/reference/kotlin/android/media/tv/AitInfo#AitInfo(kotlin.Int,%20kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `version:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs AIT info. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/tv/AitInfo#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/media/tv/AitInfo#getType())`()` Gets interactive app type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersion](https://developer.android.com/reference/kotlin/android/media/tv/AitInfo#getVersion())`()` Gets version. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/tv/AitInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/tv/AitInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AitInfo](https://developer.android.com/reference/kotlin/android/media/tv/AitInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/tv/AitInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### AitInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AitInfo(
    type: Int, 
    version: Int)
```

Constructs AIT info.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_HBBTV](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_HBBTV:kotlin.Int), [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_ATSC](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_ATSC:kotlin.Int), [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_GINGA](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_GINGA:kotlin.Int), [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_TARGETED_AD](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_TARGETED_AD:kotlin.Int), or [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_OTHER:kotlin.Int) |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Gets interactive app type.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_HBBTV](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_HBBTV:kotlin.Int), [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_ATSC](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_ATSC:kotlin.Int), [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_GINGA](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_GINGA:kotlin.Int), [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_TARGETED_AD](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_TARGETED_AD:kotlin.Int), or [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_OTHER:kotlin.Int) |

### getVersion

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVersion(): Int
```

Gets version. 

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AitInfo!>
```
