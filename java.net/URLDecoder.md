# URLDecoder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# URLDecoder

```
open class URLDecoder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.URLDecoder](../java/net/URLDecoder.md) |

Utility class for HTML form decoding. This class contains static methods for decoding a String from the`application/x-www-form-urlencoded`MIME format.

The conversion process is the reverse of that used by the URLEncoder class. It is assumed that all characters in the encoded string are one of the following: "`a`" through "`z`", "`A`" through "`Z`", "`0`" through "`9`", and "`-`", "`_`", "`.`", and "`*`". The character "`%`" is allowed but is interpreted as the start of a special escaped sequence.

The following rules are applied in the conversion:

- The alphanumeric characters "`a`" through "`z`", "`A`" through "`Z`" and "`0`" through "`9`" remain the same.
- The special characters "`.`", "`-`", "`*`", and "`_`" remain the same.
- The plus sign "`+`" is converted into a space character " " .
- A sequence of the form "*`%xy`* " will be treated as representing a byte where*xy*is the two-digit hexadecimal representation of the 8 bits. Then, all substrings that contain one or more of these byte sequences consecutively will be replaced by the character(s) whose encoding would result in those consecutive bytes. The encoding scheme used to decode these characters may be specified, or if unspecified, the default encoding of the platform will be used.

There are two possible ways in which this decoder could deal with illegal strings. It could either leave illegal characters alone or it could throw an [java.lang.IllegalArgumentException](../java/lang/IllegalArgumentException.md). Which approach the decoder takes is left to the implementation.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------|---|
| [URLDecoder](../java/net/URLDecoder.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [decode](../java/net/URLDecoder.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Decodes a`x-www-form-urlencoded`string. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [decode](../java/net/URLDecoder.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `enc:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Decodes an`application/x-www-form-urlencoded`string using a specific encoding scheme. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [decode](../java/net/URLDecoder.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `charset:` ` [Charset](../java/nio/charset/Charset.md)!`)` Decodes an`application/x-www-form-urlencoded`string using a specific [Charset](../java/nio/charset/Charset.md). |
| --- | --- |

## Public constructors

### URLDecoder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
URLDecoder()
```

## Public methods

### decode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun decode(s: String!): String!
```

**Deprecated:** *The resulting string may vary depending on the platform's default encoding. Instead, use the decode(String,String) method to specify the encoding.*

Decodes a`x-www-form-urlencoded`string. The platform's default encoding is used to determine what characters are represented by any consecutive sequences of the form "*`%xy`*".

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the`String`to decode |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the newly decoded`String` |

### decode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun decode(
    s: String!, 
    enc: String!
): String!
```

Decodes an`application/x-www-form-urlencoded`string using a specific encoding scheme.

This method behaves the same as [decode(String s, Charset charset)](../java/lang/String.md) except that it will [look up the charset](../java/nio/charset/Charset.md))using the given encoding name.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the`String`to decode |
| `enc` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of a supported [character encoding](../java/lang/_package.md). |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the newly decoded`String` |

| Exceptions ||
|----------------------------------------|--------------------------------------------------------------------------------------------|
| `java.io.UnsupportedEncodingException` | If character encoding needs to be consulted, but named character encoding is not supported |

**See Also**

- [java.net.URLEncoder#encode(java.lang.String, java.lang.String)](../java/net/URLEncoder.md)) 

### decode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun decode(
    s: String!, 
    charset: Charset!
): String!
```

Decodes an`application/x-www-form-urlencoded`string using a specific [Charset](../java/nio/charset/Charset.md). The supplied charset is used to determine what characters are represented by any consecutive sequences of the form "*`%xy`*".

***Note:** The [World Wide Web Consortium Recommendation](http://www.w3.org/TR/html40/appendix/notes.html#non-ascii-chars) states that UTF-8 should be used. Not doing so may introduce incompatibilities.*

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the`String`to decode |
| `charset` | [Charset](../java/nio/charset/Charset.md)!:the given charset |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the newly decoded`String` |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------|
| `java.lang.NullPointerException` | if`s`or`charset`is`null` |
| `java.lang.IllegalArgumentException` | if the implementation encounters illegal characters |

**See Also**

- [java.net.URLEncoder#encode(java.lang.String, java.nio.charset.Charset)](../java/net/URLEncoder.md))
