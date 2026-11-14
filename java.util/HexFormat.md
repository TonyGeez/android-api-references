# HexFormat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HexFormat

```
class HexFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.HexFormat](HexFormat.md) |

`HexFormat`converts between bytes and chars and hex-encoded strings which may include additional formatting markup such as prefixes, suffixes, and delimiters.

There are two factories of`HexFormat`with preset parameters [of()](HexFormat.md))and [ofDelimiter(delimiter)](HexFormat.md)). For other parameter combinations the`withXXX`methods return copies of`HexFormat`modified [withPrefix(java.lang.String)](HexFormat.md)), [withSuffix(java.lang.String)](HexFormat.md)), [withDelimiter(java.lang.String)](HexFormat.md))or choice of [withUpperCase()](HexFormat.md))or [withLowerCase()](HexFormat.md))parameters.

For primitive to hexadecimal string conversions the`toHexDigits`methods include [toHexDigits(byte)](HexFormat.md)), [toHexDigits(int)](HexFormat.md)), and [toHexDigits(long)](HexFormat.md)), etc. The default is to use lowercase characters`"0-9","a-f"`. For conversions producing uppercase hexadecimal the characters are`"0-9","A-F"`. Only the [HexFormat.isUpperCase()](HexFormat.md))parameter is considered; the delimiter, prefix and suffix are not used.

For hexadecimal string to primitive conversions the`fromHexDigits`methods include [fromHexDigits(string)](HexFormat.md)), [fromHexDigitsToLong(string)](HexFormat.md)), and [fromHexDigit(int)](HexFormat.md))converts a single character or codepoint. For conversions from hexadecimal characters the digits and uppercase and lowercase characters in`"0-9", "a-f", and "A-F"`are converted to corresponding values`0-15`. The delimiter, prefix, suffix, and uppercase parameters are not used.

For byte array to formatted hexadecimal string conversions the`formatHex`methods include[formatHex(byte[])](https://developer.android.com/reference/kotlin/java/util/HexFormat#formatHex(kotlin.ByteArray))and[formatHex(Appendable, byte[])](https://developer.android.com/reference/kotlin/java/util/HexFormat#formatHex(java.util.HexFormat.formatHex.A,%20kotlin.ByteArray)). The formatted output is a string or is appended to an [Appendable](../java.lang/Appendable.md) such as [StringBuilder](../java.lang/StringBuilder.md) or [java.io.PrintStream](../java.io/PrintStream.md). Each byte value is formatted as the prefix, two hexadecimal characters from the uppercase or lowercase digits, and the suffix. A delimiter follows each formatted value, except the last. For conversions producing uppercase hexadecimal strings use [withUpperCase()](HexFormat.md)).

For formatted hexadecimal string to byte array conversions the`parseHex`methods include [parseHex(CharSequence)](HexFormat.md))and[parseHex(char[], offset, length)](https://developer.android.com/reference/kotlin/java/util/HexFormat#parseHex(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)). Each byte value is parsed from the prefix, two case insensitive hexadecimal characters, and the suffix. A delimiter follows each formatted value, except the last.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [delimiter](HexFormat.md))`()` Returns the delimiter between hexadecimal values in formatted hexadecimal strings. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](HexFormat.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns`true`if the other object is a`HexFormat`with the same parameters. |
| A | [formatHex](HexFormat.md))`(`out:` `A`, `bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Appends formatted hexadecimal strings from a byte array to the [Appendable](../java.lang/Appendable.md). |
| --- | --- |
| A | [formatHex](HexFormat.md))`(`out:` `A`, `bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Appends formatted hexadecimal strings from a byte array range to the [Appendable](../java.lang/Appendable.md). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatHex](HexFormat.md))`(`bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Returns a hexadecimal string formatted from a byte array. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatHex](HexFormat.md))`(`bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a hexadecimal string formatted from a byte array range. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [fromHexDigit](HexFormat.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value for the hexadecimal character or codepoint. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [fromHexDigits](HexFormat.md))`(`string:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns the`int`value parsed from a string of up to eight hexadecimal characters. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [fromHexDigits](HexFormat.md))`(`string:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the`int`value parsed from a string range of up to eight hexadecimal characters. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [fromHexDigitsToLong](HexFormat.md))`(`string:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns the long value parsed from a string of up to sixteen hexadecimal characters. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [fromHexDigitsToLong](HexFormat.md))`(`string:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the long value parsed from a string range of up to sixteen hexadecimal characters. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](HexFormat.md))`()` Returns a hashcode for this`HexFormat`. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHexDigit](HexFormat.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns`true`if the character is a valid hexadecimal character or codepoint. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUpperCase](HexFormat.md))`()` Returns`true`if the hexadecimal digits are uppercase, otherwise`false`. |
| static [HexFormat](HexFormat.md)! | [of](HexFormat.md))`()` Returns a hexadecimal formatter with no delimiter and lowercase characters. |
| --- | --- |
| static [HexFormat](HexFormat.md)! | [ofDelimiter](HexFormat.md))`(`delimiter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a hexadecimal formatter with the delimiter and lowercase characters. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [parseHex](HexFormat.md))`(`chars:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a byte array containing hexadecimal values parsed from a range of the character array. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [parseHex](HexFormat.md))`(`string:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns a byte array containing hexadecimal values parsed from the string. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [parseHex](HexFormat.md))`(`string:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a byte array containing hexadecimal values parsed from a range of the string. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [prefix](HexFormat.md))`()` Returns the prefix used for each hexadecimal value in formatted hexadecimal strings. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [suffix](HexFormat.md))`()` Returns the suffix used for each hexadecimal value in formatted hexadecimal strings. |
| --- | --- |
| A | [toHexDigits](HexFormat.md))`(`out:` `A`, `value:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Appends two hexadecimal characters for the byte value to the [Appendable](../java.lang/Appendable.md). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toHexDigits](HexFormat.md))`(`value:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Returns the two hexadecimal characters for the`byte`value. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toHexDigits](HexFormat.md))`(`value:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Returns the four hexadecimal characters for the`char`value. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toHexDigits](HexFormat.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the eight hexadecimal characters for the`int`value. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toHexDigits](HexFormat.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the sixteen hexadecimal characters for the`long`value. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toHexDigits](HexFormat.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `digits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns up to sixteen hexadecimal characters for the`long`value. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toHexDigits](HexFormat.md))`(`value:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Returns the four hexadecimal characters for the`short`value. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [toHighHexDigit](HexFormat.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the hexadecimal character for the high 4 bits of the value considering it to be a byte. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [toLowHexDigit](HexFormat.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the hexadecimal character for the low 4 bits of the value considering it to be a byte. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](HexFormat.md))`()` Returns a description of the formatter parameters for uppercase, delimiter, prefix, and suffix. |
| [HexFormat](HexFormat.md)! | [withDelimiter](HexFormat.md))`(`delimiter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a copy of this`HexFormat`with the delimiter. |
| [HexFormat](HexFormat.md)! | [withLowerCase](HexFormat.md))`()` Returns a copy of this`HexFormat`to use lowercase hexadecimal characters. |
| --- | --- |
| [HexFormat](HexFormat.md)! | [withPrefix](HexFormat.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a copy of this`HexFormat`with the prefix. |
| [HexFormat](HexFormat.md)! | [withSuffix](HexFormat.md))`(`suffix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a copy of this`HexFormat`with the suffix. |
| [HexFormat](HexFormat.md)! | [withUpperCase](HexFormat.md))`()` Returns a copy of this`HexFormat`to use uppercase hexadecimal characters. |
| --- | --- |

## Public methods

### delimiter

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun delimiter(): String!
```

Returns the delimiter between hexadecimal values in formatted hexadecimal strings.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the delimiter, non-null, may be empty`""` |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Returns`true`if the other object is a`HexFormat`with the same parameters.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | an object, may be null |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the other object is a`HexFormat`and the parameters uppercase, delimiter, prefix, and suffix are equal; otherwise`false` |

### formatHex

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <A : Appendable!> formatHex(
    out: A, 
    bytes: ByteArray!
): A
```

Appends formatted hexadecimal strings from a byte array to the [Appendable](../java.lang/Appendable.md). Each byte value is formatted as the prefix, two hexadecimal characters [selected from](HexFormat.md))uppercase or lowercase digits, and the suffix. A delimiter follows each formatted value, except the last. The formatted hexadecimal strings are appended in zero or more calls to the [Appendable](../java.lang/Appendable.md) methods.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `<A>` | The type of`Appendable` |
| `out` | A:an`Appendable`, non-null |
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array |
| --- | --- |

| Return ||
|---|-----------------|
| A | the`Appendable` |

| Exceptions ||
|--------------------------------|----------------------------------------------------|
| `java.io.UncheckedIOException` | if an I/O exception occurs appending to the output |

### formatHex

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <A : Appendable!> formatHex(
    out: A, 
    bytes: ByteArray!, 
    fromIndex: Int, 
    toIndex: Int
): A
```

Appends formatted hexadecimal strings from a byte array range to the [Appendable](../java.lang/Appendable.md). Each byte value is formatted as the prefix, two hexadecimal characters [selected from](HexFormat.md))uppercase or lowercase digits, and the suffix. A delimiter follows each formatted value, except the last. The formatted hexadecimal strings are appended in zero or more calls to the [Appendable](../java.lang/Appendable.md) methods.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `<A>` | The type of`Appendable` |
| `out` | A:an`Appendable`, non-null |
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array, non-null |
| --- | --- |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial index of the range, inclusive |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the final index of the range, exclusive. |

| Return ||
|---|-----------------|
| A | the`Appendable` |

| Exceptions ||
|---------------------------------------|----------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the array range is out of bounds |
| `java.io.UncheckedIOException` | if an I/O exception occurs appending to the output |

### formatHex

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun formatHex(bytes: ByteArray!): String!
```

Returns a hexadecimal string formatted from a byte array. Each byte value is formatted as the prefix, two hexadecimal characters [selected from](HexFormat.md))uppercase or lowercase digits, and the suffix. A delimiter follows each formatted value, except the last. The behavior is equivalent to [formatHex(bytes, 0, bytes.length))](HexFormat.md)).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a non-null array of bytes |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string hexadecimal formatting of the byte array |

### formatHex

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun formatHex(
    bytes: ByteArray!, 
    fromIndex: Int, 
    toIndex: Int
): String!
```

Returns a hexadecimal string formatted from a byte array range. Each byte value is formatted as the prefix, two hexadecimal characters [selected from](HexFormat.md))uppercase or lowercase digits, and the suffix. A delimiter follows each formatted value, except the last.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a non-null array of bytes |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial index of the range, inclusive |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the final index of the range, exclusive |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string hexadecimal formatting each byte of the array range |

| Exceptions ||
|---------------------------------------|-------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the array range is out of bounds |

### fromHexDigit

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromHexDigit(ch: Int): Int
```

Returns the value for the hexadecimal character or codepoint. The value is:

- `(ch - '0')`for`'0'`through`'9'`inclusive,
- `(ch - 'A' + 10)`for`'A'`through`'F'`inclusive, and
- `(ch - 'a' + 10)`for`'a'`through`'f'`inclusive.

<br />

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a character or codepoint |

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0-15` |

| Exceptions ||
|-----------------------------------|-------------------------------------------------|
| `java.lang.NumberFormatException` | if the codepoint is not a hexadecimal character |

### fromHexDigits

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromHexDigits(string: CharSequence!): Int
```

Returns the`int`value parsed from a string of up to eight hexadecimal characters. The hexadecimal characters are parsed from most significant to least significant using [fromHexDigit(int)](HexFormat.md))to form an unsigned value. The value is zero extended to 32 bits and is returned as an`int`.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `string` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:a CharSequence containing up to eight hexadecimal characters |

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value parsed from the string |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the string length is greater than eight (8) or if any of the characters is not a hexadecimal character |

### fromHexDigits

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromHexDigits(
    string: CharSequence!, 
    fromIndex: Int, 
    toIndex: Int
): Int
```

Returns the`int`value parsed from a string range of up to eight hexadecimal characters. The characters in the range`fromIndex`to`toIndex`, exclusive, are parsed from most significant to least significant using [fromHexDigit(int)](HexFormat.md))to form an unsigned value. The value is zero extended to 32 bits and is returned as an`int`.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `string` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:a CharSequence containing the characters |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial index of the range, inclusive |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the final index of the range, exclusive. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value parsed from the string range |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the range is out of bounds for the`CharSequence` |
| `java.lang.IllegalArgumentException` | if length of the range is greater than eight (8) or if any of the characters is not a hexadecimal character |

### fromHexDigitsToLong

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromHexDigitsToLong(string: CharSequence!): Long
```

Returns the long value parsed from a string of up to sixteen hexadecimal characters. The hexadecimal characters are parsed from most significant to least significant using [fromHexDigit(int)](HexFormat.md))to form an unsigned value. The value is zero extended to 64 bits and is returned as a`long`.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `string` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:a CharSequence containing up to sixteen hexadecimal characters |

| Return ||
|------------------------------------------------------------------------------|----------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value parsed from the string |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the string length is greater than sixteen (16) or if any of the characters is not a hexadecimal character |

### fromHexDigitsToLong

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromHexDigitsToLong(
    string: CharSequence!, 
    fromIndex: Int, 
    toIndex: Int
): Long
```

Returns the long value parsed from a string range of up to sixteen hexadecimal characters. The characters in the range`fromIndex`to`toIndex`, exclusive, are parsed from most significant to least significant using [fromHexDigit(int)](HexFormat.md))to form an unsigned value. The value is zero extended to 64 bits and is returned as a`long`.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `string` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:a CharSequence containing the characters |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial index of the range, inclusive |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the final index of the range, exclusive. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value parsed from the string range |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the range is out of bounds for the`CharSequence` |
| `java.lang.IllegalArgumentException` | if the length of the range is greater than sixteen (16) or if any of the characters is not a hexadecimal character |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hashcode for this`HexFormat`.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hashcode for this`HexFormat` |

### isHexDigit

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isHexDigit(ch: Int): Boolean
```

Returns`true`if the character is a valid hexadecimal character or codepoint. The valid hexadecimal characters are:

- `'0' ('\u005Cu0030')`through`'9' ('\u005Cu0039')`inclusive,
- `'A' ('\u005Cu0041')`through`'F' ('\u005Cu0046')`inclusive, and
- `'a' ('\u005Cu0061')`through`'f' ('\u005Cu0066')`inclusive.

<br />

| Parameters ||
|------|----------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a codepoint |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the character is valid a hexadecimal character, otherwise`false` |

### isUpperCase

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isUpperCase(): Boolean
```

Returns`true`if the hexadecimal digits are uppercase, otherwise`false`.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the hexadecimal digits are uppercase, otherwise`false` |

### of

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(): HexFormat!
```

Returns a hexadecimal formatter with no delimiter and lowercase characters. The delimiter, prefix, and suffix are empty. The methods [withDelimiter](HexFormat.md)), [withUpperCase](HexFormat.md)), [withLowerCase](HexFormat.md)), [withPrefix](HexFormat.md)), and [withSuffix](HexFormat.md))return copies of formatters with new parameters.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [HexFormat](HexFormat.md)! | a hexadecimal formatter with no delimiter and lowercase characters |

