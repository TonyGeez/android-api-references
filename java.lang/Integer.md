# Integer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Integer

```
class Integer : Number, Comparable<Int!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.lang.Integer](Integer.md) |

The`Integer`class wraps a value of the primitive type`int`in an object. An object of type`Integer`contains a single field whose type is`int`.

In addition, this class provides several methods for converting an`int`to a`String`and a`String`to an`int`, as well as other constants and methods useful when dealing with an`int`.

Implementation note: The implementations of the "bit twiddling" methods (such as [highestOneBit](Integer.md))and [numberOfTrailingZeros](Integer.md))) are based on material from Henry S. Warren, Jr.'s*Hacker's Delight*, (Addison Wesley, 2002).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BYTES](Integer.md) The number of bytes used to represent an`int`value in two's complement binary form. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_VALUE](Integer.md) A constant holding the maximum value an`int`can have, 231-1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIN_VALUE](Integer.md) A constant holding the minimum value an`int`can have, -231. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIZE](Integer.md) The number of bits used to represent an`int`value in two's complement binary form. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Integer](Integer.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a newly allocated`Integer`object that represents the specified`int`value. |
| [Integer](Integer.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a newly allocated`Integer`object that represents the`int`value indicated by the`String`parameter. |

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bitCount](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the number of one-bits in the two's complement binary representation of the specified`int`value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](Integer.md))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Compares two`int`values numerically. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](Integer.md))`(`other:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Compares two`Integer`objects numerically. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareUnsigned](Integer.md))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Compares two`int`values numerically treating the values as unsigned. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compress](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value obtained by compressing the bits of the specified`int`value,`i`, in accordance with the specified bit mask. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [decode](Integer.md))`(`nm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Decodes a`String`into an`Integer`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [divideUnsigned](Integer.md))`(`dividend:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `divisor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the unsigned quotient of dividing the first argument by the second where each argument and the result is interpreted as an unsigned value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Integer.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this object to the specified object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [expand](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value obtained by expanding the bits of the specified`int`value,`i`, in accordance with the specified bit mask. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? | [getInteger](Integer.md))`(`nm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Determines the integer value of the system property with the specified name. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? | [getInteger](Integer.md))`(`nm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `val:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines the integer value of the system property with the specified name. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? | [getInteger](Integer.md))`(`nm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `val:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)?`)` Returns the integer value of the system property with the specified name. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Integer.md))`()` Returns a hash code for this`Integer`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Integer.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a hash code for an`int`value; compatible with`Integer.hashCode()`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [highestOneBit](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an`int`value with at most a single one-bit, in the position of the highest-order ("leftmost") one-bit in the specified`int`value. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lowestOneBit](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an`int`value with at most a single one-bit, in the position of the lowest-order ("rightmost") one-bit in the specified`int`value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [max](Integer.md))`(`a:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the greater of two`int`values as if by calling [Math.max](Math.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [min](Integer.md))`(`a:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the smaller of two`int`values as if by calling [Math.min](Math.md)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [numberOfLeadingZeros](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the number of zero bits preceding the highest-order ("leftmost") one-bit in the two's complement binary representation of the specified`int`value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [numberOfTrailingZeros](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the number of zero bits following the lowest-order ("rightmost") one-bit in the two's complement binary representation of the specified`int`value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parseInt](Integer.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `beginIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Parses the [CharSequence](CharSequence.md) argument as a signed`int`in the specified`radix`, beginning at the specified`beginIndex`and extending to`endIndex - 1`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parseInt](Integer.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Parses the string argument as a signed decimal integer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parseInt](Integer.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Parses the string argument as a signed integer in the radix specified by the second argument. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parseUnsignedInt](Integer.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `beginIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Parses the [CharSequence](CharSequence.md) argument as an unsigned`int`in the specified`radix`, beginning at the specified`beginIndex`and extending to`endIndex - 1`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parseUnsignedInt](Integer.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Parses the string argument as an unsigned decimal integer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parseUnsignedInt](Integer.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Parses the string argument as an unsigned integer in the radix specified by the second argument. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remainderUnsigned](Integer.md))`(`dividend:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `divisor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the unsigned remainder from dividing the first argument by the second where each argument and the result is interpreted as an unsigned value. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [reverse](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value obtained by reversing the order of the bits in the two's complement binary representation of the specified`int`value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [reverseBytes](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value obtained by reversing the order of the bytes in the two's complement representation of the specified`int`value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [rotateLeft](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `distance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value obtained by rotating the two's complement binary representation of the specified`int`value left by the specified number of bits. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [rotateRight](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `distance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value obtained by rotating the two's complement binary representation of the specified`int`value right by the specified number of bits. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [signum](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the signum function of the specified`int`value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [sum](Integer.md))`(`a:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds two integers together as per the + operator. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toBinaryString](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a string representation of the integer argument as an unsigned integer in base 2. |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [toByte](Integer.md))`()` Returns the value of this`Integer`as a`byte`after a narrowing primitive conversion. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](Integer.md))`()` Returns the value of this`Integer`as a`double`after a widening primitive conversion. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](Integer.md))`()` Returns the value of this`Integer`as a`float`after a widening primitive conversion. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toHexString](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a string representation of the integer argument as an unsigned integer in base 16. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](Integer.md))`()` Returns the value of this`Integer`as an`int`. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](Integer.md))`()` Returns the value of this`Integer`as a`long`after a widening primitive conversion. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toOctalString](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a string representation of the integer argument as an unsigned integer in base 8. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [toShort](Integer.md))`()` Returns the value of this`Integer`as a`short`after a narrowing primitive conversion. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Integer.md))`()` Returns a`String`object representing this`Integer`'s value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`String`object representing the specified integer. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a string representation of the first argument in the radix specified by the second argument. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toUnsignedLong](Integer.md))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Converts the argument to a`long`by an unsigned conversion. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toUnsignedString](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a string representation of the argument as an unsigned decimal value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toUnsignedString](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a string representation of the first argument as an unsigned integer value in the radix specified by the second argument. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [valueOf](Integer.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an`Integer`instance representing the specified`int`value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [valueOf](Integer.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns an`Integer`object holding the value of the specified`String`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [valueOf](Integer.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an`Integer`object holding the value extracted from the specified`String`when parsed with the radix given by the second argument. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Class](Class.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>! | [TYPE](Integer.md) The`Class`instance representing the primitive type`int`. |

