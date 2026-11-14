Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Half

Kotlin | [Java](Half.md)
| --- | --- |

```
class Half : Number, Comparable<Half!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [android.util.Half](Half.md) |

The `Half` class is a wrapper and a utility class to manipulate half-precision 16-bit [IEEE 754](https://en.wikipedia.org/wiki/Half-precision_floating-point_format) floating point data types (also called fp16 or binary16). A half-precision float can be created from or converted to single-precision floats, and is stored in a short data type. To distinguish short values holding half-precision floats from regular short values, it is recommended to use the `@HalfFloat` annotation.

The IEEE 754 standard specifies an fp16 as having the following format:

- Sign bit: 1 bit
- Exponent width: 5 bits
- Significand: 10 bits

The format is laid out as follows:

```kotlin
1   11111   1111111111
  ^   --^--   ---^---
  sign  |          |_______ significand
        |
        -- exponent
  
```

Half-precision floating points can be useful to save memory and/or bandwidth at the expense of range and precision when compared to single-precision floating points (fp32).

To help you decide whether fp16 is the right storage type for you need, please refer to the table below that shows the available precision throughout the range of possible values. The *precision* column indicates the step size between two consecutive numbers in a specific part of the range.

| Range start | Precision |
|---|---|
| 0 | 1 ⁄ 16,777,216 |
| 1 ⁄ 16,384 | 1 ⁄ 16,777,216 |
| 1 ⁄ 8,192 | 1 ⁄ 8,388,608 |
| --- | --- |
| 1 ⁄ 4,096 | 1 ⁄ 4,194,304 |
| 1 ⁄ 2,048 | 1 ⁄ 2,097,152 |
| 1 ⁄ 1,024 | 1 ⁄ 1,048,576 |
| --- | --- |
| 1 ⁄ 512 | 1 ⁄ 524,288 |
| 1 ⁄ 256 | 1 ⁄ 262,144 |
| 1 ⁄ 128 | 1 ⁄ 131,072 |
| --- | --- |
| 1 ⁄ 64 | 1 ⁄ 65,536 |
| 1 ⁄ 32 | 1 ⁄ 32,768 |
| 1 ⁄ 16 | 1 ⁄ 16,384 |
| --- | --- |
| 1 ⁄ 8 | 1 ⁄ 8,192 |
| 1 ⁄ 4 | 1 ⁄ 4,096 |
| 1 ⁄ 2 | 1 ⁄ 2,048 |
| --- | --- |
| 1 | 1 ⁄ 1,024 |
| 2 | 1 ⁄ 512 |
| 4 | 1 ⁄ 256 |
| --- | --- |
| 8 | 1 ⁄ 128 |
| 16 | 1 ⁄ 64 |
| 32 | 1 ⁄ 32 |
| --- | --- |
| 64 | 1 ⁄ 16 |
| 128 | 1 ⁄ 8 |
| 256 | 1 ⁄ 4 |
| --- | --- |
| 512 | 1 ⁄ 2 |
| 1,024 | 1 |
| 2,048 | 2 |
| --- | --- |
| 4,096 | 4 |
| 8,192 | 8 |
| 16,384 | 16 |
| --- | --- |
| 32,768 | 32 |

This table shows that numbers higher than 1024 lose all fractional precision.

## Summary

| Constants ||
|---|---|
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#EPSILON:kotlin.Short` Epsilon is the difference between 1. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#LOWEST_VALUE:kotlin.Short` Smallest negative value a half-precision float may have. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#MAX_EXPONENT:kotlin.Int` Maximum exponent a finite half-precision float may have. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#MAX_VALUE:kotlin.Short` Maximum positive finite value a half-precision float may have. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#MIN_EXPONENT:kotlin.Int` Minimum exponent a normalized half-precision float may have. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#MIN_NORMAL:kotlin.Short` Smallest positive normal value a half-precision float may have. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#MIN_VALUE:kotlin.Short` Smallest positive non-zero value a half-precision float may have. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#NEGATIVE_INFINITY:kotlin.Short` Negative infinity of type half-precision float. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#NEGATIVE_ZERO:kotlin.Short` Negative 0 of type half-precision float. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#NaN:kotlin.Short` A Not-a-Number representation of a half-precision float. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_INFINITY:kotlin.Short` Positive infinity of type half-precision float. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_ZERO:kotlin.Short` Positive 0 of type half-precision float. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#SIZE:kotlin.Int` The number of bits used to represent a half-precision float value. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Half#Half(kotlin.Double)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Constructs a newly allocated `Half` object that represents the argument converted to a half-precision float. |
| `https://developer.android.com/reference/kotlin/android/util/Half#Half(kotlin.Float)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Constructs a newly allocated `Half` object that represents the argument converted to a half-precision float. |
| `https://developer.android.com/reference/kotlin/android/util/Half#Half(kotlin.String)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Constructs a newly allocated `Half` object that represents the half-precision float value represented by the string. |
| `https://developer.android.com/reference/kotlin/android/util/Half#Half(kotlin.Short)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Constructs a newly allocated `Half` object that represents the half-precision float type argument. |

| Public methods ||
|---|---|
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#abs(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns the absolute value of the specified half-precision float. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#ceil(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns the smallest half-precision float value toward negative infinity greater than or equal to the specified half-precision float value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#compare(kotlin.Short,%20kotlin.Short)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Compares the two specified half-precision float values. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#compareTo(android.util.Half)(other: https://developer.android.com/reference/kotlin/android/util/Half#)` Compares the two specified half-precision float values. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#copySign(kotlin.Short,%20kotlin.Short)(magnitude: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html, sign: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns the first parameter with the sign of the second parameter. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares this object against the specified object. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#equals(kotlin.Short,%20kotlin.Short)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns true if the two half-precision float values are equal. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#floor(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns the largest half-precision float value toward positive infinity less than or equal to the specified half-precision float value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#getExponent(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns the unbiased exponent used in the representation of the specified half-precision float value. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#getSign(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns the sign of the specified half-precision float. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#getSignificand(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns the significand, or mantissa, used in the representation of the specified half-precision float value. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#greater(kotlin.Short,%20kotlin.Short)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns true if the first half-precision float value is greater (larger toward positive infinity) than the second half-precision float value. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#greaterEquals(kotlin.Short,%20kotlin.Short)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns true if the first half-precision float value is greater (larger toward positive infinity) than or equal to the second half-precision float value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#halfToIntBits(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns a representation of the specified half-precision float value according to the bit layout described in `https://developer.android.com/reference/kotlin/android/util/Half#`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#halfToRawIntBits(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns a representation of the specified half-precision float value according to the bit layout described in `https://developer.android.com/reference/kotlin/android/util/Half#`. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#halfToShortBits(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns a representation of the specified half-precision float value according to the bit layout described in `https://developer.android.com/reference/kotlin/android/util/Half#`. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#halfValue()()` Returns the half-precision value of this `Half` as a `short` containing the bit representation described in `https://developer.android.com/reference/kotlin/android/util/Half#`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#hashCode()()` Returns a hash code for this `Half` object. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#hashCode(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns a hash code for a half-precision float value. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#intBitsToHalf(kotlin.Int)(bits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the half-precision float value corresponding to a given bit representation. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#isInfinite(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns true if the specified half-precision float value represents infinity, false otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#isNaN()()` Returns true if this `Half` value represents a Not-a-Number, false otherwise. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#isNaN(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns true if the specified half-precision float value represents a Not-a-Number, false otherwise. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#isNormalized(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns true if the specified half-precision float value is normalized (does not have a subnormal representation). |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#less(kotlin.Short,%20kotlin.Short)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns true if the first half-precision float value is less (smaller toward negative infinity) than the second half-precision float value. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#lessEquals(kotlin.Short,%20kotlin.Short)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns true if the first half-precision float value is less (smaller toward negative infinity) than or equal to the second half-precision float value. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#max(kotlin.Short,%20kotlin.Short)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns the larger of two half-precision float values (the value closest to positive infinity). |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#min(kotlin.Short,%20kotlin.Short)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns the smaller of two half-precision float values (the value closest to negative infinity). |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#parseHalf(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the half-precision float value represented by the specified string. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#round(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns the closest integral half-precision float value to the specified half-precision float value. |
| --- | --- |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#toByte()()` Returns the value of this `Half` as a `byte` after a narrowing primitive conversion. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#toDouble()()` Returns the value of this `Half` as a `double` after a widening primitive conversion. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#toFloat()()` Returns the value of this `Half` as a `float` after a widening primitive conversion. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#toFloat(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Converts the specified half-precision float value into a single-precision float value. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#toHalf(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Converts the specified single-precision float value into a half-precision float value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#toHexString(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns a hexadecimal string representation of the specified half-precision float value. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#toInt()()` Returns the value of this `Half` as a `int` after a narrowing primitive conversion. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#toLong()()` Returns the value of this `Half` as a `long` after a narrowing primitive conversion. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#toShort()()` Returns the value of this `Half` as a `short` after a narrowing primitive conversion. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#toString()()` Returns a string representation of the specified half-precision float value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#toString(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns a string representation of the specified half-precision float value. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Half#trunc(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns the truncated half-precision float value of the specified half-precision float value. |
| --- | --- |
| static [Half](Half.md) | `https://developer.android.com/reference/kotlin/android/util/Half#valueOf(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns a `Half` instance representing the specified float value. |
| static [Half](Half.md) | `https://developer.android.com/reference/kotlin/android/util/Half#valueOf(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns a `Half` instance representing the specified string value. |
| static [Half](Half.md) | `https://developer.android.com/reference/kotlin/android/util/Half#valueOf(kotlin.Short)(h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns a `Half` instance representing the specified half-precision float value. |
| --- | --- |

## Constants

### EPSILON

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EPSILON: Short
```

