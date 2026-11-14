Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Float

```
class Float : Number, Comparable<Float!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.lang.Float](https://developer.android.com/reference/kotlin/java/lang/Float#) |

The `Float` class wraps a value of primitive type in an object. An object of type `Float` contains a single field whose type is .

In addition, this class provides several methods for converting a `float` to a `String` and a `String` to a `float`, as well as other constants and methods useful when dealing with a `float`.

This is a [value-based](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/doc-files/ValueBased.html) class; programmers should treat instances that are [equal](https://developer.android.com/reference/kotlin/java/lang/Float#equals(kotlin.Any)) as interchangeable and should not use instances for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail.

## Floating-point Equality, Equivalence, and Comparison

The class `java.lang.Double` has a [discussion of equality, equivalence, and comparison of floating-point values](https://developer.android.com/reference/kotlin/java/lang/Double#equivalenceRelation) that is equally applicable to `float` values.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#BYTES:kotlin.Int` The number of bytes used to represent a `float` value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#MAX_EXPONENT:kotlin.Int` Maximum exponent a finite `float` variable may have. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#MAX_VALUE:kotlin.Float` A constant holding the largest positive finite value of type `float`, (2-2-23)·2127. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#MIN_EXPONENT:kotlin.Int` Minimum exponent a normalized `float` variable may have. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#MIN_NORMAL:kotlin.Float` A constant holding the smallest positive normal value of type `float`, 2-126. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#MIN_VALUE:kotlin.Float` A constant holding the smallest positive nonzero value of type `float`, 2-149. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#NEGATIVE_INFINITY:kotlin.Float` A constant holding the negative infinity of type `float`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#NaN:kotlin.Float` A constant holding a Not-a-Number (NaN) value of type `float`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#POSITIVE_INFINITY:kotlin.Float` A constant holding the positive infinity of type `float`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#PRECISION:kotlin.Int` The number of bits in the significand of a `float` value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#SIZE:kotlin.Int` The number of bits used to represent a `float` value. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Float#Float(kotlin.Double)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Constructs a newly allocated `Float` object that represents the argument converted to type `float`. |
| `https://developer.android.com/reference/kotlin/java/lang/Float#Float(kotlin.Float)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Constructs a newly allocated `Float` object that represents the primitive `float` argument. |
| `https://developer.android.com/reference/kotlin/java/lang/Float#Float(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Constructs a newly allocated `Float` object that represents the floating-point value of type `float` represented by the string. |

| Public methods ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#compare(kotlin.Float,%20kotlin.Float)(f1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, f2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Compares the two specified `float` values. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#compareTo(kotlin.Float)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Compares two `Float` objects numerically. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares this object against the specified object. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#float16ToFloat(kotlin.Short)(floatBinary16: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` {@return the {@code float} value closest to the numerical value \* of the argument, a floating-point binary16 value encoded in a \* {@code short}} The conversion is exact; all binary16 values can be exactly represented in `float`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#floatToFloat16(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` {@return the floating-point binary16 value, encoded in a {@code \* short}, closest in value to the argument} The conversion is computed under the [round to nearest even rounding](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#floatToIntBits(kotlin.Float)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns a representation of the specified floating-point value according to the IEEE 754 floating-point "single format" bit layout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#floatToRawIntBits(kotlin.Float)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns a representation of the specified floating-point value according to the IEEE 754 floating-point "single format" bit layout, preserving Not-a-Number (NaN) values. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#hashCode()()` Returns a hash code for this `Float` object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#hashCode(kotlin.Float)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns a hash code for a `float` value; compatible with `Float.hashCode()`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#intBitsToFloat(kotlin.Int)(bits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the `float` value corresponding to a given bit representation. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#isFinite(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns `true` if the argument is a finite floating-point value; returns `false` otherwise (for NaN and infinity arguments). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#isInfinite()()` Returns `true` if this `Float` value is infinitely large in magnitude, `false` otherwise. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#isInfinite(kotlin.Float)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns `true` if the specified number is infinitely large in magnitude, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#isNaN()()` Returns `true` if this `Float` value is a Not-a-Number (NaN), `false` otherwise. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#isNaN(kotlin.Float)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns `true` if the specified number is a Not-a-Number (NaN) value, `false` otherwise. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#max(kotlin.Float,%20kotlin.Float)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the greater of two `float` values as if by calling `https://developer.android.com/reference/kotlin/java/lang/Math#max(kotlin.Float,%20kotlin.Float)`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#min(kotlin.Float,%20kotlin.Float)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the smaller of two `float` values as if by calling `https://developer.android.com/reference/kotlin/java/lang/Math#min(kotlin.Float,%20kotlin.Float)`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#parseFloat(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns a new `float` initialized to the value represented by the specified `String`, as performed by the `valueOf` method of class `Float`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#sum(kotlin.Float,%20kotlin.Float)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Adds two `float` values together as per the + operator. |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#toByte()()` Returns the value of this `Float` as a `byte` after a narrowing primitive conversion. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#toDouble()()` Returns the value of this `Float` as a `double` after a widening primitive conversion. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#toFloat()()` Returns the `float` value of this `Float` object. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#toHexString(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns a hexadecimal string representation of the `float` argument. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#toInt()()` Returns the value of this `Float` as an `int` after a narrowing primitive conversion. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#toLong()()` Returns value of this `Float` as a `long` after a narrowing primitive conversion. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#toShort()()` Returns the value of this `Float` as a `short` after a narrowing primitive conversion. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#toString()()` Returns a string representation of this `Float` object. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#toString(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns a string representation of the `float` argument. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#valueOf(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns a `Float` instance representing the specified `float` value. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Float#valueOf(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns a object holding the value represented by the argument string . |