## Constants

### BYTES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BYTES: Int
```

The number of bytes used to represent an`int`value in two's complement binary form. 

 Value: 4

### MAX_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_VALUE: Int
```

A constant holding the maximum value an`int`can have, 231-1. 

 Value: 2147483647

### MIN_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_VALUE: Int
```

A constant holding the minimum value an`int`can have, -231. 

 Value: -2147483648

### SIZE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIZE: Int
```

The number of bits used to represent an`int`value in two's complement binary form. 

 Value: 32

## Public constructors

### Integer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Integer(value: Int)
```

**Deprecated:** *It is rarely appropriate to use this constructor. The static factory [valueOf(int)](Integer.md))is generally a better choice, as it is likely to yield significantly better space and time performance.*

Constructs a newly allocated`Integer`object that represents the specified`int`value.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to be represented by the`Integer`object. |

### Integer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Integer(s: String)
```

**Deprecated:** *It is rarely appropriate to use this constructor. Use [parseInt(java.lang.String)](Integer.md))to convert a string to a`int`primitive, or use [valueOf(java.lang.String)](Integer.md))to convert a string to an`Integer`object.*

Constructs a newly allocated`Integer`object that represents the`int`value indicated by the`String`parameter. The string is converted to an`int`value in exactly the manner used by the`parseInt`method for radix 10.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the`String`to be converted to an`Integer`. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------|
| `java.lang.NumberFormatException` | if the`String`does not contain a parsable integer. |

## Public methods

### bitCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun bitCount(i: Int): Int
```

Returns the number of one-bits in the two's complement binary representation of the specified`int`value. This function is sometimes referred to as the*population count*.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value whose bits are to be counted |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of one-bits in the two's complement binary representation of the specified`int`value. |

### compare

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compare(
    x: Int, 
    y: Int
): Int
```

Compares two`int`values numerically. The value returned is identical to what would be returned by: 

```kotlin
Integer.valueOf(x).compareTo(Integer.valueOf(y))
  
```

<br />

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first`int`to compare |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the second`int`to compare |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if`x == y`; a value less than`0`if`x < y`; and a value greater than`0`if`x > y` |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: Int): Int
```

Compares two`Integer`objects numerically.

| Parameters ||
|------------------|-----------------------------|
| `o` | the object to be compared. |
| `anotherInteger` | the`Integer`to be compared. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if this`Integer`is equal to the argument`Integer`; a value less than`0`if this`Integer`is numerically less than the argument`Integer`; and a value greater than`0`if this`Integer`is numerically greater than the argument`Integer`(signed comparison). |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### compareUnsigned

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compareUnsigned(
    x: Int, 
    y: Int
): Int
```

Compares two`int`values numerically treating the values as unsigned.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first`int`to compare |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the second`int`to compare |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if`x == y`; a value less than`0`if`x < y`as unsigned values; and a value greater than`0`if`x > y`as unsigned values |