### ofDelimiter

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofDelimiter(delimiter: String!): HexFormat!
```

Returns a hexadecimal formatter with the delimiter and lowercase characters. The prefix and suffix are empty. The methods [withDelimiter](HexFormat.md)), [withUpperCase](HexFormat.md)), [withLowerCase](HexFormat.md)), [withPrefix](HexFormat.md)), and [withSuffix](HexFormat.md))return copies of formatters with new parameters.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------|
| `delimiter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a delimiter, non-null, may be empty |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [HexFormat](HexFormat.md)! | a [HexFormat](HexFormat.md) with the delimiter and lowercase characters |

### parseHex

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun parseHex(
    chars: CharArray!, 
    fromIndex: Int, 
    toIndex: Int
): ByteArray!
```

Returns a byte array containing hexadecimal values parsed from a range of the character array. Each byte value is parsed from the prefix, two case insensitive hexadecimal characters, and the suffix. A delimiter follows each formatted value, except the last. The delimiters, prefixes, and suffixes strings must be present; they may be empty strings. A valid character array range consists only of the above format.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `chars` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:a character array range containing an even number of hexadecimal digits, delimiters, prefix, and suffix. |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial index of the range, inclusive |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the final index of the range, exclusive. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a byte array with the values parsed from the character array range |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the prefix or suffix is not present for each byte value, the byte values are not hexadecimal characters, or if the delimiter is not present after all but the last byte value |
| `java.lang.IndexOutOfBoundsException` | if the character array range is out of bounds |

### parseHex

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun parseHex(string: CharSequence!): ByteArray!
```

