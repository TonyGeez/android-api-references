# WallpaperDescription

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WallpaperDescription

Kotlin| [Java](../android/app/wallpaper/WallpaperDescription.md) 
| --- | --- |

```
class WallpaperDescription : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.wallpaper.WallpaperDescription](../android/app/wallpaper/WallpaperDescription.md) |

Describes a wallpaper, including associated metadata and optional content to be used by its [android.service.wallpaper.WallpaperService.Engine](../android/service/wallpaper/WallpaperService.Engine.md), the [ComponentName](../android/content/ComponentName.md) to be used by [android.app.WallpaperManager](../android/app/WallpaperManager.md), and an optional id to differentiate between different distinct wallpapers rendered by the same wallpaper service.

This class is used to communicate among a wallpaper rendering service, a wallpaper chooser UI, and [android.app.WallpaperManager](../android/app/WallpaperManager.md). This class describes a specific instance of a live wallpaper, unlike [WallpaperInfo](../android/app/WallpaperInfo.md) which is common to all instances of a wallpaper component. Each [WallpaperDescription](../android/app/wallpaper/WallpaperDescription.md) can have distinct metadata.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/app/wallpaper/WallpaperDescription.Builder.md) Builder for the immutable [WallpaperDescription](../android/app/wallpaper/WallpaperDescription.md) class |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/app/wallpaper/WallpaperDescription.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/app/wallpaper/WallpaperDescription.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [ComponentName](../android/content/ComponentName.md)? | [getComponent](../android/app/wallpaper/WallpaperDescription.md))`()` <br /> |
| --- | --- |
| [PersistableBundle](../android/os/PersistableBundle.md) | [getContent](../android/app/wallpaper/WallpaperDescription.md))`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getContextDescription](../android/app/wallpaper/WallpaperDescription.md))`()` <br /> |
| [Uri](../android/net/Uri.md)? | [getContextUri](../android/app/wallpaper/WallpaperDescription.md))`()` <br /> |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\> | [getDescription](../android/app/wallpaper/WallpaperDescription.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getId](../android/app/wallpaper/WallpaperDescription.md))`()` <br /> |
| [Uri](../android/net/Uri.md)? | [getThumbnail](../android/app/wallpaper/WallpaperDescription.md))`()` <br /> |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getTitle](../android/app/wallpaper/WallpaperDescription.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/app/wallpaper/WallpaperDescription.md))`()` <br /> |
| [WallpaperDescription.Builder](../android/app/wallpaper/WallpaperDescription.Builder.md) | [toBuilder](../android/app/wallpaper/WallpaperDescription.md))`()` Convert the current description to a [Builder](../android/app/wallpaper/WallpaperDescription.Builder.md). |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/app/wallpaper/WallpaperDescription.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/app/wallpaper/WallpaperDescription.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WallpaperDescription](../android/app/wallpaper/WallpaperDescription.md)!\> | [CREATOR](../android/app/wallpaper/WallpaperDescription.md) <br /> |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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
| [ComponentName](../android/content/ComponentName.md)? | the component for this wallpaper, or`null`for a static wallpaper |

### getContent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContent(): PersistableBundle
```

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [PersistableBundle](../android/os/PersistableBundle.md) | any additional content required to render this wallpaper |

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
| [Uri](../android/net/Uri.md)? | the [Uri](../android/net/Uri.md) for the action associated with the wallpaper, or`null`if not provided |

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
| [Uri](../android/net/Uri.md)? | the thumbnail for this wallpaper, or`null`if not provided |

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

Convert the current description to a [Builder](../android/app/wallpaper/WallpaperDescription.Builder.md).

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [WallpaperDescription.Builder](../android/app/wallpaper/WallpaperDescription.Builder.md) | the Builder representing this description |

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
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WallpaperDescription!>
```