Epsilon is the difference between 1.0 and the next value representable by a half-precision floating-point.

 Value: 5120

### LOWEST_VALUE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOWEST_VALUE: Short
```

Smallest negative value a half-precision float may have.

 Value: -1025

### MAX_EXPONENT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_EXPONENT: Int
```

Maximum exponent a finite half-precision float may have.

 Value: 15

### MAX_VALUE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_VALUE: Short
```

Maximum positive finite value a half-precision float may have.

 Value: 31743

### MIN_EXPONENT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_EXPONENT: Int
```

Minimum exponent a normalized half-precision float may have.

 Value: -14

### MIN_NORMAL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_NORMAL: Short
```

Smallest positive normal value a half-precision float may have.

 Value: 1024

### MIN_VALUE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_VALUE: Short
```

Smallest positive non-zero value a half-precision float may have.

 Value: 1

### NEGATIVE_INFINITY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NEGATIVE_INFINITY: Short
```

Negative infinity of type half-precision float.

 Value: -1024

### NEGATIVE_ZERO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NEGATIVE_ZERO: Short
```

Negative 0 of type half-precision float.

 Value: -32768

### NaN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NaN: Short
```

A Not-a-Number representation of a half-precision float.

 Value: 32256

### POSITIVE_INFINITY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POSITIVE_INFINITY: Short
```

