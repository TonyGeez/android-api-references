Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WallpaperInstance

Kotlin | [Java](WallpaperInstance.md)
| --- | --- |

```
class WallpaperInstance : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.wallpaper.WallpaperInstance](WallpaperInstance.md) |

Describes a wallpaper that has been set as a current wallpaper.

This class is used by `https://developer.android.com/reference/kotlin/android/app/WallpaperManager.html#` to store information about a wallpaper that is currently in use. Because it has been set as an active wallpaper it offers some guarantees that `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription` does not:

- It contains the `https://developer.android.com/reference/kotlin/android/app/WallpaperInfo.html#` corresponding to the `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#`
specified in the description
- `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperInstance#getId()` is guaranteed to be non-null

<br />

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperInstance#WallpaperInstance(android.app.WallpaperInfo,%20android.app.wallpaper.WallpaperDescription)(info: https://developer.android.com/reference/kotlin/android/app/WallpaperInfo.html#?, description: https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription)` Create a WallpaperInstance for the wallpaper given by `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription`. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperInstance#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperInstance#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [WallpaperDescription](WallpaperDescription.md) | `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperInstance#getDescription()()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperInstance#getId()()` See `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#getId()` for rules about id uniqueness. |
| [WallpaperInfo](../android.app/WallpaperInfo.md)? | `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperInstance#getInfo()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperInstance#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperInstance#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WallpaperInstance](WallpaperInstance.md)!\> | `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperInstance#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### WallpaperInstance

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WallpaperInstance(
    info: WallpaperInfo?, 
    description: WallpaperDescription)
```

Create a WallpaperInstance for the wallpaper given by `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription`.

| Parameters ||
|---|---|
| `info` | [WallpaperInfo](../android.app/WallpaperInfo.md)?: the live wallpaper info for this wallpaper, or null if static |
| `description` | [WallpaperDescription](WallpaperDescription.md): description of the wallpaper for this instance |

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

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getDescription

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDescription(): WallpaperDescription
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription` | the description for this wallpaper |

### getId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): String
```

See `https://developer.android.com/reference/kotlin/android/app/wallpaper/WallpaperDescription#getId()` for rules about id uniqueness.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the ID of the wallpaper instance if given by the wallpaper description, otherwise a default value |

### getInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInfo(): WallpaperInfo?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/WallpaperInfo.html#?` | the live wallpaper info, or `null` if static |

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

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
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<WallpaperInstance!>
```