### compress

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compress(
    i: Int, 
    mask: Int
): Int
```

Returns the value obtained by compressing the bits of the specified`int`value,`i`, in accordance with the specified bit mask.

For each one-bit value`mb`of the mask, from least significant to most significant, the bit value of`i`at the same bit location as`mb`is assigned to the compressed value contiguously starting from the least significant bit location. All the upper remaining bits of the compressed value are set to zero.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value whose bits are to be compressed |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the bit mask |

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the compressed value |

**See Also**

- [#expand](Integer.md)) 

### decode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun decode(nm: String): Int
```

Decodes a`String`into an`Integer`. Accepts decimal, hexadecimal, and octal numbers given by the following grammar:

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

The sequence of characters following an optional sign and/or radix specifier ("`0x`", "`0X`", "", or leading zero) is parsed as by the`Integer.parseInt`method with the indicated radix (10, 16, or 8). This sequence of characters must represent a positive value or a [NumberFormatException](NumberFormatException.md) will be thrown. The result is negated if first character of the specified`String`is the minus sign. No whitespace characters are permitted in the`String`.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------|
| `nm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the`String`to decode. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`Integer`object holding the`int`value represented by`nm` |

| Exceptions ||
|-----------------------------------|----------------------------------------------------|
| `java.lang.NumberFormatException` | if the`String`does not contain a parsable integer. |

**See Also**

- [java.lang.Integer#parseInt(java.lang.String, int)](Integer.md)) 

### divideUnsigned

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun divideUnsigned(
    dividend: Int, 
    divisor: Int
): Int
```

Returns the unsigned quotient of dividing the first argument by the second where each argument and the result is interpreted as an unsigned value.

Note that in two's complement arithmetic, the three other basic arithmetic operations of add, subtract, and multiply are bit-wise identical if the two operands are regarded as both being signed or both being unsigned. Therefore separate`addUnsigned`, etc. methods are not provided.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------|
| `dividend` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to be divided |
| `divisor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value doing the dividing |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the unsigned quotient of the first argument divided by the second argument |

**See Also**

- [#remainderUnsigned](Integer.md)) 

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this object to the specified object. The result is`true`if and only if the argument is not`null`and is an`Integer`object that contains the same`int`value as this object.

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
    i: Int, 
    mask: Int
): Int
```

Returns the value obtained by expanding the bits of the specified`int`value,`i`, in accordance with the specified bit mask.

For each one-bit value`mb`of the mask, from least significant to most significant, the next contiguous bit value of`i`starting at the least significant bit is assigned to the expanded value at the same bit location as`mb`. All other remaining bits of the expanded value are set to zero.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value whose bits are to be expanded |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the bit mask |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the expanded value |

**See Also**

- [#compress](Integer.md)) 

### getInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInteger(nm: String): Int?
```

Determines the integer value of the system property with the specified name.

The first argument is treated as the name of a system property. System properties are accessible through the [java.lang.System#getProperty(java.lang.String)](System.md))method. The string value of this property is then interpreted as an integer value using the grammar supported by [decode](Integer.md))and an`Integer`object representing this value is returned.

If there is no property with the specified name, if the specified name is empty or`null`, or if the property does not have the correct numeric format, then`null`is returned.

In other words, this method returns an`Integer`object equal to the value of:
`getInteger(nm, null)`

| Parameters ||
|------|-------------------------------------------------------------------------------------------------|
| `nm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):property name. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? | the`Integer`value of the property. |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | for the same reasons as [System.getProperty](System.md)) |

**See Also**

- [java.lang.System#getProperty(java.lang.String)](System.md))
- [java.lang.System#getProperty(java.lang.String, java.lang.String)](System.md)) 

### getInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInteger(
    nm: String, 
    val: Int
): Int?
```

Determines the integer value of the system property with the specified name.

The first argument is treated as the name of a system property. System properties are accessible through the [java.lang.System#getProperty(java.lang.String)](System.md))method. The string value of this property is then interpreted as an integer value using the grammar supported by [decode](Integer.md))and an`Integer`object representing this value is returned.

The second argument is the default value. An`Integer`object that represents the value of the second argument is returned if there is no property of the specified name, if the property does not have the correct numeric format, or if the specified name is empty or`null`.

In other words, this method returns an`Integer`object equal to the value of:
`getInteger(nm, Integer.valueOf(val))`but in practice it may be implemented in a manner such as: 

```kotlin
Integer result = getInteger(nm, null);
  return (result == null) ? Integer.valueOf(val) : result;
  
```
to avoid the unnecessary allocation of an`Integer`object when the default value is not needed.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------|
| `nm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):property name. |
| `val` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)?:default value. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? | the`Integer`value of the property. |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | for the same reasons as [System.getProperty](System.md)) |

**See Also**