Positive infinity of type half-precision float.

 Value: 31744

### POSITIVE_ZERO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POSITIVE_ZERO: Short
```

Positive 0 of type half-precision float.

 Value: 0

### SIZE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIZE: Int
```

The number of bits used to represent a half-precision float value.

 Value: 16

## Public constructors

### Half

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Half(value: Double)
```

Constructs a newly allocated `Half` object that represents the argument converted to a half-precision float.

| Parameters ||
|---|---|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The value to be represented by the `Half` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/util/Half#toHalf(kotlin.Float)`

### Half

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Half(value: Float)
```

Constructs a newly allocated `Half` object that represents the argument converted to a half-precision float.

| Parameters ||
|---|---|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The value to be represented by the `Half` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/util/Half#toHalf(kotlin.Float)`

### Half

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Half(value: String)
```

Constructs a newly allocated `Half` object that represents the half-precision float value represented by the string. The string is converted to a half-precision float value as if by the `https://developer.android.com/reference/kotlin/android/util/Half#valueOf(kotlin.String)` method.

Calling this constructor is equivalent to calling:

```kotlin
new Half(Float.parseFloat(value))
  
```

| Parameters ||
|---|---|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A string to be converted to a `Half` This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NumberFormatException` | if the string does not contain a parsable number |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Float.html#valueOf(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/util/Half#toHalf(kotlin.Float)`

