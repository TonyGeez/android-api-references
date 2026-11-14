# ParcelableColorSpace

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParcelableColorSpace

Kotlin| [Java](https://developer.android.com/reference/android/graphics/ParcelableColorSpace "View this page in Java") 
| --- | --- |

```
class ParcelableColorSpace : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.ParcelableColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ParcelableColorSpace#) |

A [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) wrapper for a [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace). In order to enable parceling, the ColorSpace must be either a [Named](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) ColorSpace or a [ColorSpace.Rgb](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb) instance that has an ICC parametric transfer function as returned by [ColorSpace.Rgb.getTransferParameters()](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb#getTransferParameters()).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ParcelableColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ParcelableColorSpace#ParcelableColorSpace(android.graphics.ColorSpace))`(`colorSpace:` ` [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)`)` Constructs a new ParcelableColorSpace that wraps the provided ColorSpace. |

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/graphics/ParcelableColorSpace#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/graphics/ParcelableColorSpace#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace) | [getColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ParcelableColorSpace#getColorSpace())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/graphics/ParcelableColorSpace#hashCode())`()` <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParcelable](https://developer.android.com/reference/kotlin/android/graphics/ParcelableColorSpace#isParcelable(android.graphics.ColorSpace))`(`colorSpace:` ` [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)`)` Checks if the given ColorSpace is able to be parceled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/graphics/ParcelableColorSpace#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ParcelableColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ParcelableColorSpace#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/graphics/ParcelableColorSpace#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### ParcelableColorSpace

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ParcelableColorSpace(colorSpace: ColorSpace)
```

Constructs a new ParcelableColorSpace that wraps the provided ColorSpace.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace):The ColorSpace to wrap. The ColorSpace must be either named or be an RGB ColorSpace with an ICC parametric transfer function. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the provided ColorSpace does not satisfy the requirements to be parceled. See [isParcelable(android.graphics.ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/ParcelableColorSpace#isParcelable(android.graphics.ColorSpace)). |

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getColorSpace

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getColorSpace(): ColorSpace
```

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace) | the backing ColorSpace that this ParcelableColorSpace is wrapping. This value cannot be`null`. |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isParcelable

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isParcelable(colorSpace: ColorSpace): Boolean
```

Checks if the given ColorSpace is able to be parceled. A ColorSpace can only be parceled if it is a [Named](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) ColorSpace or a [ColorSpace.Rgb](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb) instance that has an ICC parametric transfer function as returned by [ColorSpace.Rgb.getTransferParameters()](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb#getTransferParameters())

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------|
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace):This value cannot be`null`. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ParcelableColorSpace!>
```
