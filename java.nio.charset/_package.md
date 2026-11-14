# java.nio.charset

# java.nio.charset

## Classes

| [Charset](../java/nio/charset/Charset.md) | A named mapping between sequences of sixteen-bit Unicode [code units](../java/lang/Character.md) and sequences of bytes. |
| --- | --- |
| [CharsetDecoder](../java/nio/charset/CharsetDecoder.md) | An engine that can transform a sequence of bytes in a specific charset into a sequence of sixteen-bit Unicode characters. |
| [CharsetEncoder](../java/nio/charset/CharsetEncoder.md) | An engine that can transform a sequence of sixteen-bit Unicode characters into a sequence of bytes in a specific charset. |
| [CoderResult](../java/nio/charset/CoderResult.md) | A description of the result state of a coder. |
| --- | --- |
| [CodingErrorAction](../java/nio/charset/CodingErrorAction.md) | A typesafe enumeration for coding-error actions. |
| [StandardCharsets](../java/nio/charset/StandardCharsets.md) | Constant definitions for the standard [Charsets](../java/nio/charset/Charset.md). |

## Exceptions

| [CharacterCodingException](../java/nio/charset/CharacterCodingException.md) | Checked exception thrown when a character encoding or decoding error occurs. |
| --- | --- |
| [CoderMalfunctionError](../java/nio/charset/CoderMalfunctionError.md) | Error thrown when the [decodeLoop](../java/nio/charset/CharsetDecoder.md))method of a [CharsetDecoder](../java/nio/charset/CharsetDecoder.md), or the [encodeLoop](../java/nio/charset/CharsetEncoder.md))method of a [CharsetEncoder](../java/nio/charset/CharsetEncoder.md), throws an unexpected exception. |
| [IllegalCharsetNameException](../java/nio/charset/IllegalCharsetNameException.md) | Unchecked exception thrown when a string that is not a [legal charset name](../java/nio/charset/Charset.md) is used as such. |
| [MalformedInputException](../java/nio/charset/MalformedInputException.md) | Checked exception thrown when an input byte sequence is not legal for given charset, or an input character sequence is not a legal sixteen-bit Unicode sequence. |
| --- | --- |
| [UnmappableCharacterException](../java/nio/charset/UnmappableCharacterException.md) | Checked exception thrown when an input character (or byte) sequence is valid but cannot be mapped to an output byte (or character) sequence. |
| [UnsupportedCharsetException](../java/nio/charset/UnsupportedCharsetException.md) | Unchecked exception thrown when no support is available for a requested charset. |
