Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BlackLevelPattern

Kotlin | [Java](BlackLevelPattern.md)
| --- | --- |

```
class BlackLevelPattern
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.BlackLevelPattern](BlackLevelPattern.md) |

Immutable class to store a 4-element vector of integers corresponding to a 2x2 pattern of color channel offsets used for the black level offsets of each color channel. For a camera device with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_MONOCHROME:kotlin.Int` capability, all 4 elements of the pattern will have the same value.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#COUNT:kotlin.Int` The number of offsets in this vector. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#BlackLevelPattern(kotlin.IntArray)(offsets: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Create a new `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#` from a given offset array. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#copyTo(kotlin.IntArray,%20kotlin.Int)(destination: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Copy the ColorChannel offsets into the destination vector. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Check if this `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#` is equal to another `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#getOffsetForIndex(kotlin.Int,%20kotlin.Int)(column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, row: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the color channel offset for a given index into the array of raw pixel values. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#toString()()` Return this `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#` as a string representation. |

## Constants

### COUNT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COUNT: Int
```

The number of offsets in this vector.

 Value: 4

## Public constructors

### BlackLevelPattern

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BlackLevelPattern(offsets: IntArray)
```

Create a new `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#` from a given offset array.

The given offset array must contain offsets for each color channel in a 2x2 pattern corresponding to the color filter arrangement. Offsets are given in row-column scan order.

This constructor is public to allow for easier application testing by creating custom object instances. It's not necessary to construct these objects during normal use of the camera API.

| Parameters ||
|---|---|
| `offsets` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): an array containing a 2x2 pattern of offsets. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given array has an incorrect length. |
| `java.lang.NullPointerException` | if the given array is null. |

## Public methods

### copyTo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun copyTo(
    destination: IntArray!, 
    offset: Int
): Unit
```

Copy the ColorChannel offsets into the destination vector.

Offsets are given in row-column scan order for a given 2x2 color pattern.

| Parameters ||
|---|---|
| `destination` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: an array big enough to hold at least {@value #COUNT} elements after the `offset` |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a non-negative offset into the array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if the destination vector is too small. |
| `java.lang.IllegalArgumentException` | if the offset is invalid. |
| `java.lang.NullPointerException` | if the destination is null. |
| --- | --- |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Check if this `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#` is equal to another `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#`.

Two vectors are only equal if and only if each of the respective elements is equal.

| Parameters ||
|---|---|
| `obj` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the objects were equal, `false` otherwise |

### getOffsetForIndex

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOffsetForIndex(
    column: Int, 
    row: Int
): Int
```

Return the color channel offset for a given index into the array of raw pixel values.

| Parameters ||
|---|---|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the column index in the the raw pixel array. |
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the row index in the raw pixel array. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a color channel offset. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if a column or row given is negative. |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Return this `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#` as a string representation.

`"BlackLevelPattern([%d, %d], [%d, %d])"`, where each `%d` represents one black level offset of a color channel. The values are in the same order as channels listed for the CFA layout key (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`).

A `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_MONOCHROME:kotlin.Int` camera only has one channel. As a result, the returned string will contain 4 identical values.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | string representation of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern#` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`
