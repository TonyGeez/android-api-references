Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintAttributes

Kotlin | [Java](PrintAttributes.md)
| --- | --- |

```
class PrintAttributes : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.print.PrintAttributes](PrintAttributes.md) |

This class represents the attributes of a print job. These attributes describe how the printed content should be laid out. For example, the print attributes may state that the content should be laid out on a letter size with 300 DPI (dots per inch) resolution, have a margin of 10 mills (thousand of an inch) on all sides, and be black and white.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/print/PrintAttributes.Builder` Builder for creating PrintAttributes. |
| | `https://developer.android.com/reference/kotlin/android/print/PrintAttributes.Margins` This class specifies content margins. |
| | `https://developer.android.com/reference/kotlin/android/print/PrintAttributes.MediaSize` This class specifies a supported media size. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/print/PrintAttributes.Resolution` This class specifies a supported resolution in DPI (dots per inch). |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/print/PrintAttributes#COLOR_MODE_COLOR:kotlin.Int` Color mode: Color color scheme, for example many colors are used. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/print/PrintAttributes#COLOR_MODE_MONOCHROME:kotlin.Int` Color mode: Monochrome color scheme, for example one color is used. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/print/PrintAttributes#DUPLEX_MODE_LONG_EDGE:kotlin.Int` Duplex mode: Pages are turned sideways along the long edge - like a book. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/print/PrintAttributes#DUPLEX_MODE_NONE:kotlin.Int` Duplex mode: No duplexing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/print/PrintAttributes#DUPLEX_MODE_SHORT_EDGE:kotlin.Int` Duplex mode: Pages are turned upwards along the short edge - like a notpad. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getColorMode Gets the color mode. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDuplexMode Gets the duplex mode. |
| [PrintAttributes.MediaSize](../android/print/PrintAttributes.MediaSize.md)? | getMediaSize Gets the media size. |
| [PrintAttributes.Margins](../android/print/PrintAttributes.Margins.md)? | getMinMargins Gets the minimal margins. |
| --- | --- |
| [PrintAttributes.Resolution](../android/print/PrintAttributes.Resolution.md)? | getResolution Gets the resolution. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PrintAttributes](PrintAttributes.md)!\> | `https://developer.android.com/reference/kotlin/android/print/PrintAttributes#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### COLOR_MODE_COLOR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_MODE_COLOR: Int
```

Color mode: Color color scheme, for example many colors are used.

 Value: 2

### COLOR_MODE_MONOCHROME

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_MODE_MONOCHROME: Int
```

Color mode: Monochrome color scheme, for example one color is used.

 Value: 1

### DUPLEX_MODE_LONG_EDGE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DUPLEX_MODE_LONG_EDGE: Int
```

Duplex mode: Pages are turned sideways along the long edge - like a book.

 Value: 2

### DUPLEX_MODE_NONE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DUPLEX_MODE_NONE: Int
```

Duplex mode: No duplexing.

 Value: 1

### DUPLEX_MODE_SHORT_EDGE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DUPLEX_MODE_SHORT_EDGE: Int
```

Duplex mode: Pages are turned upwards along the short edge - like a notpad.

 Value: 4

## Public methods

### describeContents

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `obj` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getColorMode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColorMode(): Int
```

Gets the color mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The color mode or zero if not set. Value is 0 or greater |

**See Also**

- `https://developer.android.com/reference/kotlin/android/print/PrintAttributes#COLOR_MODE_COLOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/print/PrintAttributes#COLOR_MODE_MONOCHROME:kotlin.Int`

### getDuplexMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDuplexMode(): Int
```

Gets the duplex mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The duplex mode or zero if not set. Value is 0 or greater |

**See Also**

- `https://developer.android.com/reference/kotlin/android/print/PrintAttributes#DUPLEX_MODE_NONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/print/PrintAttributes#DUPLEX_MODE_LONG_EDGE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/print/PrintAttributes#DUPLEX_MODE_SHORT_EDGE:kotlin.Int`

### getMediaSize

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMediaSize(): PrintAttributes.MediaSize?
```

Gets the media size.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/print/PrintAttributes.MediaSize?` | The media size or `null` if not set. |

### getMinMargins

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMinMargins(): PrintAttributes.Margins?
```

Gets the minimal margins. If the content does not fit these margins it will be clipped.

**These margins are physically imposed by the printer and they are *not* rotated, i.e. they are the same for both portrait and landscape. For example, a printer may not be able to print in a stripe on both left and right sides of the page.**

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/print/PrintAttributes.Margins?` | The margins or `null` if not set. |

### getResolution

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResolution(): PrintAttributes.Resolution?
```

Gets the resolution.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/print/PrintAttributes.Resolution?` | The resolution or `null` if not set. |

### hashCode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PrintAttributes!>
```