Returns a byte array containing hexadecimal values parsed from the string. Each byte value is parsed from the prefix, two case insensitive hexadecimal characters, and the suffix. A delimiter follows each formatted value, except the last. The delimiters, prefixes, and suffixes strings must be present; they may be empty strings. A valid string consists only of the above format.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `string` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:a string containing the byte values with prefix, hexadecimal digits, suffix, and delimiters |

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a byte array with the values parsed from the string |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the prefix or suffix is not present for each byte value, the byte values are not hexadecimal characters, or if the delimiter is not present after all but the last byte value |

### parseHex

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun parseHex(
    string: CharSequence!, 
    fromIndex: Int, 
    toIndex: Int
): ByteArray!
```

Returns a byte array containing hexadecimal values parsed from a range of the string. Each byte value is parsed from the prefix, two case insensitive hexadecimal characters, and the suffix. A delimiter follows each formatted value, except the last. The delimiters, prefixes, and suffixes strings must be present; they may be empty strings. A valid string consists only of the above format.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `string` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:a string range containing hexadecimal digits, delimiters, prefix, and suffix. |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial index of the range, inclusive |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the final index of the range, exclusive. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a byte array with the values parsed from the string range |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the prefix or suffix is not present for each byte value, the byte values are not hexadecimal characters, or if the delimiter is not present after all but the last byte value |
| `java.lang.IndexOutOfBoundsException` | if the string range is out of bounds |

### prefix

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun prefix(): String!
```

