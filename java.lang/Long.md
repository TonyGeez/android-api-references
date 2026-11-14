# Long

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Long

```
class Long : Number, Comparable<Long!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.lang.Long](Long.md) |

The`Long`class wraps a value of the primitive type`long`in an object. An object of type`Long`contains a single field whose type is`long`.

In addition, this class provides several methods for converting a`long`to a`String`and a`String`to a`long`, as well as other constants and methods useful when dealing with a`long`.

Implementation note: The implementations of the "bit twiddling" methods (such as [highestOneBit](Long.md))and [numberOfTrailingZeros](Long.md))) are based on material from Henry S. Warren, Jr.'s*Hacker's Delight*, (Addison Wesley, 2002).

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BYTES](Long.md) The number of bytes used to represent a`long`value in two's complement binary form. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [MAX_VALUE](Long.md) A constant holding the maximum value a`long`can have, 263-1. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [MIN_VALUE](Long.md) A constant holding the minimum value a`long`can have, -263. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIZE](Long.md) The number of bits used to represent a`long`value in two's complement binary form. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Long](Long.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a newly allocated`Long`object that represents the`long`value indicated by the`String`parameter. |
| [Long](Long.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs a newly allocated`Long`object that represents the specified`long`argument. |

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bitCount](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the number of one-bits in the two's complement binary representation of the specified`long`value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](Long.md))`(`x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `y:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Compares two`long`values numerically. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](Long.md))`(`other:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Compares two`Long`objects numerically. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareUnsigned](Long.md))`(`x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `y:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Compares two`long`values numerically treating the values as unsigned. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [compress](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `mask:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the value obtained by compressing the bits of the specified`long`value,`i`, in accordance with the specified bit mask. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [decode](Long.md))`(`nm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Decodes a`String`into a`Long`. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [divideUnsigned](Long.md))`(`dividend:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `divisor:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the unsigned quotient of dividing the first argument by the second where each argument and the result is interpreted as an unsigned value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Long.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this object to the specified object. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [expand](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `mask:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the value obtained by expanding the bits of the specified`long`value,`i`, in accordance with the specified bit mask. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)? | [getLong](Long.md))`(`nm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Determines the`long`value of the system property with the specified name. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)? | [getLong](Long.md))`(`nm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `val:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)?`)` Returns the`long`value of the system property with the specified name. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)? | [getLong](Long.md))`(`nm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `val:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Determines the`long`value of the system property with the specified name. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Long.md))`()` Returns a hash code for this`Long`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Long.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a hash code for a`long`value; compatible with`Long.hashCode()`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [highestOneBit](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a`long`value with at most a single one-bit, in the position of the highest-order ("leftmost") one-bit in the specified`long`value. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [lowestOneBit](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a`long`value with at most a single one-bit, in the position of the lowest-order ("rightmost") one-bit in the specified`long`value. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [max](Long.md))`(`a:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `b:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the greater of two`long`values as if by calling [Math.max](Math.md)). |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [min](Long.md))`(`a:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `b:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the smaller of two`long`values as if by calling [Math.min](Math.md)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [numberOfLeadingZeros](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the number of zero bits preceding the highest-order ("leftmost") one-bit in the two's complement binary representation of the specified`long`value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [numberOfTrailingZeros](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the number of zero bits following the lowest-order ("rightmost") one-bit in the two's complement binary representation of the specified`long`value. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [parseLong](Long.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `beginIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Parses the [CharSequence](CharSequence.md) argument as a signed`long`in the specified`radix`, beginning at the specified`beginIndex`and extending to`endIndex - 1`. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [parseLong](Long.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Parses the string argument as a signed decimal`long`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [parseLong](Long.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Parses the string argument as a signed`long`in the radix specified by the second argument. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [parseUnsignedLong](Long.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `beginIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Parses the [CharSequence](CharSequence.md) argument as an unsigned`long`in the specified`radix`, beginning at the specified`beginIndex`and extending to`endIndex - 1`. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [parseUnsignedLong](Long.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Parses the string argument as an unsigned decimal`long`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [parseUnsignedLong](Long.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Parses the string argument as an unsigned`long`in the radix specified by the second argument. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [remainderUnsigned](Long.md))`(`dividend:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `divisor:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the unsigned remainder from dividing the first argument by the second where each argument and the result is interpreted as an unsigned value. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [reverse](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the value obtained by reversing the order of the bits in the two's complement binary representation of the specified`long`value. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [reverseBytes](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the value obtained by reversing the order of the bytes in the two's complement representation of the specified`long`value. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [rotateLeft](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `distance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value obtained by rotating the two's complement binary representation of the specified`long`value left by the specified number of bits. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [rotateRight](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `distance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value obtained by rotating the two's complement binary representation of the specified`long`value right by the specified number of bits. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [signum](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the signum function of the specified`long`value. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [sum](Long.md))`(`a:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `b:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Adds two`long`values together as per the + operator. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toBinaryString](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a string representation of the`long`argument as an unsigned integer in base 2. |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [toByte](Long.md))`()` Returns the value of this`Long`as a`byte`after a narrowing primitive conversion. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](Long.md))`()` Returns the value of this`Long`as a`double`after a widening primitive conversion. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](Long.md))`()` Returns the value of this`Long`as a`float`after a widening primitive conversion. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toHexString](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a string representation of the`long`argument as an unsigned integer in base 16. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](Long.md))`()` Returns the value of this`Long`as an`int`after a narrowing primitive conversion. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](Long.md))`()` Returns the value of this`Long`as a`long`value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toOctalString](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a string representation of the`long`argument as an unsigned integer in base 8. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [toShort](Long.md))`()` Returns the value of this`Long`as a`short`after a narrowing primitive conversion. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Long.md))`()` Returns a`String`object representing this`Long`'s value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a`String`object representing the specified`long`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a string representation of the first argument in the radix specified by the second argument. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toUnsignedString](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a string representation of the argument as an unsigned decimal value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toUnsignedString](Long.md))`(`i:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a string representation of the first argument as an unsigned integer value in the radix specified by the second argument. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [valueOf](Long.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns a`Long`object holding the value of the specified`String`. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [valueOf](Long.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`Long`object holding the value extracted from the specified`String`when parsed with the radix given by the second argument. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [valueOf](Long.md))`(`l:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a`Long`instance representing the specified`long`value. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Class](Class.md)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>! | [TYPE](Long.md) The`Class`instance representing the primitive type`long`. |

## Constants

### BYTES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BYTES: Int
```

The number of bytes used to represent a`long`value in two's complement binary form. 

 Value: 8

### MAX_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_VALUE: Long
```

A constant holding the maximum value a`long`can have, 263-1. 

 Value: 9223372036854775807L

### MIN_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_VALUE: Long
```

A constant holding the minimum value a`long`can have, -263. 

 Value: -9223372036854775808L

### SIZE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIZE: Int
```

The number of bits used to represent a`long`value in two's complement binary form. 

 Value: 64

## Public constructors

### Long

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Long(s: String)
```

**Deprecated:** *It is rarely appropriate to use this constructor. Use [parseLong(java.lang.String)](Long.md))to convert a string to a`long`primitive, or use [valueOf(java.lang.String)](Long.md))to convert a string to a`Long`object.*

Constructs a newly allocated`Long`object that represents the`long`value indicated by the`String`parameter. The string is converted to a`long`value in exactly the manner used by the`parseLong`method for radix 10.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the`String`to be converted to a`Long`. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------|
| `java.lang.NumberFormatException` | if the`String`does not contain a parsable`long`. |

### Long

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Long(value: Long)
```

**Deprecated:** *It is rarely appropriate to use this constructor. The static factory [valueOf(long)](Long.md))is generally a better choice, as it is likely to yield significantly better space and time performance.*

Constructs a newly allocated`Long`object that represents the specified`long`argument.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to be represented by the`Long`object. |

## Public methods

### bitCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun bitCount(i: Long): Int
```

Returns the number of one-bits in the two's complement binary representation of the specified`long`value. This function is sometimes referred to as the*population count*.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value whose bits are to be counted |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of one-bits in the two's complement binary representation of the specified`long`value. |

### compare

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compare(
    x: Long, 
    y: Long
): Int
```

Compares two`long`values numerically. The value returned is identical to what would be returned by: 

```kotlin
Long.valueOf(x).compareTo(Long.valueOf(y))
  
```

<br />

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the first`long`to compare |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the second`long`to compare |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if`x == y`; a value less than`0`if`x < y`; and a value greater than`0`if`x > y` |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: Long): Int
```

Compares two`Long`objects numerically.

| Parameters ||
|---------------|----------------------------|
| `o` | the object to be compared. |
| `anotherLong` | the`Long`to be compared. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if this`Long`is equal to the argument`Long`; a value less than`0`if this`Long`is numerically less than the argument`Long`; and a value greater than`0`if this`Long`is numerically greater than the argument`Long`(signed comparison). |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### compareUnsigned

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compareUnsigned(
    x: Long, 
    y: Long
): Int
```

Compares two`long`values numerically treating the values as unsigned.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the first`long`to compare |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the second`long`to compare |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if`x == y`; a value less than`0`if`x < y`as unsigned values; and a value greater than`0`if`x > y`as unsigned values |

### compress

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compress(
    i: Long, 
    mask: Long
): Long
```

Returns the value obtained by compressing the bits of the specified`long`value,`i`, in accordance with the specified bit mask.

For each one-bit value`mb`of the mask, from least significant to most significant, the bit value of`i`at the same bit location as`mb`is assigned to the compressed value contiguously starting from the least significant bit location. All the upper remaining bits of the compressed value are set to zero.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value whose bits are to be compressed |
| `mask` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the bit mask |

| Return ||
|------------------------------------------------------------------------------|----------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the compressed value |

**See Also**

- [#expand](Long.md)) 

### decode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun decode(nm: String): Long
```

Decodes a`String`into a`Long`. Accepts decimal, hexadecimal, and octal numbers given by the following grammar:

*DecodableString:*
: *Signopt DecimalNumeral*
: *Signopt* `0x`*HexDigits*
: *Signopt* `0X`*HexDigits*
: *Signopt* *HexDigits*
: *Signopt* `0`*OctalDigits*

*Sign:*
: `-`
: `+`
*DecimalNumeral* ,*HexDigits* , and*OctalDigits* are as defined in section {@jls 3.10.1} of The Java Language Specification, except that underscores are not accepted between digits.

<br />

The sequence of characters following an optional sign and/or radix specifier ("`0x`", "`0X`", "", or leading zero) is parsed as by the`Long.parseLong`method with the indicated radix (10, 16, or 8). This sequence of characters must represent a positive value or a [NumberFormatException](NumberFormatException.md) will be thrown. The result is negated if first character of the specified`String`is the minus sign. No whitespace characters are permitted in the`String`.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------|
| `nm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the`String`to decode. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a`Long`object holding the`long`value represented by`nm` |

| Exceptions ||
|-----------------------------------|--------------------------------------------------|
| `java.lang.NumberFormatException` | if the`String`does not contain a parsable`long`. |

**See Also**

- [java.lang.Long#parseLong(String, int)](Long.md)) 

### divideUnsigned

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun divideUnsigned(
    dividend: Long, 
    divisor: Long
): Long
```

Returns the unsigned quotient of dividing the first argument by the second where each argument and the result is interpreted as an unsigned value.

Note that in two's complement arithmetic, the three other basic arithmetic operations of add, subtract, and multiply are bit-wise identical if the two operands are regarded as both being signed or both being unsigned. Therefore separate`addUnsigned`, etc. methods are not provided.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------|
| `dividend` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to be divided |
| `divisor` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value doing the dividing |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the unsigned quotient of the first argument divided by the second argument |

**See Also**

- [#remainderUnsigned](Long.md)) 

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this object to the specified object. The result is`true`if and only if the argument is not`null`and is a`Long`object that contains the same`long`value as this object.

| Parameters ||
|-------|-----------------------------|
| `obj` | the object to compare with. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects are the same;`false`otherwise. |

### expand

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun expand(
    i: Long, 
    mask: Long
): Long
```

Returns the value obtained by expanding the bits of the specified`long`value,`i`, in accordance with the specified bit mask.

For each one-bit value`mb`of the mask, from least significant to most significant, the next contiguous bit value of`i`starting at the least significant bit is assigned to the expanded value at the same bit location as`mb`. All other remaining bits of the expanded value are set to zero.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value whose bits are to be expanded |
| `mask` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the bit mask |

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the expanded value |

**See Also**

- [#compress](Long.md)) 

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getLong(nm: String): Long?
```

Determines the`long`value of the system property with the specified name.

The first argument is treated as the name of a system property. System properties are accessible through the [java.lang.System#getProperty(java.lang.String)](System.md))method. The string value of this property is then interpreted as a`long`value using the grammar supported by [decode](Long.md))and a`Long`object representing this value is returned.

If there is no property with the specified name, if the specified name is empty or`null`, or if the property does not have the correct numeric format, then`null`is returned.

In other words, this method returns a`Long`object equal to the value of:
`getLong(nm, null)`

| Parameters ||
|------|-------------------------------------------------------------------------------------------------|
| `nm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):property name. |

| Return ||
|-------------------------------------------------------------------------------|---------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)? | the`Long`value of the property. |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | for the same reasons as [System.getProperty](System.md)) |

**See Also**

- [java.lang.System#getProperty(java.lang.String)](System.md))
- [java.lang.System#getProperty(java.lang.String, java.lang.String)](System.md)) 

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getLong(
    nm: String, 
    val: Long?
): Long?
```

Returns the`long`value of the system property with the specified name. The first argument is treated as the name of a system property. System properties are accessible through the [java.lang.System#getProperty(java.lang.String)](System.md))method. The string value of this property is then interpreted as a`long`value, as per the [decode](Long.md))method, and a`Long`object representing this value is returned; in summary:

- If the property value begins with the two ASCII characters`0x`or the ASCII character, not followed by a minus sign, then the rest of it is parsed as a hexadecimal integer exactly as for the method [valueOf(java.lang.String,int)](Long.md))with radix 16.
- If the property value begins with the ASCII character`0`followed by another character, it is parsed as an octal integer exactly as by the method [valueOf(java.lang.String,int)](Long.md))with radix 8.
- Otherwise the property value is parsed as a decimal integer exactly as by the method [valueOf(java.lang.String,int)](Long.md))with radix 10.

<br />

Note that, in every case, neither`L`(`'\u005Cu004C'`) nor`l`(`'\u005Cu006C'`) is permitted to appear at the end of the property value as a type indicator, as would be permitted in Java programming language source code.

The second argument is the default value. The default value is returned if there is no property of the specified name, if the property does not have the correct numeric format, or if the specified name is empty or`null`.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------|
| `nm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):property name. |
| `val` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):default value. |

| Return ||
|-------------------------------------------------------------------------------|---------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)? | the`Long`value of the property. |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | for the same reasons as [System.getProperty](System.md)) |

**See Also**

- [java.lang.System#getProperty(java.lang.String)](System.md))
- [java.lang.System#getProperty(java.lang.String, java.lang.String)](System.md)) 

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getLong(
    nm: String, 
    val: Long
): Long?
```

Determines the`long`value of the system property with the specified name.

The first argument is treated as the name of a system property. System properties are accessible through the [java.lang.System#getProperty(java.lang.String)](System.md))method. The string value of this property is then interpreted as a`long`value using the grammar supported by [decode](Long.md))and a`Long`object representing this value is returned.

The second argument is the default value. A`Long`object that represents the value of the second argument is returned if there is no property of the specified name, if the property does not have the correct numeric format, or if the specified name is empty or null.

In other words, this method returns a`Long`object equal to the value of:
`getLong(nm, Long.valueOf(val))`but in practice it may be implemented in a manner such as: 

```kotlin
Long result = getLong(nm, null);
  return (result == null) ? Long.valueOf(val) : result;
  
```
to avoid the unnecessary allocation of a`Long`object when the default value is not needed.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------|
| `nm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):property name. |
| `val` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):default value. |

| Return ||
|-------------------------------------------------------------------------------|---------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)? | the`Long`value of the property. |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | for the same reasons as [System.getProperty](System.md)) |

**See Also**

- [java.lang.System#getProperty(java.lang.String)](System.md))
- [java.lang.System#getProperty(java.lang.String, java.lang.String)](System.md)) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code for this`Long`. The result is the exclusive OR of the two halves of the primitive`long`value held by this`Long`object. That is, the hashcode is the value of the expression:`(int)(this.longValue()^(this.longValue()>>>32))`

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun hashCode(value: Long): Int
```

Returns a hash code for a`long`value; compatible with`Long.hashCode()`.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to hash |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for a`long`value. |

### highestOneBit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun highestOneBit(i: Long): Long
```

Returns a`long`value with at most a single one-bit, in the position of the highest-order ("leftmost") one-bit in the specified`long`value. Returns zero if the specified value has no one-bits in its two's complement binary representation, that is, if it is equal to zero.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value whose highest one bit is to be computed |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a`long`value with a single one-bit, in the position of the highest-order one-bit in the specified value, or zero if the specified value is itself equal to zero. |

### lowestOneBit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun lowestOneBit(i: Long): Long
```

Returns a`long`value with at most a single one-bit, in the position of the lowest-order ("rightmost") one-bit in the specified`long`value. Returns zero if the specified value has no one-bits in its two's complement binary representation, that is, if it is equal to zero.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value whose lowest one bit is to be computed |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a`long`value with a single one-bit, in the position of the lowest-order one-bit in the specified value, or zero if the specified value is itself equal to zero. |

### max

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun max(
    a: Long, 
    b: Long
): Long
```

Returns the greater of two`long`values as if by calling [Math.max](Math.md)).

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------|
| `a` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the first operand |
| `b` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the second operand |

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the greater of`a`and`b` |

**See Also**

- [java.util.function.BinaryOperator](../java.util.function/BinaryOperator.md) 

### min

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun min(
    a: Long, 
    b: Long
): Long
```

Returns the smaller of two`long`values as if by calling [Math.min](Math.md)).

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------|
| `a` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the first operand |
| `b` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the second operand |

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the smaller of`a`and`b` |

**See Also**

- [java.util.function.BinaryOperator](../java.util.function/BinaryOperator.md) 

### numberOfLeadingZeros

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun numberOfLeadingZeros(i: Long): Int
```

Returns the number of zero bits preceding the highest-order ("leftmost") one-bit in the two's complement binary representation of the specified`long`value. Returns 64 if the specified value has no one-bits in its two's complement representation, in other words if it is equal to zero.

Note that this method is closely related to the logarithm base 2. For all positive`long`values x:

- floor(log2(x)) =`63 - numberOfLeadingZeros(x)`
- ceil(log2(x)) =`64 - numberOfLeadingZeros(x - 1)`

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value whose number of leading zeros is to be computed |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of zero bits preceding the highest-order ("leftmost") one-bit in the two's complement binary representation of the specified`long`value, or 64 if the value is equal to zero. |

### numberOfTrailingZeros

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun numberOfTrailingZeros(i: Long): Int
```

Returns the number of zero bits following the lowest-order ("rightmost") one-bit in the two's complement binary representation of the specified`long`value. Returns 64 if the specified value has no one-bits in its two's complement representation, in other words if it is equal to zero.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value whose number of trailing zeros is to be computed |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of zero bits following the lowest-order ("rightmost") one-bit in the two's complement binary representation of the specified`long`value, or 64 if the value is equal to zero. |

### parseLong

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseLong(
    s: CharSequence, 
    beginIndex: Int, 
    endIndex: Int, 
    radix: Int
): Long
```

Parses the [CharSequence](CharSequence.md) argument as a signed`long`in the specified`radix`, beginning at the specified`beginIndex`and extending to`endIndex - 1`.

The method does not take steps to guard against the`CharSequence`being mutated while parsing.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):the`CharSequence`containing the`long`representation to be parsed |
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the beginning index, inclusive. |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the ending index, exclusive. |
| --- | --- |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to be used while parsing`s`. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the signed`long`represented by the subsequence in the specified radix. |

| Exceptions ||
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`s`is null. |
| `java.lang.IndexOutOfBoundsException` | if`beginIndex`is negative, or if`beginIndex`is greater than`endIndex`or if`endIndex`is greater than`s.length()`. |
| `java.lang.NumberFormatException` | if the`CharSequence`does not contain a parsable`long`in the specified`radix`, or if`radix`is either smaller than [java.lang.Character#MIN_RADIX](Character.md) or larger than [java.lang.Character#MAX_RADIX](Character.md). |
| --- | --- |

### parseLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseLong(s: String): Long
```

Parses the string argument as a signed decimal`long`. The characters in the string must all be decimal digits, except that the first character may be an ASCII minus sign`'-'`(`\u005Cu002D'`) to indicate a negative value or an ASCII plus sign`'+'`(`'\u005Cu002B'`) to indicate a positive value. The resulting`long`value is returned, exactly as if the argument and the radix`10`were given as arguments to the [parseLong(java.lang.String,int)](Long.md))method.

Note that neither the character`L`(`'\u005Cu004C'`) nor`l`(`'\u005Cu006C'`) is permitted to appear at the end of the string as a type indicator, as would be permitted in Java programming language source code.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a`String`containing the`long`representation to be parsed |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the`long`represented by the argument in decimal. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------|
| `java.lang.NumberFormatException` | if the string does not contain a parsable`long`. |

### parseLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseLong(
    s: String, 
    radix: Int
): Long
```

Parses the string argument as a signed`long`in the radix specified by the second argument. The characters in the string must all be digits of the specified radix (as determined by whether [java.lang.Character#digit(char, int)](Character.md))returns a nonnegative value), except that the first character may be an ASCII minus sign`'-'`(`'\u005Cu002D'`) to indicate a negative value or an ASCII plus sign`'+'`(`'\u005Cu002B'`) to indicate a positive value. The resulting`long`value is returned.

Note that neither the character`L`(`'\u005Cu004C'`) nor`l`(`'\u005Cu006C'`) is permitted to appear at the end of the string as a type indicator, as would be permitted in Java programming language source code - except that either`L`or`l`may appear as a digit for a radix greater than or equal to 22.

An exception of type`NumberFormatException`is thrown if any of the following situations occurs:

- The first argument is`null`or is a string of length zero.
- The`radix`is either smaller than [java.lang.Character#MIN_RADIX](Character.md) or larger than [java.lang.Character#MAX_RADIX](Character.md).
- Any character of the string is not a digit of the specified radix, except that the first character may be a minus sign`'-'`(`'\u005Cu002d'`) or plus sign`'+'`(`'\u005Cu002B'`) provided that the string is longer than length 1.
- The value represented by the string is not a value of type`long`.

Examples: 

```kotlin
parseLong("0", 10) returns 0L
  parseLong("473", 10) returns 473L
  parseLong("+42", 10) returns 42L
  parseLong("-0", 10) returns 0L
  parseLong("-FF", 16) returns -255L
  parseLong("1100110", 2) returns 102L
  parseLong("99", 8) throws a NumberFormatException
  parseLong("Hazelnut", 10) throws a NumberFormatException
  parseLong("Hazelnut", 36) returns 1356099454469L
  
```

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the`String`containing the`long`representation to be parsed. |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to be used while parsing`s`. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the`long`represented by the string argument in the specified radix. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------|
| `java.lang.NumberFormatException` | if the string does not contain a parsable`long`. |

### parseUnsignedLong

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseUnsignedLong(
    s: CharSequence, 
    beginIndex: Int, 
    endIndex: Int, 
    radix: Int
): Long
```

Parses the [CharSequence](CharSequence.md) argument as an unsigned`long`in the specified`radix`, beginning at the specified`beginIndex`and extending to`endIndex - 1`.

The method does not take steps to guard against the`CharSequence`being mutated while parsing.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):the`CharSequence`containing the unsigned`long`representation to be parsed |
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the beginning index, inclusive. |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the ending index, exclusive. |
| --- | --- |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to be used while parsing`s`. |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the unsigned`long`represented by the subsequence in the specified radix. |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`s`is null. |
| `java.lang.IndexOutOfBoundsException` | if`beginIndex`is negative, or if`beginIndex`is greater than`endIndex`or if`endIndex`is greater than`s.length()`. |
| `java.lang.NumberFormatException` | if the`CharSequence`does not contain a parsable unsigned`long`in the specified`radix`, or if`radix`is either smaller than [java.lang.Character#MIN_RADIX](Character.md) or larger than [java.lang.Character#MAX_RADIX](Character.md). |
| --- | --- |

### parseUnsignedLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseUnsignedLong(s: String): Long
```

Parses the string argument as an unsigned decimal`long`. The characters in the string must all be decimal digits, except that the first character may be an ASCII plus sign`'+'`(`'\u005Cu002B'`). The resulting integer value is returned, exactly as if the argument and the radix 10 were given as arguments to the [parseUnsignedLong(java.lang.String,int)](Long.md))method.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a`String`containing the unsigned`long`representation to be parsed |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the unsigned`long`value represented by the decimal string argument |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------|
| `java.lang.NumberFormatException` | if the string does not contain a parsable unsigned integer. |

### parseUnsignedLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseUnsignedLong(
    s: String, 
    radix: Int
): Long
```

Parses the string argument as an unsigned`long`in the radix specified by the second argument. An unsigned integer maps the values usually associated with negative numbers to positive numbers larger than`MAX_VALUE`. The characters in the string must all be digits of the specified radix (as determined by whether [java.lang.Character#digit(char, int)](Character.md))returns a nonnegative value), except that the first character may be an ASCII plus sign`'+'`(`'\u005Cu002B'`). The resulting integer value is returned.

An exception of type`NumberFormatException`is thrown if any of the following situations occurs:

- The first argument is`null`or is a string of length zero.
- The radix is either smaller than [java.lang.Character#MIN_RADIX](Character.md) or larger than [java.lang.Character#MAX_RADIX](Character.md).
- Any character of the string is not a digit of the specified radix, except that the first character may be a plus sign`'+'`(`'\u005Cu002B'`) provided that the string is longer than length 1.
- The value represented by the string is larger than the largest unsigned`long`, 264-1.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the`String`containing the unsigned integer representation to be parsed |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to be used while parsing`s`. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the unsigned`long`represented by the string argument in the specified radix. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------|
| `java.lang.NumberFormatException` | if the`String`does not contain a parsable`long`. |

### remainderUnsigned

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun remainderUnsigned(
    dividend: Long, 
    divisor: Long
): Long
```

Returns the unsigned remainder from dividing the first argument by the second where each argument and the result is interpreted as an unsigned value.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------|
| `dividend` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to be divided |
| `divisor` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value doing the dividing |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the unsigned remainder of the first argument divided by the second argument |

**See Also**

- [#divideUnsigned](Long.md)) 

### reverse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun reverse(i: Long): Long
```

Returns the value obtained by reversing the order of the bits in the two's complement binary representation of the specified`long`value.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to be reversed |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value obtained by reversing order of the bits in the specified`long`value. |

### reverseBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun reverseBytes(i: Long): Long
```

Returns the value obtained by reversing the order of the bytes in the two's complement representation of the specified`long`value.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value whose bytes are to be reversed |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value obtained by reversing the bytes in the specified`long`value. |

### rotateLeft

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun rotateLeft(
    i: Long, 
    distance: Int
): Long
```

Returns the value obtained by rotating the two's complement binary representation of the specified`long`value left by the specified number of bits. (Bits shifted out of the left hand, or high-order, side reenter on the right, or low-order.)

Note that left rotation with a negative distance is equivalent to right rotation:`rotateLeft(val, -distance) == rotateRight(val, distance)`. Note also that rotation by any multiple of 64 is a no-op, so all but the last six bits of the rotation distance can be ignored, even if the distance is negative:`rotateLeft(val, distance) == rotateLeft(val, distance & 0x3F)`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value whose bits are to be rotated left |
| `distance` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bit positions to rotate left |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value obtained by rotating the two's complement binary representation of the specified`long`value left by the specified number of bits. |

### rotateRight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun rotateRight(
    i: Long, 
    distance: Int
): Long
```

Returns the value obtained by rotating the two's complement binary representation of the specified`long`value right by the specified number of bits. (Bits shifted out of the right hand, or low-order, side reenter on the left, or high-order.)

Note that right rotation with a negative distance is equivalent to left rotation:`rotateRight(val, -distance) == rotateLeft(val, distance)`. Note also that rotation by any multiple of 64 is a no-op, so all but the last six bits of the rotation distance can be ignored, even if the distance is negative:`rotateRight(val, distance) == rotateRight(val, distance & 0x3F)`.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value whose bits are to be rotated right |
| `distance` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bit positions to rotate right |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value obtained by rotating the two's complement binary representation of the specified`long`value right by the specified number of bits. |

### signum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun signum(i: Long): Int
```

Returns the signum function of the specified`long`value. (The return value is -1 if the specified value is negative; 0 if the specified value is zero; and 1 if the specified value is positive.)

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value whose signum is to be computed |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the signum function of the specified`long`value. |

### sum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun sum(
    a: Long, 
    b: Long
): Long
```

Adds two`long`values together as per the + operator.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------|
| `a` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the first operand |
| `b` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the second operand |

| Return ||
|------------------------------------------------------------------------------|---------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the sum of`a`and`b` |

**See Also**

- [java.util.function.BinaryOperator](../java.util.function/BinaryOperator.md) 

### toBinaryString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toBinaryString(i: Long): String
```

Returns a string representation of the`long`argument as an unsigned integer in base 2.

The unsigned`long`value is the argument plus 264 if the argument is negative; otherwise, it is equal to the argument. This value is converted to a string of ASCII digits in binary (base 2) with no extra leading`0`s.

The value of the argument can be recovered from the returned string`s`by calling [2)](Long.md)).