| Properties ||
|---|---|
| static [Class](https://developer.android.com/reference/kotlin/java/lang/Class)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/lang/Float#TYPE:java.lang.Class` The `Class` instance representing the primitive type `float`. |

## Constants

### BYTES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BYTES: Int
```

The number of bytes used to represent a `float` value.

 Value: 4

### MAX_EXPONENT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_EXPONENT: Int
```

Maximum exponent a finite `float` variable may have. It is equal to the value returned by `Math.getExponent(Float.MAX_VALUE)`.

 Value: 127

### MAX_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_VALUE: Float
```

A constant holding the largest positive finite value of type `float`, (2-2-23)·2127. It is equal to the hexadecimal floating-point literal `0x1.fffffeP+127f` and also equal to `Float.intBitsToFloat(0x7f7fffff)`.

 Value: 3.4028235E38f

### MIN_EXPONENT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_EXPONENT: Int
```

Minimum exponent a normalized `float` variable may have. It is equal to the value returned by `Math.getExponent(Float.MIN_NORMAL)`.

 Value: -126

### MIN_NORMAL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_NORMAL: Float
```

A constant holding the smallest positive normal value of type `float`, 2-126. It is equal to the hexadecimal floating-point literal `0x1.0p-126f` and also equal to `Float.intBitsToFloat(0x00800000)`.

 Value: 1.1754944E-38f

### MIN_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_VALUE: Float
```

A constant holding the smallest positive nonzero value of type `float`, 2-149. It is equal to the hexadecimal floating-point literal `0x0.000002P-126f` and also equal to `Float.intBitsToFloat(0x1)`.

 Value: 1.4E-45f

### NEGATIVE_INFINITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NEGATIVE_INFINITY: Float
```

A constant holding the negative infinity of type `float`. It is equal to the value returned by `Float.intBitsToFloat(0xff800000)`.

 Value: (-1.0f/0.0f)

### NaN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NaN: Float
```

A constant holding a Not-a-Number (NaN) value of type `float`. It is equivalent to the value returned by `Float.intBitsToFloat(0x7fc00000)`.

 Value: (0.0f/0.0f)

### POSITIVE_INFINITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POSITIVE_INFINITY: Float
```

A constant holding the positive infinity of type `float`. It is equal to the value returned by `Float.intBitsToFloat(0x7f800000)`.

 Value: (1.0f/0.0f)

### PRECISION

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRECISION: Int
```

The number of bits in the significand of a `float` value. This is the parameter N in section {@jls 4.2.3} of The Java Language Specification.

 Value: 24

### SIZE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIZE: Int
```

The number of bits used to represent a `float` value.

 Value: 32

## Public constructors

### Float

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Float(value: Double)
```

**Deprecated:** *It is rarely appropriate to use this constructor. Instead, use the static factory method `https://developer.android.com/reference/kotlin/java/lang/Float#valueOf(kotlin.Float)` method as follows: `Float.valueOf((float)value)`.*

Constructs a newly allocated `Float` object that represents the argument converted to type `float`.

| Parameters ||
|---|---|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the value to be represented by the `Float`. |

### Float

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Float(value: Float)
```

**Deprecated:** *It is rarely appropriate to use this constructor. The static factory `https://developer.android.com/reference/kotlin/java/lang/Float#valueOf(kotlin.Float)` is generally a better choice, as it is likely to yield significantly better space and time performance.*

Constructs a newly allocated `Float` object that represents the primitive `float` argument.

| Parameters ||
|---|---|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the value to be represented by the `Float`. |

### Float

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Float(s: String)
```

**Deprecated:** *It is rarely appropriate to use this constructor. Use `https://developer.android.com/reference/kotlin/java/lang/Float#parseFloat(kotlin.String)` to convert a string to a `float` primitive, or use `https://developer.android.com/reference/kotlin/java/lang/Float#valueOf(kotlin.String)` to convert a string to a `Float` object.*

Constructs a newly allocated `Float` object that represents the floating-point value of type `float` represented by the string. The string is converted to a `float` value as if by the `valueOf` method.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): a string to be converted to a `Float`. |

