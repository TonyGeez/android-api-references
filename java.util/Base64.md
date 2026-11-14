Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Base64

```
class Base64
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.Base64](https://developer.android.com/reference/kotlin/java/util/Base64#) |

This class consists exclusively of static methods for obtaining encoders and decoders for the Base64 encoding scheme. The implementation of this class supports the following types of Base64 as specified in [RFC 4648](http://www.ietf.org/rfc/rfc4648.txt) and [RFC 2045](http://www.ietf.org/rfc/rfc2045.txt).

- **Basic**

 Uses "The Base64 Alphabet" as specified in Table 1 of RFC 4648 and RFC 2045 for encoding and decoding operation. The encoder does not add any line feed (line separator) character. The decoder rejects data that contains characters outside the base64 alphabet.
- **URL and Filename safe**

 Uses the "URL and Filename safe Base64 Alphabet" as specified in Table 2 of RFC 4648 for encoding and decoding. The encoder does not add any line feed (line separator) character. The decoder rejects data that contains characters outside the base64 alphabet.
- **MIME**

 Uses "The Base64 Alphabet" as specified in Table 1 of RFC 2045 for encoding and decoding operation. The encoded output must be represented in lines of no more than 76 characters each and uses a carriage return `'\r'` followed immediately by a linefeed `'\n'` as the line separator. No line separator is added to the end of the encoded output. All line separators or other characters not found in the base64 alphabet table are ignored in decoding operation.

<br />

Unless otherwise noted, passing a `null` argument to a method of this class will cause a `https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#` to be thrown.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/java/util/Base64.Decoder` This class implements a decoder for decoding byte data using the Base64 encoding scheme as specified in RFC 4648 and RFC 2045. |
| | `https://developer.android.com/reference/kotlin/java/util/Base64.Encoder` This class implements an encoder for encoding byte data using the Base64 encoding scheme as specified in RFC 4648 and RFC 2045. |

| Public methods ||
|---|---|
| static [Base64.Decoder](https://developer.android.com/reference/kotlin/java/util/Base64.Decoder)! | `https://developer.android.com/reference/kotlin/java/util/Base64#getDecoder()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Base64.Decoder` that decodes using the [Basic](https://developer.android.com/reference/kotlin/java/util/Base64#basic) type base64 encoding scheme. |
| static [Base64.Encoder](https://developer.android.com/reference/kotlin/java/util/Base64.Encoder)! | `https://developer.android.com/reference/kotlin/java/util/Base64#getEncoder()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Base64.Encoder` that encodes using the [Basic](https://developer.android.com/reference/kotlin/java/util/Base64#basic) type base64 encoding scheme. |
| static [Base64.Decoder](https://developer.android.com/reference/kotlin/java/util/Base64.Decoder)! | `https://developer.android.com/reference/kotlin/java/util/Base64#getMimeDecoder()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Base64.Decoder` that decodes using the [MIME](https://developer.android.com/reference/kotlin/java/util/Base64#mime) type base64 decoding scheme. |
| --- | --- |
| static [Base64.Encoder](https://developer.android.com/reference/kotlin/java/util/Base64.Encoder)! | `https://developer.android.com/reference/kotlin/java/util/Base64#getMimeEncoder()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Base64.Encoder` that encodes using the [MIME](https://developer.android.com/reference/kotlin/java/util/Base64#mime) type base64 encoding scheme. |
| static [Base64.Encoder](https://developer.android.com/reference/kotlin/java/util/Base64.Encoder)! | `https://developer.android.com/reference/kotlin/java/util/Base64#getMimeEncoder(kotlin.Int,%20kotlin.ByteArray)(lineLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, lineSeparator: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Returns a `https://developer.android.com/reference/kotlin/java/util/Base64.Encoder` that encodes using the [MIME](https://developer.android.com/reference/kotlin/java/util/Base64#mime) type base64 encoding scheme with specified line length and line separators. |
| static [Base64.Decoder](https://developer.android.com/reference/kotlin/java/util/Base64.Decoder)! | `https://developer.android.com/reference/kotlin/java/util/Base64#getUrlDecoder()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Base64.Decoder` that decodes using the [URL and Filename safe](https://developer.android.com/reference/kotlin/java/util/Base64#url) type base64 encoding scheme. |
| --- | --- |
| static [Base64.Encoder](https://developer.android.com/reference/kotlin/java/util/Base64.Encoder)! | `https://developer.android.com/reference/kotlin/java/util/Base64#getUrlEncoder()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Base64.Encoder` that encodes using the [URL and Filename safe](https://developer.android.com/reference/kotlin/java/util/Base64#url) type base64 encoding scheme. |

## Public methods

### getDecoder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDecoder(): Base64.Decoder!
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Base64.Decoder` that decodes using the [Basic](https://developer.android.com/reference/kotlin/java/util/Base64#basic) type base64 encoding scheme.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Base64.Decoder!` | A Base64 decoder. |

### getEncoder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getEncoder(): Base64.Encoder!
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Base64.Encoder` that encodes using the [Basic](https://developer.android.com/reference/kotlin/java/util/Base64#basic) type base64 encoding scheme.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Base64.Encoder!` | A Base64 encoder. |

### getMimeDecoder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getMimeDecoder(): Base64.Decoder!
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Base64.Decoder` that decodes using the [MIME](https://developer.android.com/reference/kotlin/java/util/Base64#mime) type base64 decoding scheme.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Base64.Decoder!` | A Base64 decoder. |

### getMimeEncoder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getMimeEncoder(): Base64.Encoder!
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Base64.Encoder` that encodes using the [MIME](https://developer.android.com/reference/kotlin/java/util/Base64#mime) type base64 encoding scheme.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Base64.Encoder!` | A Base64 encoder. |

### getMimeEncoder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getMimeEncoder(
    lineLength: Int, 
    lineSeparator: ByteArray!
): Base64.Encoder!
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Base64.Encoder` that encodes using the [MIME](https://developer.android.com/reference/kotlin/java/util/Base64#mime) type base64 encoding scheme with specified line length and line separators.

| Parameters ||
|---|---|
| `lineLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of each output line (rounded down to nearest multiple of 4). If the rounded down line length is not a positive value, the output will not be separated in lines |
| `lineSeparator` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the line separator for each output line |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Base64.Encoder!` | A Base64 encoder. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `lineSeparator` includes any character of "The Base64 Alphabet" as specified in Table 1 of RFC 2045. |

### getUrlDecoder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getUrlDecoder(): Base64.Decoder!
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Base64.Decoder` that decodes using the [URL and Filename safe](https://developer.android.com/reference/kotlin/java/util/Base64#url) type base64 encoding scheme.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Base64.Decoder!` | A Base64 decoder. |

### getUrlEncoder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getUrlEncoder(): Base64.Encoder!
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Base64.Encoder` that encodes using the [URL and Filename safe](https://developer.android.com/reference/kotlin/java/util/Base64#url) type base64 encoding scheme.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Base64.Encoder!` | A Base64 encoder. |
