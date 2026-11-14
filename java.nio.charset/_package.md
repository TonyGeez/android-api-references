# java.nio.charset

# java.nio.charset

## Classes

| [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset) | A named mapping between sequences of sixteen-bit Unicode [code units](https://developer.android.com/reference/kotlin/java/lang/Character.html#unicode) and sequences of bytes. |
| [CharsetDecoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder) | An engine that can transform a sequence of bytes in a specific charset into a sequence of sixteen-bit Unicode characters. |
| [CharsetEncoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder) | An engine that can transform a sequence of sixteen-bit Unicode characters into a sequence of bytes in a specific charset. |
| [CoderResult](https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult) | A description of the result state of a coder. |
| [CodingErrorAction](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction) | A typesafe enumeration for coding-error actions. |
| [StandardCharsets](https://developer.android.com/reference/kotlin/java/nio/charset/StandardCharsets) | Constant definitions for the standard [Charsets](https://developer.android.com/reference/kotlin/java/nio/charset/Charset). |

## Exceptions

| [CharacterCodingException](https://developer.android.com/reference/kotlin/java/nio/charset/CharacterCodingException) | Checked exception thrown when a character encoding or decoding error occurs. |
| [CoderMalfunctionError](https://developer.android.com/reference/kotlin/java/nio/charset/CoderMalfunctionError) | Error thrown when the [decodeLoop](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder#decodeLoop(java.nio.ByteBuffer,%20java.nio.CharBuffer))method of a [CharsetDecoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder), or the [encodeLoop](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#encodeLoop(java.nio.CharBuffer,%20java.nio.ByteBuffer))method of a [CharsetEncoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder), throws an unexpected exception. |
| [IllegalCharsetNameException](https://developer.android.com/reference/kotlin/java/nio/charset/IllegalCharsetNameException) | Unchecked exception thrown when a string that is not a [legal charset name](https://developer.android.com/reference/kotlin/java/nio/charset/Charset#names) is used as such. |
| [MalformedInputException](https://developer.android.com/reference/kotlin/java/nio/charset/MalformedInputException) | Checked exception thrown when an input byte sequence is not legal for given charset, or an input character sequence is not a legal sixteen-bit Unicode sequence. |
| [UnmappableCharacterException](https://developer.android.com/reference/kotlin/java/nio/charset/UnmappableCharacterException) | Checked exception thrown when an input character (or byte) sequence is valid but cannot be mapped to an output byte (or character) sequence. |
| [UnsupportedCharsetException](https://developer.android.com/reference/kotlin/java/nio/charset/UnsupportedCharsetException) | Unchecked exception thrown when no support is available for a requested charset. |