Returns the prefix used for each hexadecimal value in formatted hexadecimal strings.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the prefix, non-null, may be empty`""` |

### suffix

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun suffix(): String!
```

Returns the suffix used for each hexadecimal value in formatted hexadecimal strings.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the suffix, non-null, may be empty`""` |

### toHexDigits

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <A : Appendable!> toHexDigits(
    out: A, 
    value: Byte
): A
```

Appends two hexadecimal characters for the byte value to the [Appendable](../java.lang/Appendable.md). Each nibble (4 bits) from most significant to least significant of the value is formatted as if by [toLowHexDigit(nibble)](HexFormat.md)). The hexadecimal characters are appended in one or more calls to the [Appendable](../java.lang/Appendable.md) methods. The delimiter, prefix and suffix are not used.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------|
| `<A>` | The type of`Appendable` |
| `out` | A:an`Appendable`, non-null |
| `value` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):a byte value |
| --- | --- |

| Return ||
|---|-----------------|
| A | the`Appendable` |

| Exceptions ||
|--------------------------------|----------------------------------------------------|
| `java.io.UncheckedIOException` | if an I/O exception occurs appending to the output |

### toHexDigits

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toHexDigits(value: Byte): String!
```

Returns the two hexadecimal characters for the`byte`value. Each nibble (4 bits) from most significant to least significant of the value is formatted as if by [toLowHexDigit(nibble)](HexFormat.md)). The delimiter, prefix and suffix are not used.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------|
| `value` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):a byte value |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the two hexadecimal characters for the byte value |

### toHexDigits

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toHexDigits(value: Char): String!
```

