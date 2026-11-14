# ParcelableColorSpace

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParcelableColorSpace

Kotlin| [Java](ParcelableColorSpace.md) 
| --- | --- |

```
class ParcelableColorSpace : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.ParcelableColorSpace](ParcelableColorSpace.md) |

A [Parcelable](../android.os/Parcelable.md) wrapper for a [ColorSpace](ColorSpace.md). In order to enable parceling, the ColorSpace must be either a [Named](../android/graphics/ColorSpace.Named.md) ColorSpace or a [ColorSpace.Rgb](../android/graphics/ColorSpace.Rgb.md) instance that has an ICC parametric transfer function as returned by [ColorSpace.Rgb.getTransferParameters()](../android/graphics/ColorSpace.Rgb.md)).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ParcelableColorSpace](ParcelableColorSpace.md))`(`colorSpace:` ` [ColorSpace](ColorSpace.md)`)` Constructs a new ParcelableColorSpace that wraps the provided ColorSpace. |

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](ParcelableColorSpace.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](ParcelableColorSpace.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [ColorSpace](ColorSpace.md) | [getColorSpace](ParcelableColorSpace.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](ParcelableColorSpace.md))`()` <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParcelable](ParcelableColorSpace.md))`(`colorSpace:` ` [ColorSpace](ColorSpace.md)`)` Checks if the given ColorSpace is able to be parceled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](ParcelableColorSpace.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ParcelableColorSpace](ParcelableColorSpace.md)!\> | [CREATOR](ParcelableColorSpace.md) <br /> |

## Public constructors

### ParcelableColorSpace

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ParcelableColorSpace(colorSpace: ColorSpace)
```

Constructs a new ParcelableColorSpace that wraps the provided ColorSpace.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colorSpace` | [ColorSpace](ColorSpace.md):The ColorSpace to wrap. The ColorSpace must be either named or be an RGB ColorSpace with an ICC parametric transfer function. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the provided ColorSpace does not satisfy the requirements to be parceled. See [isParcelable(android.graphics.ColorSpace)](ParcelableColorSpace.md)). |

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| [ColorSpace](ColorSpace.md) | the backing ColorSpace that this ParcelableColorSpace is wrapping. This value cannot be`null`. |

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

Checks if the given ColorSpace is able to be parceled. A ColorSpace can only be parceled if it is a [Named](../android/graphics/ColorSpace.Named.md) ColorSpace or a [ColorSpace.Rgb](../android/graphics/ColorSpace.Rgb.md) instance that has an ICC parametric transfer function as returned by [ColorSpace.Rgb.getTransferParameters()](../android/graphics/ColorSpace.Rgb.md))

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------|
| `colorSpace` | [ColorSpace](ColorSpace.md):This value cannot be`null`. |

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
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ParcelableColorSpace!>
```