- [java.lang.System#getProperty(java.lang.String)](System.md))
- [java.lang.System#getProperty(java.lang.String, java.lang.String)](System.md)) 

### getInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInteger(
    nm: String, 
    val: Int?
): Int?
```

Returns the integer value of the system property with the specified name. The first argument is treated as the name of a system property. System properties are accessible through the [java.lang.System#getProperty(java.lang.String)](System.md))method. The string value of this property is then interpreted as an integer value, as per the [decode](Integer.md))method, and an`Integer`object representing this value is returned; in summary:

- If the property value begins with the two ASCII characters`0x`or the ASCII character, not followed by a minus sign, then the rest of it is parsed as a hexadecimal integer exactly as by the method [valueOf(java.lang.String,int)](Integer.md))with radix 16.
- If the property value begins with the ASCII character`0`followed by another character, it is parsed as an octal integer exactly as by the method [valueOf(java.lang.String,int)](Integer.md))with radix 8.
- Otherwise, the property value is parsed as a decimal integer exactly as by the method [valueOf(java.lang.String,int)](Integer.md))with radix 10.

<br />

The second argument is the default value. The default value is returned if there is no property of the specified name, if the property does not have the correct numeric format, or if the specified name is empty or`null`.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------|
| `nm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):property name. |
| `val` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)?:default value. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? | the`Integer`value of the property. |

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

Returns a hash code for this`Integer`.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object, equal to the primitive`int`value represented by this`Integer`object. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun hashCode(value: Int): Int
```

Returns a hash code for an`int`value; compatible with`Integer.hashCode()`.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to hash |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for an`int`value. |

### highestOneBit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun highestOneBit(i: Int): Int
```

Returns an`int`value with at most a single one-bit, in the position of the highest-order ("leftmost") one-bit in the specified`int`value. Returns zero if the specified value has no one-bits in its two's complement binary representation, that is, if it is equal to zero.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value whose highest one bit is to be computed |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`value with a single one-bit, in the position of the highest-order one-bit in the specified value, or zero if the specified value is itself equal to zero. |

### lowestOneBit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun lowestOneBit(i: Int): Int
```

Returns an`int`value with at most a single one-bit, in the position of the lowest-order ("rightmost") one-bit in the specified`int`value. Returns zero if the specified value has no one-bits in its two's complement binary representation, that is, if it is equal to zero.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value whose lowest one bit is to be computed |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`value with a single one-bit, in the position of the lowest-order one-bit in the specified value, or zero if the specified value is itself equal to zero. |

### max

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun max(
    a: Int, 
    b: Int
): Int
```

Returns the greater of two`int`values as if by calling [Math.max](Math.md)).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first operand |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the second operand |

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the greater of`a`and`b` |

**See Also**

- [java.util.function.BinaryOperator](../java.util.function/BinaryOperator.md) 

### min

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun min(
    a: Int, 
    b: Int
): Int
```

Returns the smaller of two`int`values as if by calling [Math.min](Math.md)).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first operand |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the second operand |

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the smaller of`a`and`b` |

**See Also**

- [java.util.function.BinaryOperator](../java.util.function/BinaryOperator.md) 

### numberOfLeadingZeros

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun numberOfLeadingZeros(i: Int): Int
```

Returns the number of zero bits preceding the highest-order ("leftmost") one-bit in the two's complement binary representation of the specified`int`value. Returns 32 if the specified value has no one-bits in its two's complement representation, in other words if it is equal to zero.

Note that this method is closely related to the logarithm base 2. For all positive`int`values x:

- floor(log2(x)) =`31 - numberOfLeadingZeros(x)`
- ceil(log2(x)) =`32 - numberOfLeadingZeros(x - 1)`

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value whose number of leading zeros is to be computed |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of zero bits preceding the highest-order ("leftmost") one-bit in the two's complement binary representation of the specified`int`value, or 32 if the value is equal to zero. |

### numberOfTrailingZeros

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun numberOfTrailingZeros(i: Int): Int
```

Returns the number of zero bits following the lowest-order ("rightmost") one-bit in the two's complement binary representation of the specified`int`value. Returns 32 if the specified value has no one-bits in its two's complement representation, in other words if it is equal to zero.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value whose number of trailing zeros is to be computed |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of zero bits following the lowest-order ("rightmost") one-bit in the two's complement binary representation of the specified`int`value, or 32 if the value is equal to zero. |