### Half

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Half(value: Short)
```

Constructs a newly allocated `Half` object that represents the half-precision float type argument.

| Parameters ||
|---|---|
| `value` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The value to be represented by the `Half` |

## Public methods

### abs

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun abs(h: Short): Short
```

Returns the absolute value of the specified half-precision float. Special values are handled in the following ways:

- If the specified half-precision float is NaN, the result is NaN
- If the specified half-precision float is zero (negative or positive), the result is positive zero (see `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_ZERO:kotlin.Short`)
- If the specified half-precision float is infinity (negative or positive), the result is positive infinity (see `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_INFINITY:kotlin.Short`)

<br />

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | The absolute value of the specified half-precision float |

### ceil

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ceil(h: Short): Short
```

Returns the smallest half-precision float value toward negative infinity greater than or equal to the specified half-precision float value. Special values are handled in the following ways:

- If the specified half-precision float is NaN, the result is NaN
- If the specified half-precision float is infinity (negative or positive), the result is infinity (with the same sign)
- If the specified half-precision float is zero (negative or positive), the result is zero (with the same sign)

<br />

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | The smallest half-precision float value toward negative infinity greater than or equal to the specified half-precision float value |

### compare

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    x: Short, 
    y: Short
): Int
```

Compares the two specified half-precision float values. The following conditions apply during the comparison:

- `https://developer.android.com/reference/kotlin/android/util/Half#NaN:kotlin.Short` is considered by this method to be equal to itself and greater than all other half-precision float values (including `POSITIVE_INFINITY`)
- `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_ZERO:kotlin.Short` is considered by this method to be greater than `https://developer.android.com/reference/kotlin/android/util/Half#NEGATIVE_ZERO:kotlin.Short`.

| Parameters ||
|---|---|
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The first half-precision float value to compare. |
| `y` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The second half-precision float value to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The value `0` if `x` is numerically equal to `y`, a value less than `0` if `x` is numerically less than `y`, and a value greater than `0` if `x` is numerically greater than `y` |

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: Half): Int
```

Compares the two specified half-precision float values. The following conditions apply during the comparison:

- `https://developer.android.com/reference/kotlin/android/util/Half#NaN:kotlin.Short` is considered by this method to be equal to itself and greater than all other half-precision float values (including `POSITIVE_INFINITY`)
- `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_ZERO:kotlin.Short` is considered by this method to be greater than `https://developer.android.com/reference/kotlin/android/util/Half#NEGATIVE_ZERO:kotlin.Short`.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `h` | The half-precision float value to compare to the half-precision value represented by this `Half` object. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The value `0` if `x` is numerically equal to `y`; a value less than `0` if `x` is numerically less than `y`; and a value greater than `0` if `x` is numerically greater than `y` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### copySign

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copySign(
    magnitude: Short, 
    sign: Short
): Short
```

Returns the first parameter with the sign of the second parameter. This method treats NaNs as having a sign.

| Parameters ||
|---|---|
| `magnitude` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value providing the magnitude of the result |
| `sign` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value providing the sign of the result |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | A value with the magnitude of the first parameter and the sign of the second parameter |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Compares this object against the specified object. The result is `true` if and only if the argument is not `null` and is a `Half` object that represents the same half-precision value as the this object. Two half-precision values are considered to be the same if and only if the method `https://developer.android.com/reference/kotlin/android/util/Half#halfToIntBits(kotlin.Short)` returns an identical `int` value for both.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | The object to compare. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the objects are the same, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/util/Half#halfToIntBits(kotlin.Short)`

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    x: Short, 
    y: Short
): Boolean
```

Returns true if the two half-precision float values are equal. If either of the values is NaN, the result is false. `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_ZERO:kotlin.Short` and `https://developer.android.com/reference/kotlin/android/util/Half#NEGATIVE_ZERO:kotlin.Short` are considered equal.