| Exceptions ||
|---|---|
| `java.lang.NumberFormatException` | if the string does not contain a parsable number. |

## Public methods

### compare

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    f1: Float, 
    f2: Float
): Int
```

Compares the two specified `float` values. The sign of the integer value returned is the same as that of the integer that would be returned by the call:

```kotlin
Float.valueOf(f1).compareTo(Float.valueOf(f2))
  
```

<br />

| Parameters ||
|---|---|
| `f1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the first `float` to compare. |
| `f2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the second `float` to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if `f1` is numerically equal to `f2`; a value less than `0` if `f1` is numerically less than `f2`; and a value greater than `0` if `f1` is numerically greater than `f2`. |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: Float): Int
```

Compares two `Float` objects numerically. This method imposes a total order on `Float` objects with two differences compared to the incomplete order defined by the Java language numerical comparison operators (`<, <=, ==, >=, >`) on `float` values.

- A NaN is *unordered* with respect to other values and unequal to itself under the comparison operators. This method chooses to define `Float.NaN` to be equal to itself and greater than all other `double` values (including `Float.POSITIVE_INFINITY`).
- Positive zero and negative zero compare equal numerically, but are distinct and distinguishable values. This method chooses to define positive zero (`+0.0f`), to be greater than negative zero (`-0.0f`).

