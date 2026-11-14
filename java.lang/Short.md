# Short

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Short

```
class Short : Number, Comparable<Short!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.lang.Short](../java/lang/Short.md) |

The`Short`class wraps a value of primitive type`short`in an object. An object of type`Short`contains a single field whose type is`short`.

In addition, this class provides several methods for converting a`short`to a`String`and a`String`to a`short`, as well as other constants and methods useful when dealing with a`short`.

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BYTES](../java/lang/Short.md) The number of bytes used to represent a`short`value in two's complement binary form. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [MAX_VALUE](../java/lang/Short.md) A constant holding the maximum value a`short`can have, 215-1. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [MIN_VALUE](../java/lang/Short.md) A constant holding the minimum value a`short`can have, -215. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIZE](../java/lang/Short.md) The number of bits used to represent a`short`value in two's complement binary form. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Short](../java/lang/Short.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a newly allocated`Short`object that represents the`short`value indicated by the`String`parameter. |
| [Short](../java/lang/Short.md))`(`value:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Constructs a newly allocated`Short`object that represents the specified`short`value. |

| Public methods ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](../java/lang/Short.md))`(`x:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `y:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Compares two`short`values numerically. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](../java/lang/Short.md))`(`other:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)!`)` Compares two`Short`objects numerically. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareUnsigned](../java/lang/Short.md))`(`x:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `y:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Compares two`short`values numerically treating the values as unsigned. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)! | [decode](../java/lang/Short.md))`(`nm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Decodes a`String`into a`Short`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/lang/Short.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this object to the specified object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/lang/Short.md))`()` Returns a hash code for this`Short`; equal to the result of invoking`intValue()`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/lang/Short.md))`(`value:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Returns a hash code for a`short`value; compatible with`Short.hashCode()`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [parseShort](../java/lang/Short.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses the string argument as a signed decimal`short`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [parseShort](../java/lang/Short.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Parses the string argument as a signed`short`in the radix specified by the second argument. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [reverseBytes](../java/lang/Short.md))`(`i:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Returns the value obtained by reversing the order of the bytes in the two's complement representation of the specified`short`value. |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [toByte](../java/lang/Short.md))`()` Returns the value of this`Short`as a`byte`after a narrowing primitive conversion. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](../java/lang/Short.md))`()` Returns the value of this`Short`as a`double`after a widening primitive conversion. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](../java/lang/Short.md))`()` Returns the value of this`Short`as a`float`after a widening primitive conversion. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](../java/lang/Short.md))`()` Returns the value of this`Short`as an`int`after a widening primitive conversion. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](../java/lang/Short.md))`()` Returns the value of this`Short`as a`long`after a widening primitive conversion. |
| --- | --- |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [toShort](../java/lang/Short.md))`()` Returns the value of this`Short`as a`short`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/lang/Short.md))`()` Returns a`String`object representing this`Short`'s value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](../java/lang/Short.md))`(`s:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Returns a new`String`object representing the specified`short`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toUnsignedInt](../java/lang/Short.md))`(`x:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Converts the argument to an`int`by an unsigned conversion. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toUnsignedLong](../java/lang/Short.md))`(`x:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Converts the argument to a`long`by an unsigned conversion. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)! | [valueOf](../java/lang/Short.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`Short`object holding the value given by the specified`String`. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)! | [valueOf](../java/lang/Short.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`Short`object holding the value extracted from the specified`String`when parsed with the radix given by the second argument. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)! | [valueOf](../java/lang/Short.md))`(`s:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Returns a`Short`instance representing the specified`short`value. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Class](../java/lang/Class.md)\< [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)!\>! | [TYPE](../java/lang/Short.md) The`Class`instance representing the primitive type`short`. |

## Constants

### BYTES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BYTES: Int
```

The number of bytes used to represent a`short`value in two's complement binary form. 

 Value: 2

### MAX_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_VALUE: Short
```

A constant holding the maximum value a`short`can have, 215-1. 

 Value: 32767

### MIN_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_VALUE: Short
```

A constant holding the minimum value a`short`can have, -215. 

 Value: -32768

### SIZE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIZE: Int
```

The number of bits used to represent a`short`value in two's complement binary form. 

 Value: 16

## Public constructors

### Short

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Short(s: String!)
```

**Deprecated:** *It is rarely appropriate to use this constructor. Use [parseShort(java.lang.String)](../java/lang/Short.md))to convert a string to a`short`primitive, or use [valueOf(java.lang.String)](../java/lang/Short.md))to convert a string to a`Short`object.*

Constructs a newly allocated`Short`object that represents the`short`value indicated by the`String`parameter. The string is converted to a`short`value in exactly the manner used by the`parseShort`method for radix 10.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the`String`to be converted to a`Short` |

| Exceptions ||
|-----------------------------------|---------------------------------------------------|
| `java.lang.NumberFormatException` | If the`String`does not contain a parsable`short`. |

### Short

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Short(value: Short)
```

**Deprecated:** *It is rarely appropriate to use this constructor. The static factory [valueOf(short)](../java/lang/Short.md))is generally a better choice, as it is likely to yield significantly better space and time performance.*

Constructs a newly allocated`Short`object that represents the specified`short`value.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `value` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the value to be represented by the`Short`. |

## Public methods

### compare

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compare(
    x: Short, 
    y: Short
): Int
```

Compares two`short`values numerically. The value returned is identical to what would be returned by: 

```kotlin
Short.valueOf(x).compareTo(Short.valueOf(y))
  
```

<br />

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------|
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the first`short`to compare |
| `y` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the second`short`to compare |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if`x == y`; a value less than`0`if`x < y`; and a value greater than`0`if`x > y` |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: Short!): Int
```

Compares two`Short`objects numerically.

| Parameters ||
|----------------|----------------------------|
| `o` | the object to be compared. |
| `anotherShort` | the`Short`to be compared. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if this`Short`is equal to the argument`Short`; a value less than`0`if this`Short`is numerically less than the argument`Short`; and a value greater than`0`if this`Short`is numerically greater than the argument`Short`(signed comparison). |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### compareUnsigned

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compareUnsigned(
    x: Short, 
    y: Short
): Int
```

Compares two`short`values numerically treating the values as unsigned.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------|
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the first`short`to compare |
| `y` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the second`short`to compare |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if`x == y`; a value less than`0`if`x < y`as unsigned values; and a value greater than`0`if`x > y`as unsigned values |

### decode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun decode(nm: String!): Short!
```

Decodes a`String`into a`Short`. Accepts decimal, hexadecimal, and octal numbers given by the following grammar:

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

The sequence of characters following an optional sign and/or radix specifier ("`0x`", "`0X`", "", or leading zero) is parsed as by the`Short.parseShort`method with the indicated radix (10, 16, or 8). This sequence of characters must represent a positive value or a [NumberFormatException](../java/lang/NumberFormatException.md) will be thrown. The result is negated if first character of the specified`String`is the minus sign. No whitespace characters are permitted in the`String`.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------|
| `nm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the`String`to decode. |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)! | a`Short`object holding the`short`value represented by`nm` |

| Exceptions ||
|-----------------------------------|---------------------------------------------------|
| `java.lang.NumberFormatException` | if the`String`does not contain a parsable`short`. |

**See Also**

- [java.lang.Short#parseShort(java.lang.String, int)](../java/lang/Short.md)) 

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this object to the specified object. The result is`true`if and only if the argument is not`null`and is a`Short`object that contains the same`short`value as this object.

| Parameters ||
|-------|----------------------------|
| `obj` | the object to compare with |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects are the same;`false`otherwise. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code for this`Short`; equal to the result of invoking`intValue()`.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this`Short` |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun hashCode(value: Short): Int
```

Returns a hash code for a`short`value; compatible with`Short.hashCode()`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `value` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the value to hash |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for a`short`value. |

### parseShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseShort(s: String!): Short
```

Parses the string argument as a signed decimal`short`. The characters in the string must all be decimal digits, except that the first character may be an ASCII minus sign`'-'`(`'\u005Cu002D'`) to indicate a negative value or an ASCII plus sign`'+'`(`'\u005Cu002B'`) to indicate a positive value. The resulting`short`value is returned, exactly as if the argument and the radix 10 were given as arguments to the [parseShort(java.lang.String,int)](../java/lang/Short.md))method.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`containing the`short`representation to be parsed |

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the`short`value represented by the argument in decimal. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------|
| `java.lang.NumberFormatException` | If the string does not contain a parsable`short`. |

### parseShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseShort(
    s: String!, 
    radix: Int
): Short
```

Parses the string argument as a signed`short`in the radix specified by the second argument. The characters in the string must all be digits, of the specified radix (as determined by whether [java.lang.Character#digit(char, * int)](../java/lang/Character.md))returns a nonnegative value) except that the first character may be an ASCII minus sign`'-'`(`'\u005Cu002D'`) to indicate a negative value or an ASCII plus sign`'+'`(`'\u005Cu002B'`) to indicate a positive value. The resulting`short`value is returned.

An exception of type`NumberFormatException`is thrown if any of the following situations occurs:

- The first argument is`null`or is a string of length zero.
- The radix is either smaller than [java.lang.Character#MIN_RADIX](../java/lang/Character.md) or larger than [java.lang.Character#MAX_RADIX](../java/lang/Character.md).
- Any character of the string is not a digit of the specified radix, except that the first character may be a minus sign`'-'`(`'\u005Cu002D'`) or plus sign`'+'`(`'\u005Cu002B'`) provided that the string is longer than length 1.
- The value represented by the string is not a value of type`short`.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the`String`containing the`short`representation to be parsed |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to be used while parsing`s` |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the`short`represented by the string argument in the specified radix. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------|
| `java.lang.NumberFormatException` | If the`String`does not contain a parsable`short`. |

### reverseBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun reverseBytes(i: Short): Short
```

Returns the value obtained by reversing the order of the bytes in the two's complement representation of the specified`short`value.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------|
| `i` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the value whose bytes are to be reversed |

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the value obtained by reversing (or, equivalently, swapping) the bytes in the specified`short`value. |

### toByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toByte(): Byte
```

Returns the value of this`Short`as a`byte`after a narrowing primitive conversion.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the numeric value represented by this object after conversion to type`byte`. |

### toDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toDouble(): Double
```

Returns the value of this`Short`as a`double`after a widening primitive conversion.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the numeric value represented by this object after conversion to type`double`. |

### toFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toFloat(): Float
```

Returns the value of this`Short`as a`float`after a widening primitive conversion.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the numeric value represented by this object after conversion to type`float`. |

### toInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toInt(): Int
```

Returns the value of this`Short`as an`int`after a widening primitive conversion.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by this object after conversion to type`int`. |

### toLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toLong(): Long
```

Returns the value of this`Short`as a`long`after a widening primitive conversion.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the numeric value represented by this object after conversion to type`long`. |

### toShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toShort(): Short
```

Returns the value of this`Short`as a`short`.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the numeric value represented by this object after conversion to type`short`. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a`String`object representing this`Short`'s value. The value is converted to signed decimal representation and returned as a string, exactly as if the`short`value were given as an argument to the [java.lang.Short#toString(short)](../java/lang/Short.md))method.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the value of this object in base 10. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toString(s: Short): String!
```

Returns a new`String`object representing the specified`short`. The radix is assumed to be 10.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `s` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the`short`to be converted |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the string representation of the specified`short` |

**See Also**

- [java.lang.Integer#toString(int)](../java/lang/Integer.md)) 

### toUnsignedInt

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUnsignedInt(x: Short): Int
```

Converts the argument to an`int`by an unsigned conversion. In an unsigned conversion to an`int`, the high-order 16 bits of the`int`are zero and the low-order 16 bits are equal to the bits of the`short`argument. Consequently, zero and positive`short`values are mapped to a numerically equal`int`value and negative`short`values are mapped to an`int`value equal to the input plus 216.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------|
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the value to convert to an unsigned`int` |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the argument converted to`int`by an unsigned conversion |

### toUnsignedLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUnsignedLong(x: Short): Long
```

Converts the argument to a`long`by an unsigned conversion. In an unsigned conversion to a`long`, the high-order 48 bits of the`long`are zero and the low-order 16 bits are equal to the bits of the`short`argument. Consequently, zero and positive`short`values are mapped to a numerically equal`long`value and negative`short`values are mapped to a`long`value equal to the input plus 216.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------|
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the value to convert to an unsigned`long` |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the argument converted to`long`by an unsigned conversion |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(s: String!): Short!
```

Returns a`Short`object holding the value given by the specified`String`. The argument is interpreted as representing a signed decimal`short`, exactly as if the argument were given to the [parseShort(java.lang.String)](../java/lang/Short.md))method. The result is a`Short`object that represents the`short`value specified by the string.

In other words, this method returns a`Short`object equal to the value of:
`new Short(Short.parseShort(s))`

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to be parsed |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)! | a`Short`object holding the value represented by the string argument |

| Exceptions ||
|-----------------------------------|---------------------------------------------------|
| `java.lang.NumberFormatException` | If the`String`does not contain a parsable`short`. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(
    s: String!, 
    radix: Int
): Short!
```

Returns a`Short`object holding the value extracted from the specified`String`when parsed with the radix given by the second argument. The first argument is interpreted as representing a signed`short`in the radix specified by the second argument, exactly as if the argument were given to the [parseShort(java.lang.String,int)](../java/lang/Short.md))method. The result is a`Short`object that represents the`short`value specified by the string.

In other words, this method returns a`Short`object equal to the value of:
`new Short(Short.parseShort(s, radix))`

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to be parsed |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to be used in interpreting`s` |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)! | a`Short`object holding the value represented by the string argument in the specified radix. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------|
| `java.lang.NumberFormatException` | If the`String`does not contain a parsable`short`. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(s: Short): Short!
```

Returns a`Short`instance representing the specified`short`value. If a new`Short`instance is not required, this method should generally be used in preference to the constructor [Short(short)](../java/lang/Short.md)), as this method is likely to yield significantly better space and time performance by caching frequently requested values. This method will always cache values in the range -128 to 127, inclusive, and may cache other values outside of this range.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------|
| `s` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):a short value. |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)! | a`Short`instance representing`s`. |

## Properties

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE: Class<Short!>!
```

The`Class`instance representing the primitive type`short`.