| Parameters ||
|---|---|
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The first half-precision value |
| `y` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The second half-precision value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if x is equal to y, false otherwise |

### floor

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun floor(h: Short): Short
```

Returns the largest half-precision float value toward positive infinity less than or equal to the specified half-precision float value. Special values are handled in the following ways:

- If the specified half-precision float is NaN, the result is NaN
- If the specified half-precision float is infinity (negative or positive), the result is infinity (with the same sign)
- If the specified half-precision float is zero (negative or positive), the result is zero (with the same sign)

<br />

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | The largest half-precision float value toward positive infinity less than or equal to the specified half-precision float value |

### getExponent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getExponent(h: Short): Int
```

Returns the unbiased exponent used in the representation of the specified half-precision float value. if the value is NaN or infinite, this\* method returns `https://developer.android.com/reference/kotlin/android/util/Half#MAX_EXPONENT:kotlin.Int` + 1. If the argument is 0 or a subnormal representation, this method returns `https://developer.android.com/reference/kotlin/android/util/Half#MIN_EXPONENT:kotlin.Int` - 1.

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The unbiased exponent of the specified value |

### getSign

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getSign(h: Short): Int
```

Returns the sign of the specified half-precision float.

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | 1 if the value is positive, -1 if the value is negative |

### getSignificand

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getSignificand(h: Short): Int
```

Returns the significand, or mantissa, used in the representation of the specified half-precision float value.

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The significand, or significand, of the specified vlaue |

### greater

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun greater(
    x: Short, 
    y: Short
): Boolean
```

Returns true if the first half-precision float value is greater (larger toward positive infinity) than the second half-precision float value. If either of the values is NaN, the result is false.

| Parameters ||
|---|---|
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The first half-precision value |
| `y` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The second half-precision value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if x is greater than y, false otherwise |

### greaterEquals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun greaterEquals(
    x: Short, 
    y: Short
): Boolean
```

Returns true if the first half-precision float value is greater (larger toward positive infinity) than or equal to the second half-precision float value. If either of the values is NaN, the result is false.

| Parameters ||
|---|---|
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The first half-precision value |
| `y` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The second half-precision value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if x is greater than y, false otherwise |

### halfToIntBits

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun halfToIntBits(h: Short): Int
```

Returns a representation of the specified half-precision float value according to the bit layout described in `https://developer.android.com/reference/kotlin/android/util/Half#`.

Unlike `https://developer.android.com/reference/kotlin/android/util/Half#halfToRawIntBits(kotlin.Short)`, this method collapses all possible Not-a-Number values to a single canonical Not-a-Number value defined by `https://developer.android.com/reference/kotlin/android/util/Half#NaN:kotlin.Short`.

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The bits that represent the half-precision float value |

**See Also**

- `https://developer.android.com/reference/kotlin/android/util/Half#halfToRawIntBits(kotlin.Short)`
- `https://developer.android.com/reference/kotlin/android/util/Half#halfToShortBits(kotlin.Short)`
- `https://developer.android.com/reference/kotlin/android/util/Half#intBitsToHalf(kotlin.Int)`

### halfToRawIntBits

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun halfToRawIntBits(h: Short): Int
```

Returns a representation of the specified half-precision float value according to the bit layout described in `https://developer.android.com/reference/kotlin/android/util/Half#`.

The argument is considered to be a representation of a half-precision float value according to the bit layout described in `https://developer.android.com/reference/kotlin/android/util/Half#`. The 16 most significant bits of the returned value are set to 0.

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The bits that represent the half-precision float value |

**See Also**

- `https://developer.android.com/reference/kotlin/android/util/Half#halfToIntBits(kotlin.Short)`
- `https://developer.android.com/reference/kotlin/android/util/Half#intBitsToHalf(kotlin.Int)`

