Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SizeF

```
class SizeF : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.SizeF](SizeF.md) |

Immutable class for describing width and height dimensions in some arbitrary unit.

Width and height are finite values stored as a floating point representation.

## Summary

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| SizeF Create a new immutable SizeF instance. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Parcelable interface methods |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Check if this size is equal to another size. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getHeight Get the height of the size (as an arbitrary unit). |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getWidth Get the width of the size (as an arbitrary unit). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| static [SizeF](SizeF.md)! | parseSizeF Parses the specified string as a size value. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Return the size represented as a string with the format `"WxH"` |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Write this size to the specified parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SizeF](SizeF.md)!\> | `https://developer.android.com/reference/kotlin/android/util/SizeF#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### SizeF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SizeF(
    width: Float, 
    height: Float)
```

Create a new immutable SizeF instance.

Both the `width` and the `height` must be a finite number. In particular, `NaN` and positive/negative infinity are illegal values.

| Parameters ||
|---|---|
| `width` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The width of the size |
| `height` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The height of the size |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if either `width` or `height` was not finite. |

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Parcelable interface methods

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Check if this size is equal to another size.

Two sizes are equal if and only if both their widths and heights are the same.

For this purpose, the width/height float values are considered to be the same if and only if the method floatToIntBits returns the identical `int` value when applied to each.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the objects were equal, `false` otherwise |

### getHeight

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHeight(): Float
```

Get the height of the size (as an arbitrary unit).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | height |

### getWidth

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWidth(): Float
```

Get the width of the size (as an arbitrary unit).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | width |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### parseSizeF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parseSizeF(string: String!): SizeF!
```

Parses the specified string as a size value.

The ASCII characters `\``u002a` ('\*') and `\``u0078` ('x') are recognized as separators between the width and height.

For any `SizeF s`: `SizeF.parseSizeF(s.toString()).equals(s)`. However, the method also handles sizes expressed in the following forms:

"*width* `x`*height* " or "*width* `*`*height* " `=> new SizeF(width, height)`, where *width* and *height* are string floats potentially containing a sign, such as "-10.3", "+7" or "5.2", but not containing an `'x'` (such as a float in hexadecimal string format).

```kotlin
<code>SizeF.parseSizeF("3.2*+6").equals(new SizeF(3.2f, 6.0f)) == true
  SizeF.parseSizeF("-3x-6").equals(new SizeF(-3.0f, -6.0f)) == true
  SizeF.parseSizeF("4 by 3") =&gt; throws NumberFormatException
  </code>
```

| Parameters ||
|---|---|
| `string` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the string representation of a size value. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/SizeF#!` | the size value represented by `string`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `string` was `null` |
| `java.lang.NumberFormatException` | if `string` cannot be parsed as a size value. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Return the size represented as a string with the format `"WxH"`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | string representation of the size |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Write this size to the specified parcel. To restore a size from a parcel, use the `https://developer.android.com/reference/kotlin/android/util/SizeF#CREATOR:android.os.Parcelable.Creator`.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `out` | [Parcel](../android.os/Parcel.md): The parcel to write the point's coordinates into. This value cannot be `null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<SizeF!>
```
