# WallpaperDescription

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WallpaperDescription

Kotlin| [Java](https://developer.android.com/reference/android/app/wallpaper/WallpaperDescription "View this page in Java") 

```
class WallpaperDescription : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.wallpaper.WallpaperDescription](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#) |

Describes a wallpaper, including associated metadata and optional content to be used by its [android.service.wallpaper.WallpaperService.Engine](https://developer.android.com/reference/kotlin/android/service/wallpaper/WallpaperService.Engine.html#), the [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) to be used by [android.app.WallpaperManager](https://developer.android.com/reference/kotlin/android/app/WallpaperManager.html#), and an optional id to differentiate between different distinct wallpapers rendered by the same wallpaper service.

This class is used to communicate among a wallpaper rendering service, a wallpaper chooser UI, and [android.app.WallpaperManager](https://developer.android.com/reference/kotlin/android/app/WallpaperManager.html#). This class describes a specific instance of a live wallpaper, unlike [WallpaperInfo](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo.html#) which is common to all instances of a wallpaper component. Each [WallpaperDescription](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#) can have distinct metadata.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription.Builder) Builder for the immutable [WallpaperDescription](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#) class |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)? | [getComponent](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#getComponent())`()` <br /> |
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) | [getContent](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#getContent())`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getContextDescription](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#getContextDescription())`()` <br /> |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [getContextUri](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#getContextUri())`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\> | [getDescription](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#getDescription())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getId](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#getId())`()` <br /> |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [getThumbnail](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#getThumbnail())`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getTitle](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#getTitle())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#hashCode())`()` <br /> |
| [WallpaperDescription.Builder](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription.Builder) | [toBuilder](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#toBuilder())`()` Convert the current description to a [Builder](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription.Builder). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [WallpaperDescription](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getComponent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getComponent(): ComponentName?
```

| Return ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)? | the component for this wallpaper, or`null`for a static wallpaper |

### getContent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContent(): PersistableBundle
```

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) | any additional content required to render this wallpaper |

### getContextDescription

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContextDescription(): CharSequence?
```

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | the description for the action associated with the wallpaper, or`null`if not provided |

### getContextUri

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContextUri(): Uri?
```

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | the [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) for the action associated with the wallpaper, or`null`if not provided |

### getDescription

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDescription(): MutableList<CharSequence!>
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!> | the description for this wallpaper, with each list element intended to be shown on a separate line in the UI |

### getId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the id for this wallpaper, or`null`if not provided |

### getThumbnail

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getThumbnail(): Uri?
```

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | the thumbnail for this wallpaper, or`null`if not provided |

### getTitle

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTitle(): CharSequence?
```

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | the title for this wallpaper, or`null`if not provided |

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toBuilder

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toBuilder(): WallpaperDescription.Builder
```

Convert the current description to a [Builder](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription.Builder).

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [WallpaperDescription.Builder](https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription.Builder) | the Builder representing this description |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WallpaperDescription!>
```
