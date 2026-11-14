Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ColorSpaceTransform

Kotlin | [Java](https://developer.android.com/reference/android/hardware/camera2/params/ColorSpaceTransform "View this page in Java")
| --- | --- |

```
class ColorSpaceTransform
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.ColorSpaceTransform](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#) |

Immutable class for describing a 3x3 matrix of `https://developer.android.com/reference/kotlin/android/util/Rational.html#` values in row-major order.

This matrix maps a transform from one color space to another. For the particular color space source and target, see the appropriate camera metadata documentation for the key that provides this value.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#ColorSpaceTransform(kotlin.Array)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/util/Rational.html#!>!)` Create a new immutable `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#` instance from a `https://developer.android.com/reference/kotlin/android/util/Rational.html#` array. |
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#ColorSpaceTransform(kotlin.IntArray)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)` Create a new immutable `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#` instance from an `int` array. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#copyElements(kotlin.Array,%20kotlin.Int)(destination: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/util/Rational.html#!>!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Copy the `https://developer.android.com/reference/kotlin/android/util/Rational.html#` elements in row-major order from this matrix into the destination. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#copyElements(kotlin.IntArray,%20kotlin.Int)(destination: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Copy the `https://developer.android.com/reference/kotlin/android/util/Rational.html#` elements in row-major order from this matrix into the destination. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Check if this `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#` is equal to another `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#`. |
| --- | --- |
| [Rational](https://developer.android.com/reference/kotlin/android/util/Rational.html#)! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#getElement(kotlin.Int,%20kotlin.Int)(column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, row: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get an element of this matrix by its row and column. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#toString()()` Return the color space transform as a string representation. |
| --- | --- |

## Public constructors

### ColorSpaceTransform

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ColorSpaceTransform(elements: Array<Rational!>!)
```

Create a new immutable `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#` instance from a `https://developer.android.com/reference/kotlin/android/util/Rational.html#` array.

The elements must be stored in a row-major order.

| Parameters ||
|---|---|
| `elements` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Rational](https://developer.android.com/reference/kotlin/android/util/Rational.html#)!\>!: An array of `9` elements |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the count of `elements` is not `9` |
| `java.lang.NullPointerException` | if `elements` or any sub-element is `null` |

### ColorSpaceTransform

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ColorSpaceTransform(elements: IntArray!)
```

Create a new immutable `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#` instance from an `int` array.

The elements must be stored in a row-major order. Each rational is stored contiguously as a `(numerator, denominator)` pair.

In particular:

```kotlin
<code>int[] elements = new int[
      N11, D11, N12, D12, N13, D13,
      N21, D21, N22, D22, N23, D23,
      N31, D31, N32, D32, N33, D33
  ];
 
  new ColorSpaceTransform(elements)</code>
```
where `Nij` and `Dij` is the numerator and denominator for row `i` and column `j`.

<br />

| Parameters ||
|---|---|
| `elements` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: An array of `18` elements |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the count of `elements` is not `18` |
| `java.lang.NullPointerException` | if `elements` is `null` |

## Public methods

### copyElements

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun copyElements(
    destination: Array<Rational!>!, 
    offset: Int
): Unit
```

Copy the `https://developer.android.com/reference/kotlin/android/util/Rational.html#` elements in row-major order from this matrix into the destination.

| Parameters ||
|---|---|
| `destination` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Rational](https://developer.android.com/reference/kotlin/android/util/Rational.html#)!\>!: an array big enough to hold at least `9` elements after the `offset` |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a non-negative offset into the array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | If there's not enough room to write the elements at the specified destination and offset. |
| `java.lang.NullPointerException` | If `destination` was `null` |

### copyElements

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun copyElements(
    destination: IntArray!, 
    offset: Int
): Unit
```

Copy the `https://developer.android.com/reference/kotlin/android/util/Rational.html#` elements in row-major order from this matrix into the destination.

Each element is stored as a contiguous rational packed as a `(numerator, denominator)` pair of ints, identical to the `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#ColorSpaceTransform(kotlin.IntArray)`.

| Parameters ||
|---|---|
| `destination` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: an array big enough to hold at least `18` elements after the `offset` |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a non-negative offset into the array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | If there's not enough room to write the elements at the specified destination and offset. |
| `java.lang.NullPointerException` | If `destination` was `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#ColorSpaceTransform(kotlin.IntArray)`

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Check if this `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#` is equal to another `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform#`.

Two color space transforms are equal if and only if all of their elements are `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)`.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the objects were equal, `false` otherwise |

### getElement

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getElement(
    column: Int, 
    row: Int
): Rational!
```

Get an element of this matrix by its row and column.

The rows must be within the range \[0, 3), and the column must be within the range \[0, 3).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Rational.html#!` | element (non-`null`) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if column or row was out of range |

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

Return the color space transform as a string representation.

Example: `"ColorSpaceTransform([1/1, 0/1, 0/1], [0/1, 1/1, 0/1], [0/1, 0/1, 1/1])"` is an identity transform. Elements are printed in row major order.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | string representation of color space transform |