### parseInt

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseInt(
    s: CharSequence, 
    beginIndex: Int, 
    endIndex: Int, 
    radix: Int
): Int
```

Parses the [CharSequence](CharSequence.md) argument as a signed`int`in the specified`radix`, beginning at the specified`beginIndex`and extending to`endIndex - 1`.

The method does not take steps to guard against the`CharSequence`being mutated while parsing.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):the`CharSequence`containing the`int`representation to be parsed |
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the beginning index, inclusive. |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the ending index, exclusive. |
| --- | --- |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to be used while parsing`s`. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the signed`int`represented by the subsequence in the specified radix. |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`s`is null. |
| `java.lang.IndexOutOfBoundsException` | if`beginIndex`is negative, or if`beginIndex`is greater than`endIndex`or if`endIndex`is greater than`s.length()`. |
| `java.lang.NumberFormatException` | if the`CharSequence`does not contain a parsable`int`in the specified`radix`, or if`radix`is either smaller than [java.lang.Character#MIN_RADIX](Character.md) or larger than [java.lang.Character#MAX_RADIX](Character.md). |
| --- | --- |

### parseInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseInt(s: String): Int
```

Parses the string argument as a signed decimal integer. The characters in the string must all be decimal digits, except that the first character may be an ASCII minus sign`'-'`(`'\u005Cu002D'`) to indicate a negative value or an ASCII plus sign`'+'`(`'\u005Cu002B'`) to indicate a positive value. The resulting integer value is returned, exactly as if the argument and the radix 10 were given as arguments to the [parseInt(java.lang.String,int)](Integer.md))method.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a`String`containing the`int`representation to be parsed |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the integer value represented by the argument in decimal. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------|
| `java.lang.NumberFormatException` | if the string does not contain a parsable integer. |

### parseInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseInt(
    s: String, 
    radix: Int
): Int
```

Parses the string argument as a signed integer in the radix specified by the second argument. The characters in the string must all be digits of the specified radix (as determined by whether [java.lang.Character#digit(char, int)](Character.md))returns a nonnegative value), except that the first character may be an ASCII minus sign`'-'`(`'\u005Cu002D'`) to indicate a negative value or an ASCII plus sign`'+'`(`'\u005Cu002B'`) to indicate a positive value. The resulting integer value is returned.

An exception of type`NumberFormatException`is thrown if any of the following situations occurs:

- The first argument is`null`or is a string of length zero.
- The radix is either smaller than [java.lang.Character#MIN_RADIX](Character.md) or larger than [java.lang.Character#MAX_RADIX](Character.md).
- Any character of the string is not a digit of the specified radix, except that the first character may be a minus sign`'-'`(`'\u005Cu002D'`) or plus sign`'+'`(`'\u005Cu002B'`) provided that the string is longer than length 1.
- The value represented by the string is not a value of type`int`.

Examples: 

```kotlin
parseInt("0", 10) returns 0
  parseInt("473", 10) returns 473
  parseInt("+42", 10) returns 42
  parseInt("-0", 10) returns 0
  parseInt("-FF", 16) returns -255
  parseInt("1100110", 2) returns 102
  parseInt("2147483647", 10) returns 2147483647
  parseInt("-2147483648", 10) returns -2147483648
  parseInt("2147483648", 10) throws a NumberFormatException
  parseInt("99", 8) throws a NumberFormatException
  parseInt("Kona", 10) throws a NumberFormatException
  parseInt("Kona", 27) returns 411787
  
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the`String`containing the integer representation to be parsed |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to be used while parsing`s`. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the integer represented by the string argument in the specified radix. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------|
| `java.lang.NumberFormatException` | if the`String`does not contain a parsable`int`. |

### parseUnsignedInt

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseUnsignedInt(
    s: CharSequence, 
    beginIndex: Int, 
    endIndex: Int, 
    radix: Int
): Int
```

Parses the [CharSequence](CharSequence.md) argument as an unsigned`int`in the specified`radix`, beginning at the specified`beginIndex`and extending to`endIndex - 1`.

The method does not take steps to guard against the`CharSequence`being mutated while parsing.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):the`CharSequence`containing the unsigned`int`representation to be parsed |
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the beginning index, inclusive. |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the ending index, exclusive. |
| --- | --- |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to be used while parsing`s`. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the unsigned`int`represented by the subsequence in the specified radix. |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`s`is null. |
| `java.lang.IndexOutOfBoundsException` | if`beginIndex`is negative, or if`beginIndex`is greater than`endIndex`or if`endIndex`is greater than`s.length()`. |
| `java.lang.NumberFormatException` | if the`CharSequence`does not contain a parsable unsigned`int`in the specified`radix`, or if`radix`is either smaller than [java.lang.Character#MIN_RADIX](Character.md) or larger than [java.lang.Character#MAX_RADIX](Character.md). |
| --- | --- |

### parseUnsignedInt

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseUnsignedInt(s: String): Int
```

Parses the string argument as an unsigned decimal integer. The characters in the string must all be decimal digits, except that the first character may be an ASCII plus sign`'+'`(`'\u005Cu002B'`). The resulting integer value is returned, exactly as if the argument and the radix 10 were given as arguments to the [parseUnsignedInt(java.lang.String,int)](Integer.md))method.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a`String`containing the unsigned`int`representation to be parsed |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the unsigned integer value represented by the argument in decimal. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------|
| `java.lang.NumberFormatException` | if the string does not contain a parsable unsigned integer. |

