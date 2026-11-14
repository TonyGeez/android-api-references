# Base64

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Base64

Kotlin| [Java](../android/util/Base64.md) 
| --- | --- |

```
open class Base64
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.Base64](../android/util/Base64.md) |

Utilities for encoding and decoding the Base64 representation of binary data. See RFCs [2045](http://www.ietf.org/rfc/rfc2045.txt) and [3548](http://www.ietf.org/rfc/rfc3548.txt).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CRLF](../android/util/Base64.md) Encoder flag bit to indicate lines should be terminated with a CRLF pair instead of just an LF. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT](../android/util/Base64.md) Default values for encoder/decoder flags. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_CLOSE](../android/util/Base64.md) Flag to pass to [Base64OutputStream](../android/util/Base64OutputStream.md) to indicate that it should not close the output stream it is wrapping when it itself is closed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_PADDING](../android/util/Base64.md) Encoder flag bit to omit the padding '=' characters at the end of the output (if any). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_WRAP](../android/util/Base64.md) Encoder flag bit to omit all line terminators (i.e., the output will be on one long line). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [URL_SAFE](../android/util/Base64.md) Encoder/decoder flag bit to indicate using the "URL and filename safe" variant of Base64 (see RFC 3548 section 4) where`-`and`_`are used in place of`+`and`/`. |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [decode](../android/util/Base64.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Decode the Base64-encoded data in input and return the data in a new byte array. |
| openstatic [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [decode](../android/util/Base64.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Decode the Base64-encoded data in input and return the data in a new byte array. |
| openstatic [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [decode](../android/util/Base64.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Decode the Base64-encoded data in input and return the data in a new byte array. |
| --- | --- |
| openstatic [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [encode](../android/util/Base64.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Base64-encode the given data and return a newly allocated byte\[\] with the result. |
| openstatic [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [encode](../android/util/Base64.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Base64-encode the given data and return a newly allocated byte\[\] with the result. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [encodeToString](../android/util/Base64.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Base64-encode the given data and return a newly allocated String with the result. |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [encodeToString](../android/util/Base64.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Base64-encode the given data and return a newly allocated String with the result. |

## Constants

### CRLF

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CRLF: Int
```

Encoder flag bit to indicate lines should be terminated with a CRLF pair instead of just an LF. Has no effect if`NO_WRAP`is specified as well. 

 Value: 4

### DEFAULT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT: Int
```

Default values for encoder/decoder flags. 

 Value: 0

### NO_CLOSE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_CLOSE: Int
```

Flag to pass to [Base64OutputStream](../android/util/Base64OutputStream.md) to indicate that it should not close the output stream it is wrapping when it itself is closed. 

 Value: 16

### NO_PADDING

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_PADDING: Int
```

Encoder flag bit to omit the padding '=' characters at the end of the output (if any). 

 Value: 1

### NO_WRAP

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_WRAP: Int
```

Encoder flag bit to omit all line terminators (i.e., the output will be on one long line). 

 Value: 2

### URL_SAFE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val URL_SAFE: Int
```

Encoder/decoder flag bit to indicate using the "URL and filename safe" variant of Base64 (see RFC 3548 section 4) where`-`and`_`are used in place of`+`and`/`. 

 Value: 8

## Public methods

### decode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun decode(
    input: ByteArray!, 
    flags: Int
): ByteArray!
```

Decode the Base64-encoded data in input and return the data in a new byte array.

The padding '=' characters at the end are considered optional, but if any are present, there must be the correct number of them.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the input array to decode |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):controls certain features of the decoded output. Pass`DEFAULT`to decode standard Base64. |

| Exceptions ||
|--------------------------------------|-----------------------------------------|
| `java.lang.IllegalArgumentException` | if the input contains incorrect padding |

### decode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun decode(
    input: ByteArray!, 
    offset: Int, 
    len: Int, 
    flags: Int
): ByteArray!
```

Decode the Base64-encoded data in input and return the data in a new byte array.

The padding '=' characters at the end are considered optional, but if any are present, there must be the correct number of them.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data to decode |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position within the input array at which to start |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes of input to decode |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):controls certain features of the decoded output. Pass`DEFAULT`to decode standard Base64. |

| Exceptions ||
|--------------------------------------|-----------------------------------------|
| `java.lang.IllegalArgumentException` | if the input contains incorrect padding |

### decode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun decode(
    str: String!, 
    flags: Int
): ByteArray!
```

Decode the Base64-encoded data in input and return the data in a new byte array.

The padding '=' characters at the end are considered optional, but if any are present, there must be the correct number of them.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the input String to decode, which is converted to bytes using the default charset |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):controls certain features of the decoded output. Pass`DEFAULT`to decode standard Base64. |

| Exceptions ||
|--------------------------------------|-----------------------------------------|
| `java.lang.IllegalArgumentException` | if the input contains incorrect padding |

### encode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun encode(
    input: ByteArray!, 
    flags: Int
): ByteArray!
```

Base64-encode the given data and return a newly allocated byte\[\] with the result.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data to encode |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):controls certain features of the encoded output. Passing`DEFAULT`results in output that adheres to RFC 2045. |

### encode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun encode(
    input: ByteArray!, 
    offset: Int, 
    len: Int, 
    flags: Int
): ByteArray!
```

Base64-encode the given data and return a newly allocated byte\[\] with the result.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data to encode |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position within the input array at which to start |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes of input to encode |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):controls certain features of the encoded output. Passing`DEFAULT`results in output that adheres to RFC 2045. |

### encodeToString

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun encodeToString(
    input: ByteArray!, 
    flags: Int
): String!
```

Base64-encode the given data and return a newly allocated String with the result.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data to encode |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):controls certain features of the encoded output. Passing`DEFAULT`results in output that adheres to RFC 2045. |

### encodeToString

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun encodeToString(
    input: ByteArray!, 
    offset: Int, 
    len: Int, 
    flags: Int
): String!
```

Base64-encode the given data and return a newly allocated String with the result.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data to encode |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position within the input array at which to start |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes of input to encode |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):controls certain features of the encoded output. Passing`DEFAULT`results in output that adheres to RFC 2045. |