### halfToShortBits

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun halfToShortBits(h: Short): Short
```

Returns a representation of the specified half-precision float value according to the bit layout described in `https://developer.android.com/reference/kotlin/android/util/Half#`.

Similar to `https://developer.android.com/reference/kotlin/android/util/Half#halfToIntBits(kotlin.Short)`, this method collapses all possible Not-a-Number values to a single canonical Not-a-Number value defined by `https://developer.android.com/reference/kotlin/android/util/Half#NaN:kotlin.Short`.

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | The bits that represent the half-precision float value |

**See Also**

- `https://developer.android.com/reference/kotlin/android/util/Half#halfToIntBits(kotlin.Short)`

### halfValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun halfValue(): Short
```

Returns the half-precision value of this `Half` as a `short` containing the bit representation described in `https://developer.android.com/reference/kotlin/android/util/Half#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | The half-precision float value represented by this object |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code for this `Half` object. The result is the integer bit representation, exactly as produced by the method `https://developer.android.com/reference/kotlin/android/util/Half#halfToIntBits(kotlin.Short)`, of the primitive half-precision float value represented by this `Half` object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A hash code value for this object |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hashCode(h: Short): Int
```

Returns a hash code for a half-precision float value.

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The value to hash |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A hash code value for a half-precision float value |

### intBitsToHalf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun intBitsToHalf(bits: Int): Short
```

Returns the half-precision float value corresponding to a given bit representation.

The argument is considered to be a representation of a half-precision float value according to the bit layout described in `https://developer.android.com/reference/kotlin/android/util/Half#`. The 16 most significant bits of the argument are ignored.

| Parameters ||
|---|---|
| `bits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An integer |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | The half-precision float value with the same bit pattern |

### isInfinite

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isInfinite(h: Short): Boolean
```

Returns true if the specified half-precision float value represents infinity, false otherwise.

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value is positive infinity or negative infinity, false otherwise |

### isNaN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isNaN(): Boolean
```

Returns true if this `Half` value represents a Not-a-Number, false otherwise.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value is a NaN, false otherwise |

### isNaN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isNaN(h: Short): Boolean
```

Returns true if the specified half-precision float value represents a Not-a-Number, false otherwise.

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value is a NaN, false otherwise |

### isNormalized

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isNormalized(h: Short): Boolean
```

Returns true if the specified half-precision float value is normalized (does not have a subnormal representation). If the specified value is `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_INFINITY:kotlin.Short`, `https://developer.android.com/reference/kotlin/android/util/Half#NEGATIVE_INFINITY:kotlin.Short`, `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_ZERO:kotlin.Short`, `https://developer.android.com/reference/kotlin/android/util/Half#NEGATIVE_ZERO:kotlin.Short`, NaN or any subnormal number, this method returns false.

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value is normalized, false otherwise |

### less

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun less(
    x: Short, 
    y: Short
): Boolean
```

Returns true if the first half-precision float value is less (smaller toward negative infinity) than the second half-precision float value. If either of the values is NaN, the result is false.

| Parameters ||
|---|---|
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The first half-precision value |
| `y` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The second half-precision value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if x is less than y, false otherwise |

### lessEquals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun lessEquals(
    x: Short, 
    y: Short
): Boolean
```

Returns true if the first half-precision float value is less (smaller toward negative infinity) than or equal to the second half-precision float value. If either of the values is NaN, the result is false.

| Parameters ||
|---|---|
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The first half-precision value |
| `y` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The second half-precision value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if x is less than or equal to y, false otherwise |

### max

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun max(
    x: Short, 
    y: Short
): Short
```

Returns the larger of two half-precision float values (the value closest to positive infinity). Special values are handled in the following ways:

- If either value is NaN, the result is NaN
- `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_ZERO:kotlin.Short` is greater than `https://developer.android.com/reference/kotlin/android/util/Half#NEGATIVE_ZERO:kotlin.Short`

<br />

| Parameters ||
|---|---|
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The first half-precision value |
| `y` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The second half-precision value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | The larger of the two specified half-precision values |