### parseUnsignedInt

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseUnsignedInt(
    s: String, 
    radix: Int
): Int
```

Parses the string argument as an unsigned integer in the radix specified by the second argument. An unsigned integer maps the values usually associated with negative numbers to positive numbers larger than`MAX_VALUE`. The characters in the string must all be digits of the specified radix (as determined by whether [java.lang.Character#digit(char, int)](Character.md))returns a nonnegative value), except that the first character may be an ASCII plus sign`'+'`(`'\u005Cu002B'`). The resulting integer value is returned.

An exception of type`NumberFormatException`is thrown if any of the following situations occurs:

- The first argument is`null`or is a string of length zero.
- The radix is either smaller than [java.lang.Character#MIN_RADIX](Character.md) or larger than [java.lang.Character#MAX_RADIX](Character.md).
- Any character of the string is not a digit of the specified radix, except that the first character may be a plus sign`'+'`(`'\u005Cu002B'`) provided that the string is longer than length 1.
- The value represented by the string is larger than the largest unsigned`int`, 232-1.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the`String`containing the unsigned integer representation to be parsed |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to be used while parsing`s`. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the integer represented by the string argument in the specified radix. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------|
| `java.lang.NumberFormatException` | if the`String`does not contain a parsable`int`. |

### remainderUnsigned

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun remainderUnsigned(
    dividend: Int, 
    divisor: Int
): Int
```

Returns the unsigned remainder from dividing the first argument by the second where each argument and the result is interpreted as an unsigned value.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------|
| `dividend` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to be divided |
| `divisor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value doing the dividing |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the unsigned remainder of the first argument divided by the second argument |

**See Also**

- [#divideUnsigned](Integer.md)) 

### reverse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun reverse(i: Int): Int
```

Returns the value obtained by reversing the order of the bits in the two's complement binary representation of the specified`int`value.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to be reversed |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value obtained by reversing order of the bits in the specified`int`value. |

### reverseBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun reverseBytes(i: Int): Int
```

Returns the value obtained by reversing the order of the bytes in the two's complement representation of the specified`int`value.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value whose bytes are to be reversed |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value obtained by reversing the bytes in the specified`int`value. |

### rotateLeft

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun rotateLeft(
    i: Int, 
    distance: Int
): Int
```

Returns the value obtained by rotating the two's complement binary representation of the specified`int`value left by the specified number of bits. (Bits shifted out of the left hand, or high-order, side reenter on the right, or low-order.)

Note that left rotation with a negative distance is equivalent to right rotation:`rotateLeft(val, -distance) == rotateRight(val, distance)`. Note also that rotation by any multiple of 32 is a no-op, so all but the last five bits of the rotation distance can be ignored, even if the distance is negative:`rotateLeft(val, distance) == rotateLeft(val, distance & 0x1F)`.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value whose bits are to be rotated left |
| `distance` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bit positions to rotate left |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value obtained by rotating the two's complement binary representation of the specified`int`value left by the specified number of bits. |

### rotateRight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun rotateRight(
    i: Int, 
    distance: Int
): Int
```

Returns the value obtained by rotating the two's complement binary representation of the specified`int`value right by the specified number of bits. (Bits shifted out of the right hand, or low-order, side reenter on the left, or high-order.)

Note that right rotation with a negative distance is equivalent to left rotation:`rotateRight(val, -distance) == rotateLeft(val, distance)`. Note also that rotation by any multiple of 32 is a no-op, so all but the last five bits of the rotation distance can be ignored, even if the distance is negative:`rotateRight(val, distance) == rotateRight(val, distance & 0x1F)`.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value whose bits are to be rotated right |
| `distance` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bit positions to rotate right |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value obtained by rotating the two's complement binary representation of the specified`int`value right by the specified number of bits. |

### signum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun signum(i: Int): Int
```

Returns the signum function of the specified`int`value. (The return value is -1 if the specified value is negative; 0 if the specified value is zero; and 1 if the specified value is positive.)

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value whose signum is to be computed |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the signum function of the specified`int`value. |

### sum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun sum(
    a: Int, 
    b: Int
): Int
```

Adds two integers together as per the + operator.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first operand |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the second operand |

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the sum of`a`and`b` |

**See Also**

- [java.util.function.BinaryOperator](../java.util.function/BinaryOperator.md) 

### toBinaryString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toBinaryString(i: Int): String
```

Returns a string representation of the integer argument as an unsigned integer in base 2.

The unsigned integer value is the argument plus 232 if the argument is negative; otherwise it is equal to the argument. This value is converted to a string of ASCII digits in binary (base 2) with no extra leading`0`s.