Returns the four hexadecimal characters for the`char`value. Each nibble (4 bits) from most significant to least significant of the value is formatted as if by [toLowHexDigit(nibble)](HexFormat.md)). The delimiter, prefix and suffix are not used.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------|
| `value` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):a`char`value |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the four hexadecimal characters for the`char`value |

### toHexDigits

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toHexDigits(value: Int): String!
```

Returns the eight hexadecimal characters for the`int`value. Each nibble (4 bits) from most significant to least significant of the value is formatted as if by [toLowHexDigit(nibble)](HexFormat.md)). The delimiter, prefix and suffix are not used.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an`int`value |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the eight hexadecimal characters for the`int`value |

**See Also**

- [java.lang.Integer#toHexString](../java.lang/Integer.md)) 

### toHexDigits

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toHexDigits(value: Long): String!
```

Returns the sixteen hexadecimal characters for the`long`value. Each nibble (4 bits) from most significant to least significant of the value is formatted as if by [toLowHexDigit(nibble)](HexFormat.md)). The delimiter, prefix and suffix are not used.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a`long`value |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the sixteen hexadecimal characters for the`long`value |

**See Also**

- [java.lang.Long#toHexString](../java.lang/Long.md)) 

### toHexDigits

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toHexDigits(
    value: Long, 
    digits: Int
): String!
```

Returns up to sixteen hexadecimal characters for the`long`value. Each nibble (4 bits) from most significant to least significant of the value is formatted as if by [toLowHexDigit(nibble)](HexFormat.md)). The delimiter, prefix and suffix are not used.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a`long`value |
| `digits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of hexadecimal digits to return, 0 to 16 |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the hexadecimal characters for the`long`value |

| Exceptions ||
|--------------------------------------|------------------------------------------|
| `java.lang.IllegalArgumentException` | if`digits`is negative or greater than 16 |

### toHexDigits

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toHexDigits(value: Short): String!
```

Returns the four hexadecimal characters for the`short`value. Each nibble (4 bits) from most significant to least significant of the value is formatted as if by [toLowHexDigit(nibble)](HexFormat.md)). The delimiter, prefix and suffix are not used.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------|
| `value` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):a`short`value |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the four hexadecimal characters for the`short`value |

### toHighHexDigit

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toHighHexDigit(value: Int): Char
```

Returns the hexadecimal character for the high 4 bits of the value considering it to be a byte. If the parameter [isUpperCase()](HexFormat.md))is`true`the character returned for values`10-15`is uppercase`"A-F"`, otherwise the character returned is lowercase`"a-f"`. The values in the range`0-9`are returned as`"0-9"`.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a value, only bits`4-7`of the value are used |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the hexadecimal character for the bits`4-7`of the value |