### min

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun min(
    x: Short, 
    y: Short
): Short
```

Returns the smaller of two half-precision float values (the value closest to negative infinity). Special values are handled in the following ways:

- If either value is NaN, the result is NaN
- `https://developer.android.com/reference/kotlin/android/util/Half#NEGATIVE_ZERO:kotlin.Short` is smaller than `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_ZERO:kotlin.Short`

<br />

| Parameters ||
|---|---|
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The first half-precision value |
| `y` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The second half-precision value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | The smaller of the two specified half-precision values |

### parseHalf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parseHalf(s: String): Short
```

Returns the half-precision float value represented by the specified string. Calling this method is equivalent to calling `toHalf(Float.parseString(h))`. See `https://developer.android.com/reference/kotlin/java/lang/Float.html#valueOf(kotlin.String)` for more information on the format of the string representation.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The string to be parsed. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | A half-precision float value represented by the string |

| Exceptions ||
|---|---|
| `java.lang.NumberFormatException` | if the string does not contain a parsable half-precision float value |

### round

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun round(h: Short): Short
```

Returns the closest integral half-precision float value to the specified half-precision float value. Special values are handled in the following ways:

- If the specified half-precision float is NaN, the result is NaN
- If the specified half-precision float is infinity (negative or positive), the result is infinity (with the same sign)
- If the specified half-precision float is zero (negative or positive), the result is zero (with the same sign)

<br />

**Note:** Unlike the identically named `int java.lang.Math.round(float)` method, this returns a Half value stored in a short, **not** an actual short integer result.

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | The value of the specified half-precision float rounded to the nearest half-precision float value |

### toByte

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toByte(): Byte
```

Returns the value of this `Half` as a `byte` after a narrowing primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | The half-precision float value represented by this object converted to type `byte` |

### toDouble

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toDouble(): Double
```

Returns the value of this `Half` as a `double` after a widening primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | The half-precision float value represented by this object converted to type `double` |

### toFloat

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toFloat(): Float
```

Returns the value of this `Half` as a `float` after a widening primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The half-precision float value represented by this object converted to type `float` |

### toFloat

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toFloat(h: Short): Float
```

Converts the specified half-precision float value into a single-precision float value. The following special cases are handled:

- If the input is `https://developer.android.com/reference/kotlin/android/util/Half#NaN:kotlin.Short`, the returned value is `https://developer.android.com/reference/kotlin/java/lang/Float.html#NaN:kotlin.Float`
- If the input is `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_INFINITY:kotlin.Short` or `https://developer.android.com/reference/kotlin/android/util/Half#NEGATIVE_INFINITY:kotlin.Short`, the returned value is respectively `https://developer.android.com/reference/kotlin/java/lang/Float.html#POSITIVE_INFINITY:kotlin.Float` or `https://developer.android.com/reference/kotlin/java/lang/Float.html#NEGATIVE_INFINITY:kotlin.Float`
- If the input is 0 (positive or negative), the returned value is +/-0.0f
- Otherwise, the returned value is a normalized single-precision float value

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The half-precision float value to convert to single-precision |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | A normalized single-precision float value |

### toHalf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toHalf(f: Float): Short
```

Converts the specified single-precision float value into a half-precision float value. The following special cases are handled:

- If the input is NaN (see `https://developer.android.com/reference/kotlin/java/lang/Float.html#isNaN(kotlin.Float)`), the returned value is `https://developer.android.com/reference/kotlin/android/util/Half#NaN:kotlin.Short`
- If the input is `https://developer.android.com/reference/kotlin/java/lang/Float.html#POSITIVE_INFINITY:kotlin.Float` or `https://developer.android.com/reference/kotlin/java/lang/Float.html#NEGATIVE_INFINITY:kotlin.Float`, the returned value is respectively `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_INFINITY:kotlin.Short` or `https://developer.android.com/reference/kotlin/android/util/Half#NEGATIVE_INFINITY:kotlin.Short`
- If the input is 0 (positive or negative), the returned value is `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_ZERO:kotlin.Short` or `https://developer.android.com/reference/kotlin/android/util/Half#NEGATIVE_ZERO:kotlin.Short`
- If the input is a less than `https://developer.android.com/reference/kotlin/android/util/Half#MIN_VALUE:kotlin.Short`, the returned value is flushed to `https://developer.android.com/reference/kotlin/android/util/Half#POSITIVE_ZERO:kotlin.Short` or `https://developer.android.com/reference/kotlin/android/util/Half#NEGATIVE_ZERO:kotlin.Short`
- If the input is a less than `https://developer.android.com/reference/kotlin/android/util/Half#MIN_NORMAL:kotlin.Short`, the returned value is a denorm half-precision float
- Otherwise, the returned value is rounded to the nearest representable half-precision float value

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The single-precision float value to convert to half-precision |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | A half-precision float value |