The value of the argument can be recovered from the returned string`s`by calling [Integer.parseUnsignedInt(s, 2)](Integer.md)).

If the unsigned magnitude is zero, it is represented by a single zero character`'0'`(`'\u005Cu0030'`); otherwise, the first character of the representation of the unsigned magnitude will not be the zero character. The characters`'0'`(`'\u005Cu0030'`) and`'1'`(`'\u005Cu0031'`) are used as binary digits.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer to be converted to a string. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of the unsigned integer value represented by the argument in binary (base 2). |

**See Also**

- [#parseUnsignedInt(String, int)](Integer.md))
- [#toUnsignedString(int, int)](Integer.md)) 

### toByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toByte(): Byte
```

Returns the value of this`Integer`as a`byte`after a narrowing primitive conversion.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the numeric value represented by this object after conversion to type`byte`. |

### toDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toDouble(): Double
```

Returns the value of this`Integer`as a`double`after a widening primitive conversion.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the numeric value represented by this object after conversion to type`double`. |

### toFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toFloat(): Float
```

Returns the value of this`Integer`as a`float`after a widening primitive conversion.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the numeric value represented by this object after conversion to type`float`. |

### toHexString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toHexString(i: Int): String
```

Returns a string representation of the integer argument as an unsigned integer in base 16.

The unsigned integer value is the argument plus 232 if the argument is negative; otherwise, it is equal to the argument. This value is converted to a string of ASCII digits in hexadecimal (base 16) with no extra leading`0`s.

The value of the argument can be recovered from the returned string`s`by calling [Integer.parseUnsignedInt(s, 16)](Integer.md)).

If the unsigned magnitude is zero, it is represented by a single zero character`'0'`(`'\u005Cu0030'`); otherwise, the first character of the representation of the unsigned magnitude will not be the zero character. The following characters are used as hexadecimal digits:
`0123456789abcdef`These are the characters`'\u005Cu0030'`through`'\u005Cu0039'`and`'\u005Cu0061'`through`'\u005Cu0066'`. If uppercase letters are desired, the [java.lang.String#toUpperCase()](String.md))method may be called on the result:`Integer.toHexString(n).toUpperCase()`

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer to be converted to a string. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of the unsigned integer value represented by the argument in hexadecimal (base 16). |

**See Also**

- [#parseUnsignedInt(String, int)](Integer.md))
- [#toUnsignedString(int, int)](Integer.md)) 

### toInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toInt(): Int
```

Returns the value of this`Integer`as an`int`.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by this object after conversion to type`int`. |

### toLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toLong(): Long
```

Returns the value of this`Integer`as a`long`after a widening primitive conversion.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the numeric value represented by this object after conversion to type`long`. |

**See Also**

- [java.lang.Integer#toUnsignedLong(int)](Integer.md)) 

### toOctalString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toOctalString(i: Int): String
```

Returns a string representation of the integer argument as an unsigned integer in base 8.

The unsigned integer value is the argument plus 232 if the argument is negative; otherwise, it is equal to the argument. This value is converted to a string of ASCII digits in octal (base 8) with no extra leading`0`s.

The value of the argument can be recovered from the returned string`s`by calling [Integer.parseUnsignedInt(s, 8)](Integer.md)).

If the unsigned magnitude is zero, it is represented by a single zero character`'0'`(`'\u005Cu0030'`); otherwise, the first character of the representation of the unsigned magnitude will not be the zero character. The following characters are used as octal digits:
`01234567`These are the characters`'\u005Cu0030'`through`'\u005Cu0037'`.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer to be converted to a string. |

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of the unsigned integer value represented by the argument in octal (base 8). |

**See Also**

- [#parseUnsignedInt(String, int)](Integer.md))
- [#toUnsignedString(int, int)](Integer.md)) 

### toShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toShort(): Short
```

Returns the value of this`Integer`as a`short`after a narrowing primitive conversion.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the numeric value represented by this object after conversion to type`short`. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a`String`object representing this`Integer`'s value. The value is converted to signed decimal representation and returned as a string, exactly as if the integer value were given as an argument to the [java.lang.Integer#toString(int)](Integer.md))method.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the value of this object in base 10. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toString(i: Int): String
```

Returns a`String`object representing the specified integer. The argument is converted to signed decimal representation and returned as a string, exactly as if the argument and radix 10 were given as arguments to the [toString(int,int)](Integer.md))method.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer to be converted. |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the argument in base 10. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toString(
    i: Int, 
    radix: Int
): String
```

Returns a string representation of the first argument in the radix specified by the second argument.

If the radix is smaller than`Character.MIN_RADIX`or larger than`Character.MAX_RADIX`, then the radix`10`is used instead.

If the first argument is negative, the first element of the result is the ASCII minus character`'-'`(`'\u005Cu002D'`). If the first argument is not negative, no sign character appears in the result.

The remaining characters of the result represent the magnitude of the first argument. If the magnitude is zero, it is represented by a single zero character`'0'`(`'\u005Cu0030'`); otherwise, the first character of the representation of the magnitude will not be the zero character. The following ASCII characters are used as digits:
`0123456789abcdefghijklmnopqrstuvwxyz`These are`'\u005Cu0030'`through`'\u005Cu0039'`and`'\u005Cu0061'`through`'\u005Cu007A'`. If`radix`is N, then the first N of these characters are used as radix-N digits in the order shown. Thus, the digits for hexadecimal (radix 16) are`0123456789abcdef`. If uppercase letters are desired, the [java.lang.String#toUpperCase()](String.md))method may be called on the result:`Integer.toString(n, 16).toUpperCase()`

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer to be converted to a string. |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to use in the string representation. |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the argument in the specified radix. |

**See Also**

- [java.lang.Character#MAX_RADIX](Character.md)
- [java.lang.Character#MIN_RADIX](Character.md) 

### toUnsignedLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUnsignedLong(x: Int): Long
```

Converts the argument to a`long`by an unsigned conversion. In an unsigned conversion to a`long`, the high-order 32 bits of the`long`are zero and the low-order 32 bits are equal to the bits of the integer argument. Consequently, zero and positive`int`values are mapped to a numerically equal`long`value and negative`int`values are mapped to a`long`value equal to the input plus 232.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to convert to an unsigned`long` |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the argument converted to`long`by an unsigned conversion |

### toUnsignedString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUnsignedString(i: Int): String
```

Returns a string representation of the argument as an unsigned decimal value. The argument is converted to unsigned decimal representation and returned as a string exactly as if the argument and radix 10 were given as arguments to the [toUnsignedString(int,int)](Integer.md))method.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer to be converted to an unsigned string. |

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | an unsigned string representation of the argument. |

**See Also**

- [#toUnsignedString(int, int)](Integer.md)) 

### toUnsignedString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUnsignedString(
    i: Int, 
    radix: Int
): String
```

Returns a string representation of the first argument as an unsigned integer value in the radix specified by the second argument.

If the radix is smaller than`Character.MIN_RADIX`or larger than`Character.MAX_RADIX`, then the radix`10`is used instead.

Note that since the first argument is treated as an unsigned value, no leading sign character is printed.

If the magnitude is zero, it is represented by a single zero character`'0'`(`'\u005Cu0030'`); otherwise, the first character of the representation of the magnitude will not be the zero character.

The behavior of radixes and the characters used as digits are the same as [toString](Integer.md)).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer to be converted to an unsigned string. |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to use in the string representation. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | an unsigned string representation of the argument in the specified radix. |

**See Also**

- [#toString(int, int)](Integer.md)) 

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(i: Int): Int
```

Returns an`Integer`instance representing the specified`int`value. If a new`Integer`instance is not required, this method should generally be used in preference to the constructor [Integer(int)](Integer.md)), as this method is likely to yield significantly better space and time performance by caching frequently requested values. This method will always cache values in the range -128 to 127, inclusive, and may cache other values outside of this range.

| Parameters ||
|-----|------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an`int`value. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`Integer`instance representing`i`. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(s: String): Int
```

Returns an`Integer`object holding the value of the specified`String`. The argument is interpreted as representing a signed decimal integer, exactly as if the argument were given to the [parseInt(java.lang.String)](Integer.md))method. The result is an`Integer`object that represents the integer value specified by the string.

In other words, this method returns an`Integer`object equal to the value of:
`Integer.valueOf(Integer.parseInt(s))`

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the string to be parsed. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`Integer`object holding the value represented by the string argument. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------|
| `java.lang.NumberFormatException` | if the string cannot be parsed as an integer. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(
    s: String, 
    radix: Int
): Int
```

Returns an`Integer`object holding the value extracted from the specified`String`when parsed with the radix given by the second argument. The first argument is interpreted as representing a signed integer in the radix specified by the second argument, exactly as if the arguments were given to the [parseInt(java.lang.String,int)](Integer.md))method. The result is an`Integer`object that represents the integer value specified by the string.

In other words, this method returns an`Integer`object equal to the value of:
`Integer.valueOf(Integer.parseInt(s, radix))`

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the string to be parsed. |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to be used in interpreting`s` |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`Integer`object holding the value represented by the string argument in the specified radix. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------|
| `java.lang.NumberFormatException` | if the`String`does not contain a parsable`int`. |

## Properties

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE: Class<Int!>!
```

The`Class`instance representing the primitive type`int`.
