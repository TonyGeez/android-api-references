# IDN

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IDN

```
class IDN
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.IDN](https://developer.android.com/reference/kotlin/java/net/IDN#) |

Provides methods to convert internationalized domain names (IDNs) between a normal Unicode representation and an ASCII Compatible Encoding (ACE) representation. Internationalized domain names can use characters from the entire range of Unicode, while traditional domain names are restricted to ASCII characters. ACE is an encoding of Unicode strings that uses only ASCII characters and can be used with software (such as the Domain Name System) that only understands traditional domain names.

Internationalized domain names are defined in [RFC 3490](http://www.ietf.org/rfc/rfc3490.txt). RFC 3490 defines two operations: ToASCII and ToUnicode. These 2 operations employ [Nameprep](http://www.ietf.org/rfc/rfc3491.txt) algorithm, which is a profile of [Stringprep](http://www.ietf.org/rfc/rfc3454.txt), and [Punycode](http://www.ietf.org/rfc/rfc3492.txt) algorithm to convert domain name string back and forth.

The behavior of aforementioned conversion process can be adjusted by various flags:

- If the ALLOW_UNASSIGNED flag is used, the domain name string to be converted can contain code points that are unassigned in Unicode 3.2, which is the Unicode version on which IDN conversion is based. If the flag is not used, the presence of such unassigned code points is treated as an error.
- If the USE_STD3_ASCII_RULES flag is used, ASCII strings are checked against [RFC 1122](http://www.ietf.org/rfc/rfc1122.txt) and [RFC 1123](http://www.ietf.org/rfc/rfc1123.txt). It is an error if they don't meet the requirements.

These flags can be logically OR'ed together.

The security consideration is important with respect to internationalization domain name support. For example, English domain names may be*homographed* - maliciously misspelled by substitution of non-Latin letters. [Unicode Technical Report #36](http://www.unicode.org/reports/tr36/) discusses security issues of IDN support as well as possible solutions. Applications are responsible for taking adequate security measures when using international domain names.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALLOW_UNASSIGNED](https://developer.android.com/reference/kotlin/java/net/IDN#ALLOW_UNASSIGNED:kotlin.Int) Flag to allow processing of unassigned code points |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USE_STD3_ASCII_RULES](https://developer.android.com/reference/kotlin/java/net/IDN#USE_STD3_ASCII_RULES:kotlin.Int) Flag to turn on the check against STD-3 ASCII rules |

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toASCII](https://developer.android.com/reference/kotlin/java/net/IDN#toASCII(kotlin.String))`(`input:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Translates a string from Unicode to ASCII Compatible Encoding (ACE), as defined by the ToASCII operation of [RFC 3490](http://www.ietf.org/rfc/rfc3490.txt). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toASCII](https://developer.android.com/reference/kotlin/java/net/IDN#toASCII(kotlin.String,%20kotlin.Int))`(`input:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `flag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Translates a string from Unicode to ASCII Compatible Encoding (ACE), as defined by the ToASCII operation of [RFC 3490](http://www.ietf.org/rfc/rfc3490.txt). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toUnicode](https://developer.android.com/reference/kotlin/java/net/IDN#toUnicode(kotlin.String))`(`input:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Translates a string from ASCII Compatible Encoding (ACE) to Unicode, as defined by the ToUnicode operation of [RFC 3490](http://www.ietf.org/rfc/rfc3490.txt). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toUnicode](https://developer.android.com/reference/kotlin/java/net/IDN#toUnicode(kotlin.String,%20kotlin.Int))`(`input:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `flag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Translates a string from ASCII Compatible Encoding (ACE) to Unicode, as defined by the ToUnicode operation of [RFC 3490](http://www.ietf.org/rfc/rfc3490.txt). |

## Constants

### ALLOW_UNASSIGNED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALLOW_UNASSIGNED: Int
```

Flag to allow processing of unassigned code points 

 Value: 1

### USE_STD3_ASCII_RULES

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USE_STD3_ASCII_RULES: Int
```

Flag to turn on the check against STD-3 ASCII rules 

 Value: 2

## Public methods

### toASCII

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toASCII(input: String!): String!
```

Translates a string from Unicode to ASCII Compatible Encoding (ACE), as defined by the ToASCII operation of [RFC 3490](http://www.ietf.org/rfc/rfc3490.txt).

This convenience method works as if by invoking the two-argument counterpart as follows:
[toASCII](https://developer.android.com/reference/kotlin/java/net/IDN#toASCII(kotlin.String,%20kotlin.Int))(input, 0);

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `input` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to be processed |

| Return ||
|-----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the translated`String` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the input string doesn't conform to RFC 3490 specification |

### toASCII

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toASCII(
    input: String!, 
    flag: Int
): String!
```

Translates a string from Unicode to ASCII Compatible Encoding (ACE), as defined by the ToASCII operation of [RFC 3490](http://www.ietf.org/rfc/rfc3490.txt).

ToASCII operation can fail. ToASCII fails if any step of it fails. If ToASCII operation fails, an IllegalArgumentException will be thrown. In this case, the input string should not be used in an internationalized domain name.

A label is an individual part of a domain name. The original ToASCII operation, as defined in RFC 3490, only operates on a single label. This method can handle both label and entire domain name, by assuming that labels in a domain name are always separated by dots. The following characters are recognized as dots: \\u002E (full stop), \\u3002 (ideographic full stop), \\uFF0E (fullwidth full stop), and \\uFF61 (halfwidth ideographic full stop). if dots are used as label separators, this method also changes all of them to \\u002E (full stop) in output translated string.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to be processed |
| `flag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):process flag; can be 0 or any logical OR of possible flags |

| Return ||
|-----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the translated`String` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the input string doesn't conform to RFC 3490 specification |

### toUnicode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUnicode(input: String!): String!
```

Translates a string from ASCII Compatible Encoding (ACE) to Unicode, as defined by the ToUnicode operation of [RFC 3490](http://www.ietf.org/rfc/rfc3490.txt).

This convenience method works as if by invoking the two-argument counterpart as follows:
[toUnicode](https://developer.android.com/reference/kotlin/java/net/IDN#toUnicode(kotlin.String,%20kotlin.Int))(input, 0);

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `input` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to be processed |

| Return ||
|-----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the translated`String` |

### toUnicode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUnicode(
    input: String!, 
    flag: Int
): String!
```

Translates a string from ASCII Compatible Encoding (ACE) to Unicode, as defined by the ToUnicode operation of [RFC 3490](http://www.ietf.org/rfc/rfc3490.txt).

ToUnicode never fails. In case of any error, the input string is returned unmodified.

A label is an individual part of a domain name. The original ToUnicode operation, as defined in RFC 3490, only operates on a single label. This method can handle both label and entire domain name, by assuming that labels in a domain name are always separated by dots. The following characters are recognized as dots: \\u002E (full stop), \\u3002 (ideographic full stop), \\uFF0E (fullwidth full stop), and \\uFF61 (halfwidth ideographic full stop).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to be processed |
| `flag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):process flag; can be 0 or any logical OR of possible flags |

| Return ||
|-----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the translated`String` |