### toHexString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toHexString(h: Short): String
```

Returns a hexadecimal string representation of the specified half-precision float value. If the value is a NaN, the result is `"NaN"`, otherwise the result follows this format:

- If the sign is positive, no sign character appears in the result
- If the sign is negative, the first character is `'-'`
- If the value is inifinity, the string is `"Infinity"`
- If the value is 0, the string is `"0x0.0p0"`
- If the value has a normalized representation, the exponent and significand are represented in the string in two fields. The significand starts with `"0x1."` followed by its lowercase hexadecimal representation. Trailing zeroes are removed unless all digits are 0, then a single zero is used. The significand representation is followed by the exponent, represented by `"p"`, itself followed by a decimal string of the unbiased exponent
- If the value has a subnormal representation, the significand starts with `"0x0."` followed by its lowercase hexadecimal representation. Trailing zeroes are removed unless all digits are 0, then a single zero is used. The significand representation is followed by the exponent, represented by `"p-14"`

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A hexadecimal string representation of the specified value. This value cannot be `null`. |

### toInt

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toInt(): Int
```

Returns the value of this `Half` as a `int` after a narrowing primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The half-precision float value represented by this object converted to type `int` |

### toLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toLong(): Long
```

Returns the value of this `Half` as a `long` after a narrowing primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The half-precision float value represented by this object converted to type `long` |

### toShort

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toShort(): Short
```

Returns the value of this `Half` as a `short` after a narrowing primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | The half-precision float value represented by this object converted to type `short` |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the specified half-precision float value. See `https://developer.android.com/reference/kotlin/android/util/Half#toString(kotlin.Short)` for more information.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A string representation of this `Half` object. This value cannot be `null`. |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(h: Short): String
```

Returns a string representation of the specified half-precision float value. Calling this method is equivalent to calling `Float.toString(toFloat(h))`. See `https://developer.android.com/reference/kotlin/java/lang/Float.html#toString(kotlin.Float)` for more information on the format of the string representation.

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A string representation of the specified value. This value cannot be `null`. |

### trunc

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun trunc(h: Short): Short
```

Returns the truncated half-precision float value of the specified half-precision float value. Special values are handled in the following ways:

- If the specified half-precision float is NaN, the result is NaN
- If the specified half-precision float is infinity (negative or positive), the result is infinity (with the same sign)
- If the specified half-precision float is zero (negative or positive), the result is zero (with the same sign)

<br />

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | The truncated half-precision float value of the specified half-precision float value |

### valueOf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(f: Float): Half
```

Returns a `Half` instance representing the specified float value.

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): A float value |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Half#` | a `Half` instance representing `f` This value cannot be `null`. |

### valueOf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(s: String): Half
```

Returns a `Half` instance representing the specified string value. Calling this method is equivalent to calling `toHalf(Float.parseString(h))`. See `https://developer.android.com/reference/kotlin/java/lang/Float.html#valueOf(kotlin.String)` for more information on the format of the string representation.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The string to be parsed. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Half#` | a `Half` instance representing `h` This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NumberFormatException` | if the string does not contain a parsable half-precision float value |

### valueOf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(h: Short): Half
```

Returns a `Half` instance representing the specified half-precision float value.

| Parameters ||
|---|---|
| `h` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): A half-precision float value |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Half#` | a `Half` instance representing `h` This value cannot be `null`. |
