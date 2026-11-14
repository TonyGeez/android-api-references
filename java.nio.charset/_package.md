# java.nio.charset

# java.nio.charset

## Classes

| [Charset](Charset.md) | A named mapping between sequences of sixteen-bit Unicode [code units](../java.lang/Character.md) and sequences of bytes. |
| --- | --- |
| [CharsetDecoder](CharsetDecoder.md) | An engine that can transform a sequence of bytes in a specific charset into a sequence of sixteen-bit Unicode characters. |
| [CharsetEncoder](CharsetEncoder.md) | An engine that can transform a sequence of sixteen-bit Unicode characters into a sequence of bytes in a specific charset. |
| [CoderResult](CoderResult.md) | A description of the result state of a coder. |
| --- | --- |
| [CodingErrorAction](CodingErrorAction.md) | A typesafe enumeration for coding-error actions. |
| [StandardCharsets](StandardCharsets.md) | Constant definitions for the standard [Charsets](Charset.md). |

## Exceptions

| [CharacterCodingException](CharacterCodingException.md) | Checked exception thrown when a character encoding or decoding error occurs. |
| --- | --- |
| [CoderMalfunctionError](CoderMalfunctionError.md) | Error thrown when the [decodeLoop](CharsetDecoder.md))method of a [CharsetDecoder](CharsetDecoder.md), or the [encodeLoop](CharsetEncoder.md))method of a [CharsetEncoder](CharsetEncoder.md), throws an unexpected exception. |
| [IllegalCharsetNameException](IllegalCharsetNameException.md) | Unchecked exception thrown when a string that is not a [legal charset name](Charset.md) is used as such. |
| [MalformedInputException](MalformedInputException.md) | Checked exception thrown when an input byte sequence is not legal for given charset, or an input character sequence is not a legal sixteen-bit Unicode sequence. |
| --- | --- |
| [UnmappableCharacterException](UnmappableCharacterException.md) | Checked exception thrown when an input character (or byte) sequence is valid but cannot be mapped to an output byte (or character) sequence. |
| [UnsupportedCharsetException](UnsupportedCharsetException.md) | Unchecked exception thrown when no support is available for a requested charset. |