### toLowHexDigit

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toLowHexDigit(value: Int): Char
```

Returns the hexadecimal character for the low 4 bits of the value considering it to be a byte. If the parameter [isUpperCase()](HexFormat.md))is`true`the character returned for values`10-15`is uppercase`"A-F"`, otherwise the character returned is lowercase`"a-f"`. The values in the range`0-9`are returned as`"0-9"`.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a value, only the low 4 bits`0-3`of the value are used |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the hexadecimal character for the low 4 bits`0-3`of the value |

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a description of the formatter parameters for uppercase, delimiter, prefix, and suffix.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a description of this`HexFormat` |

### withDelimiter

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withDelimiter(delimiter: String!): HexFormat!
```

Returns a copy of this`HexFormat`with the delimiter.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------|
| `delimiter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the delimiter, non-null, may be empty |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [HexFormat](HexFormat.md)! | a copy of this`HexFormat`with the delimiter |

### withLowerCase

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withLowerCase(): HexFormat!
```

Returns a copy of this`HexFormat`to use lowercase hexadecimal characters. The lowercase hexadecimal characters are`"0-9", "a-f"`.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------|
| [HexFormat](HexFormat.md)! | a copy of this`HexFormat`with lowercase hexadecimal characters |

### withPrefix

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withPrefix(prefix: String!): HexFormat!
```

Returns a copy of this`HexFormat`with the prefix.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a prefix, non-null, may be empty |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [HexFormat](HexFormat.md)! | a copy of this`HexFormat`with the prefix |

### withSuffix

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withSuffix(suffix: String!): HexFormat!
```

Returns a copy of this`HexFormat`with the suffix.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `suffix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a suffix, non-null, may be empty |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [HexFormat](HexFormat.md)! | a copy of this`HexFormat`with the suffix |

### withUpperCase

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withUpperCase(): HexFormat!
```

Returns a copy of this`HexFormat`to use uppercase hexadecimal characters. The uppercase hexadecimal characters are`"0-9", "A-F"`.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------|
| [HexFormat](HexFormat.md)! | a copy of this`HexFormat`with uppercase hexadecimal characters |
