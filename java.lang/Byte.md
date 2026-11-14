# Byte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Byte

```
class Byte : Number, Comparable<Byte!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.lang.Byte](https://developer.android.com/reference/kotlin/java/lang/Byte#) |

The`Byte`class wraps a value of primitive type`byte`in an object. An object of type`Byte`contains a single field whose type is`byte`.

In addition, this class provides several methods for converting a`byte`to a`String`and a`String`to a`byte`, as well as other constants and methods useful when dealing with a`byte`.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BYTES](https://developer.android.com/reference/kotlin/java/lang/Byte#BYTES:kotlin.Int) The number of bytes used to represent a`byte`value in two's complement binary form. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Byte#MAX_VALUE:kotlin.Byte) A constant holding the maximum value a`byte`can have, 27-1. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [MIN_VALUE](https://developer.android.com/reference/kotlin/java/lang/Byte#MIN_VALUE:kotlin.Byte) A constant holding the minimum value a`byte`can have, -27. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIZE](https://developer.android.com/reference/kotlin/java/lang/Byte#SIZE:kotlin.Int) The number of bits used to represent a`byte`value in two's complement binary form. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Byte](https://developer.android.com/reference/kotlin/java/lang/Byte#Byte(kotlin.Byte))`(`value:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Constructs a newly allocated`Byte`object that represents the specified`byte`value. |
| [Byte](https://developer.android.com/reference/kotlin/java/lang/Byte#Byte(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a newly allocated`Byte`object that represents the`byte`value indicated by the`String`parameter. |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](https://developer.android.com/reference/kotlin/java/lang/Byte#compare(kotlin.Byte,%20kotlin.Byte))`(`x:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`, `y:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Compares two`byte`values numerically. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/lang/Byte#compareTo(kotlin.Byte))`(`other:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Compares two`Byte`objects numerically. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareUnsigned](https://developer.android.com/reference/kotlin/java/lang/Byte#compareUnsigned(kotlin.Byte,%20kotlin.Byte))`(`x:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`, `y:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Compares two`byte`values numerically treating the values as unsigned. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [decode](https://developer.android.com/reference/kotlin/java/lang/Byte#decode(kotlin.String))`(`nm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Decodes a`String`into a`Byte`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/lang/Byte#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this object to the specified object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/lang/Byte#hashCode())`()` Returns a hash code for this`Byte`; equal to the result of invoking`intValue()`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/lang/Byte#hashCode(kotlin.Byte))`(`value:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Returns a hash code for a`byte`value; compatible with`Byte.hashCode()`. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [parseByte](https://developer.android.com/reference/kotlin/java/lang/Byte#parseByte(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Parses the string argument as a signed decimal`byte`. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [parseByte](https://developer.android.com/reference/kotlin/java/lang/Byte#parseByte(kotlin.String,%20kotlin.Int))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Parses the string argument as a signed`byte`in the radix specified by the second argument. |
| --- | --- |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [toByte](https://developer.android.com/reference/kotlin/java/lang/Byte#toByte())`()` Returns the value of this`Byte`as a`byte`. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](https://developer.android.com/reference/kotlin/java/lang/Byte#toDouble())`()` Returns the value of this`Byte`as a`double`after a widening primitive conversion. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](https://developer.android.com/reference/kotlin/java/lang/Byte#toFloat())`()` Returns the value of this`Byte`as a`float`after a widening primitive conversion. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](https://developer.android.com/reference/kotlin/java/lang/Byte#toInt())`()` Returns the value of this`Byte`as an`int`after a widening primitive conversion. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](https://developer.android.com/reference/kotlin/java/lang/Byte#toLong())`()` Returns the value of this`Byte`as a`long`after a widening primitive conversion. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [toShort](https://developer.android.com/reference/kotlin/java/lang/Byte#toShort())`()` Returns the value of this`Byte`as a`short`after a widening primitive conversion. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/lang/Byte#toString())`()` Returns a`String`object representing this`Byte`'s value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/lang/Byte#toString(kotlin.Byte))`(`b:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Returns a new`String`object representing the specified`byte`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toUnsignedInt](https://developer.android.com/reference/kotlin/java/lang/Byte#toUnsignedInt(kotlin.Byte))`(`x:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Converts the argument to an`int`by an unsigned conversion. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toUnsignedLong](https://developer.android.com/reference/kotlin/java/lang/Byte#toUnsignedLong(kotlin.Byte))`(`x:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Converts the argument to a`long`by an unsigned conversion. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [valueOf](https://developer.android.com/reference/kotlin/java/lang/Byte#valueOf(kotlin.Byte))`(`b:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Returns a`Byte`instance representing the specified`byte`value. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [valueOf](https://developer.android.com/reference/kotlin/java/lang/Byte#valueOf(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns a`Byte`object holding the value given by the specified`String`. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [valueOf](https://developer.android.com/reference/kotlin/java/lang/Byte#valueOf(kotlin.String,%20kotlin.Int))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`Byte`object holding the value extracted from the specified`String`when parsed with the radix given by the second argument. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Class](https://developer.android.com/reference/kotlin/java/lang/Class)\< [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)!\>! | [TYPE](https://developer.android.com/reference/kotlin/java/lang/Byte#TYPE:java.lang.Class) The`Class`instance representing the primitive type`byte`. |

## Constants

### BYTES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BYTES: Int
```

The number of bytes used to represent a`byte`value in two's complement binary form. 

 Value: 1

### MAX_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_VALUE: Byte
```

A constant holding the maximum value a`byte`can have, 27-1. 

 Value: 127

### MIN_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_VALUE: Byte
```

A constant holding the minimum value a`byte`can have, -27. 

 Value: -128

### SIZE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIZE: Int
```

The number of bits used to represent a`byte`value in two's complement binary form. 

 Value: 8

## Public constructors

### Byte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Byte(value: Byte)
```

**Deprecated:** *It is rarely appropriate to use this constructor. The static factory [valueOf(byte)](https://developer.android.com/reference/kotlin/java/lang/Byte#valueOf(kotlin.Byte))is generally a better choice, as it is likely to yield significantly better space and time performance.*

Constructs a newly allocated`Byte`object that represents the specified`byte`value.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `value` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the value to be represented by the`Byte`. |

### Byte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Byte(s: String)
```

**Deprecated:** *It is rarely appropriate to use this constructor. Use [parseByte(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/Byte#parseByte(kotlin.String))to convert a string to a`byte`primitive, or use [valueOf(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/Byte#valueOf(kotlin.String))to convert a string to a`Byte`object.*

Constructs a newly allocated`Byte`object that represents the`byte`value indicated by the`String`parameter. The string is converted to a`byte`value in exactly the manner used by the`parseByte`method for radix 10.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the`String`to be converted to a`Byte` |

| Exceptions ||
|-----------------------------------|--------------------------------------------------|
| `java.lang.NumberFormatException` | if the`String`does not contain a parsable`byte`. |

## Public methods

### compare

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compare(
    x: Byte, 
    y: Byte
): Int
```

Compares two`byte`values numerically. The value returned is identical to what would be returned by: 

```kotlin
Byte.valueOf(x).compareTo(Byte.valueOf(y))
  
```

<br />

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------|
| `x` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the first`byte`to compare |
| `y` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the second`byte`to compare |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if`x == y`; a value less than`0`if`x < y`; and a value greater than`0`if`x > y` |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: Byte): Int
```

Compares two`Byte`objects numerically.

| Parameters ||
|---------------|----------------------------|
| `o` | the object to be compared. |
| `anotherByte` | the`Byte`to be compared. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if this`Byte`is equal to the argument`Byte`; a value less than`0`if this`Byte`is numerically less than the argument`Byte`; and a value greater than`0`if this`Byte`is numerically greater than the argument`Byte`(signed comparison). |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### compareUnsigned

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compareUnsigned(
    x: Byte, 
    y: Byte
): Int
```

Compares two`byte`values numerically treating the values as unsigned.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------|
| `x` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the first`byte`to compare |
| `y` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the second`byte`to compare |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if`x == y`; a value less than`0`if`x < y`as unsigned values; and a value greater than`0`if`x > y`as unsigned values |

### decode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun decode(nm: String): Byte
```

Decodes a`String`into a`Byte`. Accepts decimal, hexadecimal, and octal numbers given by the following grammar:

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

The sequence of characters following an optional sign and/or radix specifier ("`0x`", "`0X`", "", or leading zero) is parsed as by the`Byte.parseByte`method with the indicated radix (10, 16, or 8). This sequence of characters must represent a positive value or a [NumberFormatException](https://developer.android.com/reference/kotlin/java/lang/NumberFormatException) will be thrown. The result is negated if first character of the specified`String`is the minus sign. No whitespace characters are permitted in the`String`.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------|
| `nm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the`String`to decode. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | a`Byte`object holding the`byte`value represented by`nm` |

| Exceptions ||
|-----------------------------------|--------------------------------------------------|
| `java.lang.NumberFormatException` | if the`String`does not contain a parsable`byte`. |

**See Also**

- [java.lang.Byte#parseByte(java.lang.String, int)](https://developer.android.com/reference/kotlin/java/lang/Byte#parseByte(kotlin.String,%20kotlin.Int)) 

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this object to the specified object. The result is`true`if and only if the argument is not`null`and is a`Byte`object that contains the same`byte`value as this object.

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

Returns a hash code for this`Byte`; equal to the result of invoking`intValue()`.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this`Byte` |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun hashCode(value: Byte): Int
```

Returns a hash code for a`byte`value; compatible with`Byte.hashCode()`.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------|
| `value` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the value to hash |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for a`byte`value. |

### parseByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseByte(s: String): Byte
```

Parses the string argument as a signed decimal`byte`. The characters in the string must all be decimal digits, except that the first character may be an ASCII minus sign`'-'`(`'\u005Cu002D'`) to indicate a negative value or an ASCII plus sign`'+'`(`'\u005Cu002B'`) to indicate a positive value. The resulting`byte`value is returned, exactly as if the argument and the radix 10 were given as arguments to the [parseByte(java.lang.String,int)](https://developer.android.com/reference/kotlin/java/lang/Byte#parseByte(kotlin.String,%20kotlin.Int))method.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a`String`containing the`byte`representation to be parsed |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the`byte`value represented by the argument in decimal |

| Exceptions ||
|-----------------------------------|--------------------------------------------------|
| `java.lang.NumberFormatException` | if the string does not contain a parsable`byte`. |

### parseByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseByte(
    s: String, 
    radix: Int
): Byte
```

Parses the string argument as a signed`byte`in the radix specified by the second argument. The characters in the string must all be digits, of the specified radix (as determined by whether [java.lang.Character#digit(char, * int)](https://developer.android.com/reference/kotlin/java/lang/Character#digit(kotlin.Char,%20kotlin.Int))returns a nonnegative value) except that the first character may be an ASCII minus sign`'-'`(`'\u005Cu002D'`) to indicate a negative value or an ASCII plus sign`'+'`(`'\u005Cu002B'`) to indicate a positive value. The resulting`byte`value is returned.

An exception of type`NumberFormatException`is thrown if any of the following situations occurs:

- The first argument is`null`or is a string of length zero.
- The radix is either smaller than [java.lang.Character#MIN_RADIX](https://developer.android.com/reference/kotlin/java/lang/Character#MIN_RADIX:kotlin.Int) or larger than [java.lang.Character#MAX_RADIX](https://developer.android.com/reference/kotlin/java/lang/Character#MAX_RADIX:kotlin.Int).
- Any character of the string is not a digit of the specified radix, except that the first character may be a minus sign`'-'`(`'\u005Cu002D'`) or plus sign`'+'`(`'\u005Cu002B'`) provided that the string is longer than length 1.
- The value represented by the string is not a value of type`byte`.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the`String`containing the`byte`representation to be parsed |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to be used while parsing`s` |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the`byte`value represented by the string argument in the specified radix |

| Exceptions ||
|-----------------------------------|--------------------------------------------------|
| `java.lang.NumberFormatException` | If the string does not contain a parsable`byte`. |

### toByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toByte(): Byte
```

Returns the value of this`Byte`as a`byte`.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the numeric value represented by this object after conversion to type`byte`. |

### toDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toDouble(): Double
```

Returns the value of this`Byte`as a`double`after a widening primitive conversion.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the numeric value represented by this object after conversion to type`double`. |

### toFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toFloat(): Float
```

Returns the value of this`Byte`as a`float`after a widening primitive conversion.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the numeric value represented by this object after conversion to type`float`. |

### toInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toInt(): Int
```

Returns the value of this`Byte`as an`int`after a widening primitive conversion.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by this object after conversion to type`int`. |

### toLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toLong(): Long
```

Returns the value of this`Byte`as a`long`after a widening primitive conversion.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the numeric value represented by this object after conversion to type`long`. |

### toShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toShort(): Short
```

Returns the value of this`Byte`as a`short`after a widening primitive conversion.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the numeric value represented by this object after conversion to type`short`. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a`String`object representing this`Byte`'s value. The value is converted to signed decimal representation and returned as a string, exactly as if the`byte`value were given as an argument to the [java.lang.Byte#toString(byte)](https://developer.android.com/reference/kotlin/java/lang/Byte#toString(kotlin.Byte))method.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the value of this object in base 10. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toString(b: Byte): String
```

Returns a new`String`object representing the specified`byte`. The radix is assumed to be 10.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `b` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the`byte`to be converted |

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of the specified`byte` |

**See Also**

- [java.lang.Integer#toString(int)](https://developer.android.com/reference/kotlin/java/lang/Integer#toString(kotlin.Int)) 

### toUnsignedInt

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUnsignedInt(x: Byte): Int
```

Converts the argument to an`int`by an unsigned conversion. In an unsigned conversion to an`int`, the high-order 24 bits of the`int`are zero and the low-order 8 bits are equal to the bits of the`byte`argument. Consequently, zero and positive`byte`values are mapped to a numerically equal`int`value and negative`byte`values are mapped to an`int`value equal to the input plus 28.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------|
| `x` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the value to convert to an unsigned`int` |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the argument converted to`int`by an unsigned conversion |

### toUnsignedLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUnsignedLong(x: Byte): Long
```

Converts the argument to a`long`by an unsigned conversion. In an unsigned conversion to a`long`, the high-order 56 bits of the`long`are zero and the low-order 8 bits are equal to the bits of the`byte`argument. Consequently, zero and positive`byte`values are mapped to a numerically equal`long`value and negative`byte`values are mapped to a`long`value equal to the input plus 28.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------|
| `x` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the value to convert to an unsigned`long` |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the argument converted to`long`by an unsigned conversion |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(b: Byte): Byte
```

Returns a`Byte`instance representing the specified`byte`value. If a new`Byte`instance is not required, this method should generally be used in preference to the constructor [Byte(byte)](https://developer.android.com/reference/kotlin/java/lang/Byte#Byte(kotlin.Byte)), as this method is likely to yield significantly better space and time performance since all byte values are cached.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------|
| `b` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):a byte value. |

| Return ||
|------------------------------------------------------------------------------|----------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | a`Byte`instance representing`b`. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(s: String): Byte
```

Returns a`Byte`object holding the value given by the specified`String`. The argument is interpreted as representing a signed decimal`byte`, exactly as if the argument were given to the [parseByte(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/Byte#parseByte(kotlin.String))method. The result is a`Byte`object that represents the`byte`value specified by the string.

In other words, this method returns a`Byte`object equal to the value of:
`new Byte(Byte.parseByte(s))`

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the string to be parsed |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | a`Byte`object holding the value represented by the string argument |

| Exceptions ||
|-----------------------------------|--------------------------------------------------|
| `java.lang.NumberFormatException` | If the`String`does not contain a parsable`byte`. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(
    s: String, 
    radix: Int
): Byte
```

Returns a`Byte`object holding the value extracted from the specified`String`when parsed with the radix given by the second argument. The first argument is interpreted as representing a signed`byte`in the radix specified by the second argument, exactly as if the argument were given to the [parseByte(java.lang.String,int)](https://developer.android.com/reference/kotlin/java/lang/Byte#parseByte(kotlin.String,%20kotlin.Int))method. The result is a`Byte`object that represents the`byte`value specified by the string.

In other words, this method returns a`Byte`object equal to the value of:
`new Byte(Byte.parseByte(s, radix))`

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the string to be parsed |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix to be used in interpreting`s` |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | a`Byte`object holding the value represented by the string argument in the specified radix. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------|
| `java.lang.NumberFormatException` | If the`String`does not contain a parsable`byte`. |

## Properties

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE: Class<Byte!>!
```

The`Class`instance representing the primitive type`byte`.