This ensures that the *natural ordering* of `Float` objects imposed by this method is *consistent with equals* ; see [this discussion](https://developer.android.com/reference/kotlin/java/lang/Double#equivalenceRelation) for details of floating-point comparison and ordering.

<br />

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `anotherFloat` | the `Float` to be compared. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if `anotherFloat` is numerically equal to this `Float`; a value less than `0` if this `Float` is numerically less than `anotherFloat`; and a value greater than `0` if this `Float` is numerically greater than `anotherFloat`. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Compares this object against the specified object. The result is `true` if and only if the argument is not `null` and is a `Float` object that represents a `float` with the same value as the `float` represented by this object. For this purpose, two `float` values are considered to be the same if and only if the method `https://developer.android.com/reference/kotlin/java/lang/Float#floatToIntBits(kotlin.Float)` returns the identical `int` value when applied to each.

| Parameters ||
|---|---|
| `obj` | the object to be compared |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the objects are the same; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Float#floatToIntBits(kotlin.Float)`

### float16ToFloat

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun float16ToFloat(floatBinary16: Short): Float
```

{@return the {@code float} value closest to the numerical value \* of the argument, a floating-point binary16 value encoded in a \* {@code short}} The conversion is exact; all binary16 values can be exactly represented in `float`. Special cases:

- If the argument is zero, the result is a zero with the same sign as the argument.
- If the argument is infinite, the result is an infinity with the same sign as the argument.
- If the argument is a NaN, the result is a NaN.

#### IEEE 754 binary16 format

The IEEE 754 standard defines binary16 as a 16-bit format, along with the 32-bit binary32 format (corresponding to the `float` type) and the 64-bit binary64 format (corresponding to the `double` type). The binary16 format is similar to the other IEEE 754 formats, except smaller, having all the usual IEEE 754 values such as NaN, signed infinities, signed zeros, and subnormals. The parameters (JLS {@jls 4.2.3}) for the binary16 format are N = 11 precision bits, K = 5 exponent bits, *E* *max* = 15, and *E* *min* = -14.

<br />

| Parameters ||
|---|---|
| `floatBinary16` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): the binary16 value to convert to `float` |

### floatToFloat16

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun floatToFloat16(f: Float): Short
```

{@return the floating-point binary16 value, encoded in a {@code \* short}, closest in value to the argument} The conversion is computed under the [round to nearest even rounding](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#). Special cases:

- If the argument is zero, the result is a zero with the same sign as the argument.
- If the argument is infinite, the result is an infinity with the same sign as the argument.
- If the argument is a NaN, the result is a NaN.

The [binary16 format](https://developer.android.com/reference/kotlin/java/lang/Float#binary16Format) is discussed in more detail in the `https://developer.android.com/reference/kotlin/java/lang/Float#float16ToFloat(kotlin.Short)` method.

<br />

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the `float` value to convert to binary16 |

### floatToIntBits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun floatToIntBits(value: Float): Int
```

Returns a representation of the specified floating-point value according to the IEEE 754 floating-point "single format" bit layout.

Bit 31 (the bit that is selected by the mask `0x80000000`) represents the sign of the floating-point number. Bits 30-23 (the bits that are selected by the mask `0x7f800000`) represent the exponent. Bits 22-0 (the bits that are selected by the mask `0x007fffff`) represent the significand (sometimes called the mantissa) of the floating-point number.

If the argument is positive infinity, the result is `0x7f800000`.

If the argument is negative infinity, the result is `0xff800000`.

If the argument is NaN, the result is `0x7fc00000`.

In all cases, the result is an integer that, when given to the `https://developer.android.com/reference/kotlin/java/lang/Float#intBitsToFloat(kotlin.Int)` method, will produce a floating-point value the same as the argument to `floatToIntBits` (except all NaN values are collapsed to a single "canonical" NaN value).

| Parameters ||
|---|---|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a floating-point number. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the bits that represent the floating-point number. |

### floatToRawIntBits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun floatToRawIntBits(value: Float): Int
```

Returns a representation of the specified floating-point value according to the IEEE 754 floating-point "single format" bit layout, preserving Not-a-Number (NaN) values.

Bit 31 (the bit that is selected by the mask `0x80000000`) represents the sign of the floating-point number. Bits 30-23 (the bits that are selected by the mask `0x7f800000`) represent the exponent. Bits 22-0 (the bits that are selected by the mask `0x007fffff`) represent the significand (sometimes called the mantissa) of the floating-point number.

If the argument is positive infinity, the result is `0x7f800000`.

If the argument is negative infinity, the result is `0xff800000`.

If the argument is NaN, the result is the integer representing the actual NaN value. Unlike the `floatToIntBits` method, `floatToRawIntBits` does not collapse all the bit patterns encoding a NaN to a single "canonical" NaN value.

In all cases, the result is an integer that, when given to the `https://developer.android.com/reference/kotlin/java/lang/Float#intBitsToFloat(kotlin.Int)` method, will produce a floating-point value the same as the argument to `floatToRawIntBits`.

| Parameters ||
|---|---|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a floating-point number. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the bits that represent the floating-point number. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code for this `Float` object. The result is the integer bit representation, exactly as produced by the method `https://developer.android.com/reference/kotlin/java/lang/Float#floatToIntBits(kotlin.Float)`, of the primitive `float` value represented by this `Float` object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hashCode(value: Float): Int
```

Returns a hash code for a `float` value; compatible with `Float.hashCode()`.

| Parameters ||
|---|---|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the value to hash |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for a `float` value. |

### intBitsToFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun intBitsToFloat(bits: Int): Float
```

Returns the `float` value corresponding to a given bit representation. The argument is considered to be a representation of a floating-point value according to the IEEE 754 floating-point "single format" bit layout.

If the argument is `0x7f800000`, the result is positive infinity.

If the argument is `0xff800000`, the result is negative infinity.

If the argument is any value in the range `0x7f800001` through `0x7fffffff` or in the range `0xff800001` through `0xffffffff`, the result is a NaN. No IEEE 754 floating-point operation provided by Java can distinguish between two NaN values of the same type with different bit patterns. Distinct values of NaN are only distinguishable by use of the `Float.floatToRawIntBits` method.

In all other cases, let *s* , *e* , and *m* be three values that can be computed from the argument: {@snippet lang="java" : \* int s = ((bits \>\> 31) == 0) ? 1 : -1; \* int e = ((bits \>\> 23) \& 0xff); \* int m = (e == 0) ? \* (bits \& 0x7fffff) \<\< 1 : \* (bits \& 0x7fffff) | 0x800000; \* } Then the floating-point result equals the value of the mathematical expression *s* ·*m* ·2*e*-150.

Note that this method may not be able to return a `float` NaN with exactly same bit pattern as the `int` argument. IEEE 754 distinguishes between two kinds of NaNs, quiet NaNs and *signaling NaNs* . The differences between the two kinds of NaN are generally not visible in Java. Arithmetic operations on signaling NaNs turn them into quiet NaNs with a different, but often similar, bit pattern. However, on some processors merely copying a signaling NaN also performs that conversion. In particular, copying a signaling NaN to return it to the calling method may perform this conversion. So `intBitsToFloat` may not be able to return a `float` with a signaling NaN bit pattern. Consequently, for some `int` values, `floatToRawIntBits(intBitsToFloat(start))` may *not* equal `start`. Moreover, which particular bit patterns represent signaling NaNs is platform dependent; although all NaN bit patterns, quiet or signaling, must be in the NaN range identified above.

| Parameters ||
|---|---|
| `bits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an integer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the `float` floating-point value with the same bit pattern. |

### isFinite

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isFinite(f: Float): Boolean
```

Returns `true` if the argument is a finite floating-point value; returns `false` otherwise (for NaN and infinity arguments).

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the `float` value to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the argument is a finite floating-point value, `false` otherwise. |

### isInfinite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isInfinite(): Boolean
```

Returns `true` if this `Float` value is infinitely large in magnitude, `false` otherwise.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the value represented by this object is positive infinity or negative infinity; `false` otherwise. |

### isInfinite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isInfinite(v: Float): Boolean
```

Returns `true` if the specified number is infinitely large in magnitude, `false` otherwise.

| Parameters ||
|---|---|
| `v` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the value to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the argument is positive infinity or negative infinity; `false` otherwise. |

### isNaN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isNaN(): Boolean
```

Returns `true` if this `Float` value is a Not-a-Number (NaN), `false` otherwise.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the value represented by this object is NaN; `false` otherwise. |

### isNaN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isNaN(v: Float): Boolean
```

Returns `true` if the specified number is a Not-a-Number (NaN) value, `false` otherwise.

| Parameters ||
|---|---|
| `v` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the value to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the argument is NaN; `false` otherwise. |

### max

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun max(
    a: Float, 
    b: Float
): Float
```

Returns the greater of two `float` values as if by calling `https://developer.android.com/reference/kotlin/java/lang/Math#max(kotlin.Float,%20kotlin.Float)`.

| Parameters ||
|---|---|
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the first operand |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the second operand |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the greater of `a` and `b` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#`

### min

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun min(
    a: Float, 
    b: Float
): Float
```

Returns the smaller of two `float` values as if by calling `https://developer.android.com/reference/kotlin/java/lang/Math#min(kotlin.Float,%20kotlin.Float)`.

| Parameters ||
|---|---|
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the first operand |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the second operand |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the smaller of `a` and `b` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#`

### parseFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parseFloat(s: String): Float
```

Returns a new `float` initialized to the value represented by the specified `String`, as performed by the `valueOf` method of class `Float`.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the string to be parsed. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the `float` value represented by the string argument. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the string is null |
| `java.lang.NumberFormatException` | if the string does not contain a parsable `float`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Float#valueOf(kotlin.String)`

### sum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sum(
    a: Float, 
    b: Float
): Float
```

Adds two `float` values together as per the + operator.

| Parameters ||
|---|---|
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the first operand |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the second operand |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the sum of `a` and `b` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#`

### toByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toByte(): Byte
```

Returns the value of this `Float` as a `byte` after a narrowing primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | the `float` value represented by this object converted to type `byte` |

### toDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toDouble(): Double
```

Returns the value of this `Float` as a `double` after a widening primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the `float` value represented by this object converted to type `double` |

### toFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toFloat(): Float
```

Returns the `float` value of this `Float` object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the `float` value represented by this object |

### toHexString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toHexString(f: Float): String
```

Returns a hexadecimal string representation of the `float` argument. All characters mentioned below are ASCII characters.

- If the argument is NaN, the result is the string "`NaN`".
- Otherwise, the result is a string that represents the sign and magnitude (absolute value) of the argument. If the sign is negative, the first character of the result is '`-`' (`'\u005Cu002D'`); if the sign is positive, no sign character appears in the result. As for the magnitude *m* :
 - If *m* is infinity, it is represented by the string `"Infinity"`; thus, positive infinity produces the result `"Infinity"` and negative infinity produces the result `"-Infinity"`.
 - If *m* is zero, it is represented by the string `"0x0.0p0"`; thus, negative zero produces the result `"-0x0.0p0"` and positive zero produces the result `"0x0.0p0"`.
 - If *m* is a `float` value with a normalized representation, substrings are used to represent the significand and exponent fields. The significand is represented by the characters `"0x1."` followed by a lowercase hexadecimal representation of the rest of the significand as a fraction. Trailing zeros in the hexadecimal representation are removed unless all the digits are zero, in which case a single zero is used. Next, the exponent is represented by `"p"` followed by a decimal string of the unbiased exponent as if produced by a call to `https://developer.android.com/reference/kotlin/java/lang/Integer#toString(kotlin.Int)` on the exponent value.
 - If *m* is a `float` value with a subnormal representation, the significand is represented by the characters `"0x0."` followed by a hexadecimal representation of the rest of the significand as a fraction. Trailing zeros in the hexadecimal representation are removed. Next, the exponent is represented by `"p-126"`. Note that there must be at least one nonzero digit in a subnormal significand.

| Floating-point Value | Hexadecimal String |
| `1.0` | `0x1.0p0` |
| `-1.0` | `-0x1.0p0` |
| `2.0` | `0x1.0p1` |
| `3.0` | `0x1.8p1` |
| `0.5` | `0x1.0p-1` |
| `0.25` | `0x1.0p-2` |
| `Float.MAX_VALUE` | `0x1.fffffep127` |
| `Minimum Normal Value` | `0x1.0p-126` |
| `Maximum Subnormal Value` | `0x0.fffffep-126` |
| `Float.MIN_VALUE` | `0x0.000002p-126` |
|---|---|

<br />

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the `float` to be converted. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a hex string representation of the argument. |

### toInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toInt(): Int
```

Returns the value of this `Float` as an `int` after a narrowing primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the `float` value represented by this object converted to type `int` |

### toLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toLong(): Long
```

Returns value of this `Float` as a `long` after a narrowing primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the `float` value represented by this object converted to type `long` |

### toShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toShort(): Short
```

Returns the value of this `Float` as a `short` after a narrowing primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | the `float` value represented by this object converted to type `short` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of this `Float` object. The primitive `float` value represented by this object is converted to a `String` exactly as if by the method `toString` of one argument.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a `String` representation of this object. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Float#toString(kotlin.Float)`

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(f: Float): String
```

Returns a string representation of the `float` argument. All characters mentioned below are ASCII characters.

- If the argument is NaN, the result is the string "`NaN`".
- Otherwise, the result is a string that represents the sign and magnitude (absolute value) of the argument. If the sign is negative, the first character of the result is '`-`' (`'\u005Cu002D'`); if the sign is positive, no sign character appears in the result. As for the magnitude *m* :
 - If *m* is infinity, it is represented by the characters `"Infinity"`; thus, positive infinity produces the result `"Infinity"` and negative infinity produces the result `"-Infinity"`.
 - If *m* is zero, it is represented by the characters `"0.0"`; thus, negative zero produces the result `"-0.0"` and positive zero produces the result `"0.0"`.
 - Otherwise *m* is positive and finite. It is converted to a string in two stages:
 - *Selection of a decimal* : A well-defined decimal *d* *m* is selected to represent *m* . This decimal is (almost always) the *shortest* one that rounds to *m* according to the round to nearest rounding policy of IEEE 754 floating-point arithmetic.
 - *Formatting as a string* : The decimal *d* *m* is formatted as a string, either in plain or in computerized scientific notation, depending on its value.

<br />

A *decimal* is a number of the form *s* ×10*i* for some (unique) integers *s* \> 0 and *i* such that *s* is not a multiple of 10. These integers are the *significand* and the *exponent* , respectively, of the decimal. The *length* of the decimal is the (unique) positive integer *n* meeting 10*n* -1 ≤ *s* \< 10*n*.

The decimal *d* *m* for a finite positive *m* is defined as follows:

- Let *R* be the set of all decimals that round to *m* according to the usual *round to nearest* rounding policy of IEEE 754 floating-point arithmetic.
- Let *p* be the minimal length over all decimals in *R*.
- When *p* ≥ 2, let *T* be the set of all decimals in *R* with length *p* . Otherwise, let *T* be the set of all decimals in *R* with length 1 or 2.
- Define *d* *m* as the decimal in *T* that is closest to *m* . Or if there are two such decimals in *T*, select the one with the even significand.

The (uniquely) selected decimal *d* *m* is then formatted. Let *s* , *i* and *n* be the significand, exponent and length of *d* *m* , respectively. Further, let *e* = *n* + *i* - 1 and let *s* 1...*s* *n* be the usual decimal expansion of *s* . Note that *s* 1 ≠ 0 and *s* *n* ≠ 0. Below, the decimal point `'.'` is `'\u005Cu002E'` and the exponent indicator `'E'` is `'\u005Cu0045'`.

- Case -3 ≤ *e* \< 0: *d* *m* is formatted as `0.0`...`0`*s* 1...*s* *n* , where there are exactly -(*n* + *i* ) zeroes between the decimal point and *s* 1. For example, 123 × 10-4 is formatted as `0.0123`.
- Case 0 ≤ *e* \< 7:
 - Subcase *i* ≥ 0: *d* *m* is formatted as *s* 1...*s* *n* `0`...`0.0`, where there are exactly *i* zeroes between *s* *n* and the decimal point. For example, 123 × 102 is formatted as `12300.0`.
 - Subcase *i* \< 0: *d* *m* is formatted as *s* 1...*s* *n* +*i* `.`*s* *n* +*i* +1...*s* *n* , where there are exactly -*i* digits to the right of the decimal point. For example, 123 × 10-1 is formatted as `12.3`.
- Case *e* \< -3 or *e* ≥ 7: computerized scientific notation is used to format *d* *m* . Here *e* is formatted as by `https://developer.android.com/reference/kotlin/java/lang/Integer#toString(kotlin.Int)`.
 - Subcase *n* = 1: *d* *m* is formatted as *s* 1`.0E`*e* . For example, 1 × 1023 is formatted as `1.0E23`.
 - Subcase *n* \> 1: *d* *m* is formatted as *s* 1`.`*s* 2...*s* *n* `E`*e* . For example, 123 × 10-21 is formatted as `1.23E-19`.

To create localized string representations of a floating-point value, use subclasses of `https://developer.android.com/reference/kotlin/java/text/NumberFormat.html#`.

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the `float` to be converted. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the argument. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(f: Float): Float
```

Returns a `Float` instance representing the specified `float` value. If a new `Float` instance is not required, this method should generally be used in preference to the constructor `https://developer.android.com/reference/kotlin/java/lang/Float#Float(kotlin.Float)`, as this method is likely to yield significantly better space and time performance by caching frequently requested values.

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a float value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | a `Float` instance representing `f`. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(s: String): Float
```

Returns a object holding the value represented by the argument string .

If `s` is `null`, then a `NullPointerException` is thrown.

Leading and trailing whitespace characters in `s` are ignored. Whitespace is removed as if by the `https://developer.android.com/reference/kotlin/java/lang/String#trim()` method; that is, both ASCII space and control characters are removed. The rest of `s` should constitute a *FloatValue* as described by the lexical syntax rules:

*FloatValue:*
: *Signopt* `NaN`
: *Signopt* `Infinity`
: *Signopt FloatingPointLiteral*
: *Signopt HexFloatingPointLiteral*
: *SignedInteger*

*HexFloatingPointLiteral*:
: *HexSignificand BinaryExponent FloatTypeSuffixopt*

*HexSignificand:*
: *HexNumeral*
: *HexNumeral* `.`
: `0x` *HexDigitsopt* `.`*HexDigits*
: `0X`*HexDigitsopt* `.` *HexDigits*

*BinaryExponent:*
: *BinaryExponentIndicator SignedInteger*

*BinaryExponentIndicator:*
: `p`
: `P`
where *Sign* , *FloatingPointLiteral* , *HexNumeral* , *HexDigits* , *SignedInteger* and *FloatTypeSuffix* are as defined in the lexical structure sections of The Java Language Specification, except that underscores are not accepted between digits. If `s` does not have the form of a *FloatValue* , then a `NumberFormatException` is thrown. Otherwise, `s` is regarded as representing an exact decimal value in the usual "computerized scientific notation" or as an exact hexadecimal value; this exact numerical value is then conceptually converted to an "infinitely precise" binary value that is then rounded to type `float` by the usual round-to-nearest rule of IEEE 754 floating-point arithmetic, which includes preserving the sign of a zero value. Note that the round-to-nearest rule also implies overflow and underflow behaviour; if the exact value of `s` is large enough in magnitude (greater than or equal to (`https://developer.android.com/reference/kotlin/java/lang/Float#MAX_VALUE:kotlin.Float` + `https://developer.android.com/reference/kotlin/java/lang/Math#ulp(kotlin.Float)`/2), rounding to `float` will result in an infinity and if the exact value of `s` is small enough in magnitude (less than or equal to `https://developer.android.com/reference/kotlin/java/lang/Float#MIN_VALUE:kotlin.Float`/2), rounding to float will result in a zero. Finally, after rounding a `Float` object representing this `float` value is returned.

To interpret localized string representations of a floating-point value, use subclasses of `https://developer.android.com/reference/kotlin/java/text/NumberFormat.html#`.

Note that trailing format specifiers, specifiers that determine the type of a floating-point literal (`1.0f` is a `float` value; `1.0d` is a `double` value), do *not* influence the results of this method. In other words, the numerical value of the input string is converted directly to the target floating-point type. In general, the two-step sequence of conversions, string to `double` followed by `double` to `float`, is *not* equivalent to converting a string directly to `float`. For example, if first converted to an intermediate `double` and then to `float`, the string 
`"1.00000017881393421514957253748434595763683319091796875001d"` 
results in the `float` value `1.0000002f`; if the string is converted directly to `float`, `1.0000001f` results.

To avoid calling this method on an invalid string and having a `NumberFormatException` be thrown, the documentation for java.lang.Double#valueOf lists a regular expression which can be used to screen the input.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the string to be parsed. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | a `Float` object holding the value represented by the `String` argument. |

| Exceptions ||
|---|---|
| `java.lang.NumberFormatException` | if the string does not contain a parsable number. |

## Properties

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE: Class<Float!>!
```

The `Class` instance representing the primitive type `float`.