If the unsigned magnitude is zero, it is represented by a single zero character`'0'`(`'\u005Cu0030'`); otherwise, the first character of the representation of the unsigned magnitude will not be the zero character. The characters`'0'`(`'\u005Cu0030'`) and`'1'`(`'\u005Cu0031'`) are used as binary digits.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a`long`to be converted to a string. |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of the unsigned`long`value represented by the argument in binary (base 2). |

**See Also**

- [#parseUnsignedLong(String, int)](Long.md))
- [#toUnsignedString(long, int)](Long.md)) 

### toByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toByte(): Byte
```

Returns the value of this`Long`as a`byte`after a narrowing primitive conversion.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the numeric value represented by this object after conversion to type`byte`. |

### toDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toDouble(): Double
```

Returns the value of this`Long`as a`double`after a widening primitive conversion.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the numeric value represented by this object after conversion to type`double`. |

### toFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toFloat(): Float
```

Returns the value of this`Long`as a`float`after a widening primitive conversion.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the numeric value represented by this object after conversion to type`float`. |

### toHexString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toHexString(i: Long): String
```

Returns a string representation of the`long`argument as an unsigned integer in base 16.

The unsigned`long`value is the argument plus 264 if the argument is negative; otherwise, it is equal to the argument. This value is converted to a string of ASCII digits in hexadecimal (base 16) with no extra leading`0`s.

The value of the argument can be recovered from the returned string`s`by calling [16)](Long.md)).

