Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# URLEncoder

```
open class URLEncoder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.URLEncoder](URLEncoder.md) |

Utility class for HTML form encoding. This class contains static methods for converting a String to the `application/x-www-form-urlencoded` MIME format. For more information about HTML form encoding, consult the HTML [specification](http://www.w3.org/TR/html4/).

When encoding a String, the following rules apply:

- The alphanumeric characters "`a`" through "`z`", "`A`" through "`Z`" and "`0`" through "`9`" remain the same.
- The special characters "`.`", "`-`", "`*`", and "`_`" remain the same.
- The space character " " is converted into a plus sign "`+`".
- All other characters are unsafe and are first converted into one or more bytes using some encoding scheme. Then each byte is represented by the 3-character string "*`%xy`* ", where *xy* is the two-digit hexadecimal representation of the byte. The recommended encoding scheme to use is UTF-8. However, for compatibility reasons, if an encoding is not specified, then the default encoding of the platform is used.

For example using UTF-8 as the encoding scheme the string "The string ü@foo-bar" would get converted to "The+string+%C3%BC%40foo-bar" because in UTF-8 the character ü is encoded as two bytes C3 (hex) and BC (hex), and the character @ is encoded as one byte 40 (hex).

## Summary

| Public methods ||
|---|---|
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/URLEncoder#encode(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Translates a string into `x-www-form-urlencoded` format. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/URLEncoder#encode(kotlin.String,%20kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, enc: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Translates a string into `application/x-www-form-urlencoded` format using a specific encoding scheme. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/URLEncoder#encode(kotlin.String,%20java.nio.charset.Charset)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, charset: https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#!)` Translates a string into `application/x-www-form-urlencoded` format using a specific [Charset](../java.nio.charset/Charset.md). |
| --- | --- |

## Public methods

### encode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun encode(s: String!): String!
```

**Deprecated:** *The resulting string may vary depending on the platform's default encoding. Instead, use the encode(String,String) method to specify the encoding.*

Translates a string into `x-www-form-urlencoded` format. This method uses the platform's default encoding as the encoding scheme to obtain the bytes for unsafe characters.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: `String` to be translated. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the translated `String`. |

### encode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun encode(
    s: String!, 
    enc: String!
): String!
```

Translates a string into `application/x-www-form-urlencoded` format using a specific encoding scheme.

This method behaves the same as [encode(String s, Charset charset)](../java.lang/String.md) except that it will java.nio.charset.Charset#forName using the given encoding name.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: `String` to be translated. |
| `enc` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of a supported [character encoding](../java.lang/_package.md). |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the translated `String`. |

| Exceptions ||
|---|---|
| `java.io.UnsupportedEncodingException` | If the named encoding is not supported |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/URLDecoder#decode(kotlin.String,%20kotlin.String)`

### encode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun encode(
    s: String!, 
    charset: Charset!
): String!
```

Translates a string into `application/x-www-form-urlencoded` format using a specific [Charset](../java.nio.charset/Charset.md). This method uses the supplied charset to obtain the bytes for unsafe characters.

***Note:** The [World Wide Web Consortium Recommendation](http://www.w3.org/TR/html40/appendix/notes.html#non-ascii-chars) states that UTF-8 should be used. Not doing so may introduce incompatibilities.*

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: `String` to be translated. |
| `charset` | [Charset](../java.nio.charset/Charset.md)!: the given charset |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the translated `String`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `s` or `charset` is `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/URLDecoder#decode(kotlin.String,%20java.nio.charset.Charset)`