If the unsigned magnitude is zero, it is represented by a single zero character`'0'`(`'\u005Cu0030'`); otherwise, the first character of the representation of the unsigned magnitude will not be the zero character. The following characters are used as hexadecimal digits:
`0123456789abcdef`These are the characters`'\u005Cu0030'`through`'\u005Cu0039'`and`'\u005Cu0061'`through`'\u005Cu0066'`. If uppercase letters are desired, the [java.lang.String#toUpperCase()](String.md))method may be called on the result:`Long.toHexString(n).toUpperCase()`

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a`long`to be converted to a string. |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of the unsigned`long`value represented by the argument in hexadecimal (base 16). |

**See Also**

- [#parseUnsignedLong(String, int)](Long.md))
- [#toUnsignedString(long, int)](Long.md)) 

### toInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toInt(): Int
```

Returns the value of this`Long`as an`int`after a narrowing primitive conversion.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by this object after conversion to type`int`. |

### toLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toLong(): Long
```

Returns the value of this`Long`as a`long`value.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the numeric value represented by this object after conversion to type`long`. |

### toOctalString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toOctalString(i: Long): String
```

Returns a string representation of the`long`argument as an unsigned integer in base 8.

The unsigned`long`value is the argument plus 264 if the argument is negative; otherwise, it is equal to the argument. This value is converted to a string of ASCII digits in octal (base 8) with no extra leading`0`s.

The value of the argument can be recovered from the returned string`s`by calling [8)](Long.md)).

If the unsigned magnitude is zero, it is represented by a single zero character`'0'`(`'\u005Cu0030'`); otherwise, the first character of the representation of the unsigned magnitude will not be the zero character. The following characters are used as octal digits:
`01234567`These are the characters`'\u005Cu0030'`through`'\u005Cu0037'`.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a`long`to be converted to a string. |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of the unsigned`long`value represented by the argument in octal (base 8). |

**See Also**

- [#parseUnsignedLong(String, int)](Long.md))
- [#toUnsignedString(long, int)](Long.md)) 

### toShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toShort(): Short
```

Returns the value of this`Long`as a`short`after a narrowing primitive conversion.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the numeric value represented by this object after conversion to type`short`. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a`String`object representing this`Long`'s value. The value is converted to signed decimal representation and returned as a string, exactly as if the`long`value were given as an argument to the [java.lang.Long#toString(long)](Long.md))method.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the value of this object in base 10. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toString(i: Long): String
```

Returns a`String`object representing the specified`long`. The argument is converted to signed decimal representation and returned as a string, exactly as if the argument and the radix 10 were given as arguments to the [toString(long,int)](Long.md))method.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a`long`to be converted. |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the argument in base 10. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toString(
    i: Long, 
    radix: Int
): String
```

Returns a string representation of the first argument in the radix specified by the second argument.

If the radix is smaller than`Character.MIN_RADIX`or larger than`Character.MAX_RADIX`, then the radix`10`is used instead.

If the first argument is negative, the first element of the result is the ASCII minus sign`'-'`(`'\u005Cu002d'`). If the first argument is not negative, no sign character appears in the result.

The remaining characters of the result represent the magnitude of the first argument. If the magnitude is zero, it is represented by a single zero character`'0'`(`'\u005Cu0030'`); otherwise, the first character of the representation of the magnitude will not be the zero character. The following ASCII characters are used as digits:
`0123456789abcdefghijklmnopqrstuvwxyz`These are`'\u005Cu0030'`through`'\u005Cu0039'`and`'\u005Cu0061'`through`'\u005Cu007a'`. If`radix`is N, then the first N of these characters are used as radix-N digits in the order shown. Thus, the digits for hexadecimal (radix 16) are`0123456789abcdef`. If uppercase letters are desired, the [java.lang.String#toUpperCase()](String.md))method may be called on the result:`Long.toString(n, 16).toUpperCase()`

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a`long`to be converted to a string. |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to use in the string representation. |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the argument in the specified radix. |

**See Also**

- [java.lang.Character#MAX_RADIX](Character.md)
- [java.lang.Character#MIN_RADIX](Character.md) 

### toUnsignedString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUnsignedString(i: Long): String
```

Returns a string representation of the argument as an unsigned decimal value. The argument is converted to unsigned decimal representation and returned as a string exactly as if the argument and radix 10 were given as arguments to the [toUnsignedString(long,int)](Long.md))method.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):an integer to be converted to an unsigned string. |

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | an unsigned string representation of the argument. |

**See Also**

- [#toUnsignedString(long, int)](Long.md)) 

### toUnsignedString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUnsignedString(
    i: Long, 
    radix: Int
): String
```

Returns a string representation of the first argument as an unsigned integer value in the radix specified by the second argument.

If the radix is smaller than`Character.MIN_RADIX`or larger than`Character.MAX_RADIX`, then the radix`10`is used instead.

Note that since the first argument is treated as an unsigned value, no leading sign character is printed.

If the magnitude is zero, it is represented by a single zero character`'0'`(`'\u005Cu0030'`); otherwise, the first character of the representation of the magnitude will not be the zero character.

The behavior of radixes and the characters used as digits are the same as [toString](Long.md)).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):an integer to be converted to an unsigned string. |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to use in the string representation. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | an unsigned string representation of the argument in the specified radix. |

**See Also**

- [#toString(long, int)](Long.md)) 

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(s: String): Long
```

Returns a`Long`object holding the value of the specified`String`. The argument is interpreted as representing a signed decimal`long`, exactly as if the argument were given to the [parseLong(java.lang.String)](Long.md))method. The result is a`Long`object that represents the integer value specified by the string.

In other words, this method returns a`Long`object equal to the value of:
`Long.valueOf(Long.parseLong(s))`

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the string to be parsed. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a`Long`object holding the value represented by the string argument. |

| Exceptions ||
|-----------------------------------|--------------------------------------------|
| `java.lang.NumberFormatException` | If the string cannot be parsed as a`long`. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(
    s: String, 
    radix: Int
): Long
```

Returns a`Long`object holding the value extracted from the specified`String`when parsed with the radix given by the second argument. The first argument is interpreted as representing a signed`long`in the radix specified by the second argument, exactly as if the arguments were given to the [parseLong(java.lang.String,int)](Long.md))method. The result is a`Long`object that represents the`long`value specified by the string.

In other words, this method returns a`Long`object equal to the value of:
`Long.valueOf(Long.parseLong(s, radix))`

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the string to be parsed |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to be used in interpreting`s` |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a`Long`object holding the value represented by the string argument in the specified radix. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------|
| `java.lang.NumberFormatException` | If the`String`does not contain a parsable`long`. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(l: Long): Long
```

Returns a`Long`instance representing the specified`long`value. If a new`Long`instance is not required, this method should generally be used in preference to the constructor [Long(long)](Long.md)), as this method is likely to yield significantly better space and time performance by caching frequently requested values. This method will always cache values in the range -128 to 127, inclusive, and may cache other values outside of this range.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------|
| `l` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a long value. |

| Return ||
|------------------------------------------------------------------------------|----------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a`Long`instance representing`l`. |

## Properties

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE: Class<Long!>!
```

The`Class`instance representing the primitive type`long`.
