Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CharsetEncoder

```
abstract class CharsetEncoder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.nio.charset.CharsetEncoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#) |

An engine that can transform a sequence of sixteen-bit Unicode characters into a sequence of bytes in a specific charset.

The input character sequence is provided in a character buffer or a series of such buffers. The output byte sequence is written to a byte buffer or a series of such buffers. An encoder should always be used by making the following sequence of method invocations, hereinafter referred to as an *encoding operation*:

1. Reset the encoder via the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#reset()` method, unless it has not been used before;
2. Invoke the #encode method zero or more times, as long as additional input may be available, passing `false` for the `endOfInput` argument and filling the input buffer and flushing the output buffer between invocations;
3. Invoke the #encode method one final time, passing `true` for the `endOfInput` argument; and then
4. Invoke the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#flush(java.nio.ByteBuffer)` method so that the encoder can flush any internal state to the output buffer.

Each invocation of the #encode method will encode as many characters as possible from the input buffer, writing the resulting bytes to the output buffer. The #encode method returns when more input is required, when there is not enough room in the output buffer, or when an encoding error has occurred. In each case a `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult` object is returned to describe the reason for termination. An invoker can examine this object and fill the input buffer, flush the output buffer, or attempt to recover from an encoding error, as appropriate, and try again.

There are two general types of encoding errors. If the input character sequence is not a legal sixteen-bit Unicode sequence then the input is considered *malformed* . If the input character sequence is legal but cannot be mapped to a valid byte sequence in the given charset then an *unmappable character* has been encountered.

How an encoding error is handled depends upon the action requested for that type of error, which is described by an instance of the `https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction` class. The possible error actions are to [ignore](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#IGNORE:java.nio.charset.CodingErrorAction) the erroneous input, [report](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#REPORT:java.nio.charset.CodingErrorAction) the error to the invoker via the returned `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult` object, or [replace](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#REPLACE:java.nio.charset.CodingErrorAction) the erroneous input with the current value of the replacement byte array. The replacement is initially set to the encoder's default replacement, which often (but not always) has the initial value `{` `(byte)'?'` `}`; its value may be changed via the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#replaceWith(kotlin.ByteArray)` method.

The default action for malformed-input and unmappable-character errors is to [report](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#REPORT:java.nio.charset.CodingErrorAction) them. The malformed-input error action may be changed via the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#onMalformedInput(java.nio.charset.CodingErrorAction)` method; the unmappable-character action may be changed via the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#onUnmappableCharacter(java.nio.charset.CodingErrorAction)` method.

This class is designed to handle many of the details of the encoding process, including the implementation of error actions. An encoder for a specific charset, which is a concrete subclass of this class, need only implement the abstract `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#encodeLoop(java.nio.CharBuffer,%20java.nio.ByteBuffer)` method, which encapsulates the basic encoding loop. A subclass that maintains internal state should, additionally, override the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#implFlush(java.nio.ByteBuffer)` and `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#implReset()` methods.

Instances of this class are not safe for use by multiple concurrent threads.

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#CharsetEncoder(java.nio.charset.Charset,%20kotlin.Float,%20kotlin.Float)(cs: https://developer.android.com/reference/kotlin/java/nio/charset/Charset!, averageBytesPerChar: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, maxBytesPerChar: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Initializes a new encoder. |
| `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#CharsetEncoder(java.nio.charset.Charset,%20kotlin.Float,%20kotlin.Float,%20kotlin.ByteArray)(cs: https://developer.android.com/reference/kotlin/java/nio/charset/Charset!, averageBytesPerChar: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, maxBytesPerChar: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, replacement: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Initializes a new encoder. |

| Public methods ||
|---|---|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#averageBytesPerChar()()` Returns the average number of bytes that will be produced for each character of input. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#canEncode(kotlin.Char)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Tells whether or not this encoder can encode the given character. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#canEncode(kotlin.CharSequence)(cs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Tells whether or not this encoder can encode the given character sequence. |
| [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset)! | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#charset()()` Returns the charset that created this encoder. |
| [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)! | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#encode(java.nio.CharBuffer)(in: https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#!)` Convenience method that encodes the remaining content of a single input character buffer into a newly-allocated byte buffer. |
| [CoderResult](https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult)! | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#encode(java.nio.CharBuffer,%20java.nio.ByteBuffer,%20kotlin.Boolean)(in: https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#!, out: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!, endOfInput: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Encodes as many characters as possible from the given input buffer, writing the results to the given output buffer. |
| [CoderResult](https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult)! | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#flush(java.nio.ByteBuffer)(out: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!)` Flushes this encoder. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#isLegalReplacement(kotlin.ByteArray)(repl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Tells whether or not the given byte array is a legal replacement value for this encoder. |
| open [CodingErrorAction](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction)! | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#malformedInputAction()()` Returns this encoder's current action for malformed-input errors. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#maxBytesPerChar()()` Returns the maximum number of bytes that will be produced for each character of input. |
| [CharsetEncoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#)! | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#onMalformedInput(java.nio.charset.CodingErrorAction)(newAction: https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction!)` Changes this encoder's action for malformed-input errors. |
| [CharsetEncoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#)! | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#onUnmappableCharacter(java.nio.charset.CodingErrorAction)(newAction: https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction!)` Changes this encoder's action for unmappable-character errors. |
| [CharsetEncoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#)! | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#replaceWith(kotlin.ByteArray)(newReplacement: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Changes this encoder's replacement value. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#replacement()()` Returns this encoder's replacement value. |
| [CharsetEncoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#)! | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#reset()()` Resets this encoder, clearing any internal state. |
| open [CodingErrorAction](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction)! | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#unmappableCharacterAction()()` Returns this encoder's current action for unmappable-character errors. |

| Protected methods ||
|---|---|
| abstract [CoderResult](https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult)! | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#encodeLoop(java.nio.CharBuffer,%20java.nio.ByteBuffer)(in: https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#!, out: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!)` Encodes one or more characters into one or more bytes. |
| open [CoderResult](https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult)! | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#implFlush(java.nio.ByteBuffer)(out: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!)` Flushes this encoder. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#implOnMalformedInput(java.nio.charset.CodingErrorAction)(newAction: https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction!)` Reports a change to this encoder's malformed-input action. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#implOnUnmappableCharacter(java.nio.charset.CodingErrorAction)(newAction: https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction!)` Reports a change to this encoder's unmappable-character action. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#implReplaceWith(kotlin.ByteArray)(newReplacement: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Reports a change to this encoder's replacement value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#implReset()()` Resets this encoder, clearing any charset-specific internal state. |

## Protected constructors

### CharsetEncoder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected CharsetEncoder(
    cs: Charset!, 
    averageBytesPerChar: Float, 
    maxBytesPerChar: Float)
```

Initializes a new encoder. The new encoder will have the given bytes-per-char values and its replacement will be the byte array `{` `(byte)'?'` `}`.

| Parameters ||
|---|---|
| `cs` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset)!: The charset that created this encoder |
| `averageBytesPerChar` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): A positive float value indicating the expected number of bytes that will be produced for each input character |
| `maxBytesPerChar` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): A positive float value indicating the maximum number of bytes that will be produced for each input character |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the preconditions on the parameters do not hold |

### CharsetEncoder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected CharsetEncoder(
    cs: Charset!, 
    averageBytesPerChar: Float, 
    maxBytesPerChar: Float, 
    replacement: ByteArray!)
```

Initializes a new encoder. The new encoder will have the given bytes-per-char and replacement values.

| Parameters ||
|---|---|
| `cs` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset)!: The charset that created this encoder |
| `averageBytesPerChar` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): A positive float value indicating the expected number of bytes that will be produced for each input character |
| `maxBytesPerChar` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): A positive float value indicating the maximum number of bytes that will be produced for each input character |
| `replacement` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The initial replacement; must not be `null`, must have non-zero length, must not be longer than maxBytesPerChar, and must be [legal](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#isLegalReplacement(kotlin.ByteArray)) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the preconditions on the parameters do not hold |

## Public methods

### averageBytesPerChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun averageBytesPerChar(): Float
```

Returns the average number of bytes that will be produced for each character of input. This heuristic value may be used to estimate the size of the output buffer required for a given input sequence.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The average number of bytes produced per character of input |

### canEncode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canEncode(c: Char): Boolean
```

Tells whether or not this encoder can encode the given character.

This method returns `false` if the given character is a surrogate character; such characters can be interpreted only when they are members of a pair consisting of a high surrogate followed by a low surrogate. The `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#canEncode(kotlin.CharSequence)` method may be used to test whether or not a character sequence can be encoded.

This method may modify this encoder's state; it should therefore not be invoked if an [encoding operation](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#steps) is already in progress.

The default implementation of this method is not very efficient; it should generally be overridden to improve performance.

| Parameters ||
|---|---|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The given character |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if, and only if, this encoder can encode the given character |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If an encoding operation is already in progress |

### canEncode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canEncode(cs: CharSequence!): Boolean
```

Tells whether or not this encoder can encode the given character sequence.

If this method returns `false` for a particular character sequence then more information about why the sequence cannot be encoded may be obtained by performing a full [encoding operation](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#steps).

This method may modify this encoder's state; it should therefore not be invoked if an encoding operation is already in progress.

The default implementation of this method is not very efficient; it should generally be overridden to improve performance.

| Parameters ||
|---|---|
| `cs` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The given character sequence |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if, and only if, this encoder can encode the given character without throwing any exceptions and without performing any replacements |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If an encoding operation is already in progress |

### charset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun charset(): Charset!
```

Returns the charset that created this encoder.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/Charset!` | This encoder's charset |

### encode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun encode(in: CharBuffer!): ByteBuffer!
```

Convenience method that encodes the remaining content of a single input character buffer into a newly-allocated byte buffer.

This method implements an entire [encoding operation](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#steps); that is, it resets this encoder, then it encodes the characters in the given character buffer, and finally it flushes this encoder. This method should therefore not be invoked if an encoding operation is already in progress.

| Parameters ||
|---|---|
| `in` | [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#)!: The input character buffer |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!` | A newly-allocated byte buffer containing the result of the encoding operation. The buffer's position will be zero and its limit will follow the last byte written. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If an encoding operation is already in progress |
| `java.lang.NullPointerException` | if input buffer is null |
| `java.nio.charset.CoderMalfunctionError` | If an invocation of the encodeLoop method threw an unexpected exception |
| `java.nio.charset.MalformedInputException` | If the character sequence starting at the input buffer's current position is not a legal sixteen-bit Unicode sequence and the current malformed-input action is `https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#REPORT:java.nio.charset.CodingErrorAction` |
| `java.nio.charset.UnmappableCharacterException` | If the character sequence starting at the input buffer's current position cannot be mapped to an equivalent byte sequence and the current unmappable-character action is `https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#REPORT:java.nio.charset.CodingErrorAction` |

### encode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun encode(
    in: CharBuffer!, 
    out: ByteBuffer!, 
    endOfInput: Boolean
): CoderResult!
```

Encodes as many characters as possible from the given input buffer, writing the results to the given output buffer.

The buffers are read from, and written to, starting at their current positions. At most `https://developer.android.com/reference/kotlin/java/nio/Buffer.html#remaining()` characters will be read and at most `https://developer.android.com/reference/kotlin/java/nio/Buffer.html#remaining()` bytes will be written. The buffers' positions will be advanced to reflect the characters read and the bytes written, but their marks and limits will not be modified.

In addition to reading characters from the input buffer and writing bytes to the output buffer, this method returns a `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult` object to describe its reason for termination:

- `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult#UNDERFLOW:java.nio.charset.CoderResult` indicates that as much of the input buffer as possible has been encoded. If there is no further input then the invoker can proceed to the next step of the [encoding operation](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#steps). Otherwise this method should be invoked again with further input.
- `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult#OVERFLOW:java.nio.charset.CoderResult` indicates that there is insufficient space in the output buffer to encode any more characters. This method should be invoked again with an output buffer that has more [remaining](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#remaining()) bytes. This is typically done by draining any encoded bytes from the output buffer.
- A [malformed-input](https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult#malformedForLength(kotlin.Int)) result indicates that a malformed-input error has been detected. The malformed characters begin at the input buffer's (possibly incremented) position; the number of malformed characters may be determined by invoking the result object's `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult#length()` method. This case applies only if the [malformed action](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#onMalformedInput(java.nio.charset.CodingErrorAction)) of this encoder is `https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#REPORT:java.nio.charset.CodingErrorAction`; otherwise the malformed input will be ignored or replaced, as requested.
- An [unmappable-character](https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult#unmappableForLength(kotlin.Int)) result indicates that an unmappable-character error has been detected. The characters that encode the unmappable character begin at the input buffer's (possibly incremented) position; the number of such characters may be determined by invoking the result object's `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult#length()` method. This case applies only if the [unmappable action](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#onUnmappableCharacter(java.nio.charset.CodingErrorAction)) of this encoder is `https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#REPORT:java.nio.charset.CodingErrorAction`; otherwise the unmappable character will be ignored or replaced, as requested.

In any case, if this method is to be reinvoked in the same encoding operation then care should be taken to preserve any characters remaining in the input buffer so that they are available to the next invocation.

The `endOfInput` parameter advises this method as to whether the invoker can provide further input beyond that contained in the given input buffer. If there is a possibility of providing additional input then the invoker should pass `false` for this parameter; if there is no possibility of providing further input then the invoker should pass `true`. It is not erroneous, and in fact it is quite common, to pass `false` in one invocation and later discover that no further input was actually available. It is critical, however, that the final invocation of this method in a sequence of invocations always pass `true` so that any remaining unencoded input will be treated as being malformed.

This method works by invoking the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#encodeLoop(java.nio.CharBuffer,%20java.nio.ByteBuffer)` method, interpreting its results, handling error conditions, and reinvoking it as necessary.

| Parameters ||
|---|---|
| `in` | [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#)!: The input character buffer |
| `out` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!: The output byte buffer |
| `endOfInput` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if, and only if, the invoker can provide no additional input characters beyond those in the given buffer |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult!` | A coder-result object describing the reason for termination |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If an encoding operation is already in progress and the previous step was an invocation neither of the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#reset()` method, nor of this method with a value of `false` for the `endOfInput` parameter, nor of this method with a value of `true` for the `endOfInput` parameter but a return value indicating an incomplete encoding operation |
| `java.lang.NullPointerException` | if input or output buffer is null |
| `java.nio.charset.CoderMalfunctionError` | If an invocation of the encodeLoop method threw an unexpected exception |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun flush(out: ByteBuffer!): CoderResult!
```

Flushes this encoder.

Some encoders maintain internal state and may need to write some final bytes to the output buffer once the overall input sequence has been read.

Any additional output is written to the output buffer beginning at its current position. At most `https://developer.android.com/reference/kotlin/java/nio/Buffer.html#remaining()` bytes will be written. The buffer's position will be advanced appropriately, but its mark and limit will not be modified.

If this method completes successfully then it returns `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult#UNDERFLOW:java.nio.charset.CoderResult`. If there is insufficient room in the output buffer then it returns `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult#OVERFLOW:java.nio.charset.CoderResult`. If this happens then this method must be invoked again, with an output buffer that has more room, in order to complete the current [encoding operation](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#steps).

If this encoder has already been flushed then invoking this method has no effect.

This method invokes the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#implFlush(java.nio.ByteBuffer)` method to perform the actual flushing operation.

| Parameters ||
|---|---|
| `out` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!: The output byte buffer |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult!` | A coder-result object, either `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult#UNDERFLOW:java.nio.charset.CoderResult` or `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult#OVERFLOW:java.nio.charset.CoderResult` |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If the previous step of the current encoding operation was an invocation neither of the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#flush(java.nio.ByteBuffer)` method nor of the three-argument `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#encode(java.nio.CharBuffer,%20java.nio.ByteBuffer,%20kotlin.Boolean)` method with a value of `true` for the `endOfInput` parameter |

### isLegalReplacement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isLegalReplacement(repl: ByteArray!): Boolean
```

Tells whether or not the given byte array is a legal replacement value for this encoder.

A replacement is legal if, and only if, it is a legal sequence of bytes in this encoder's charset; that is, it must be possible to decode the replacement into one or more sixteen-bit Unicode characters.

The default implementation of this method is not very efficient; it should generally be overridden to improve performance.

| Parameters ||
|---|---|
| `repl` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The byte array to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if, and only if, the given byte array is a legal replacement value for this encoder |

### malformedInputAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun malformedInputAction(): CodingErrorAction!
```

Returns this encoder's current action for malformed-input errors.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction!` | The current malformed-input action, which is never `null` |

### maxBytesPerChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun maxBytesPerChar(): Float
```

Returns the maximum number of bytes that will be produced for each character of input. This value may be used to compute the worst-case size of the output buffer required for a given input sequence. This value accounts for any necessary content-independent prefix or suffix bytes, such as byte-order marks.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The maximum number of bytes that will be produced per character of input |

### onMalformedInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun onMalformedInput(newAction: CodingErrorAction!): CharsetEncoder!
```

Changes this encoder's action for malformed-input errors.

This method invokes the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#implOnMalformedInput(java.nio.charset.CodingErrorAction)` method, passing the new action.

| Parameters ||
|---|---|
| `newAction` | [CodingErrorAction](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction)!: The new action; must not be `null` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#!` | This encoder |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the precondition on the parameter does not hold |

### onUnmappableCharacter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun onUnmappableCharacter(newAction: CodingErrorAction!): CharsetEncoder!
```

Changes this encoder's action for unmappable-character errors.

This method invokes the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#implOnUnmappableCharacter(java.nio.charset.CodingErrorAction)` method, passing the new action.

| Parameters ||
|---|---|
| `newAction` | [CodingErrorAction](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction)!: The new action; must not be `null` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#!` | This encoder |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the precondition on the parameter does not hold |

### replaceWith

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun replaceWith(newReplacement: ByteArray!): CharsetEncoder!
```

Changes this encoder's replacement value.

This method invokes the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#implReplaceWith(kotlin.ByteArray)` method, passing the new replacement, after checking that the new replacement is acceptable.

| Parameters ||
|---|---|
| `newReplacement` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The new replacement; must not be `null`, must have non-zero length, must not be longer than the value returned by the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#maxBytesPerChar()` method, and must be `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#isLegalReplacement(kotlin.ByteArray)` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#!` | This encoder |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the preconditions on the parameter do not hold |

### replacement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun replacement(): ByteArray!
```

Returns this encoder's replacement value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | This encoder's current replacement, which is never `null` and is never empty |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reset(): CharsetEncoder!
```

Resets this encoder, clearing any internal state.

This method resets charset-independent state and also invokes the `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#implReset()` method in order to perform any charset-specific reset actions.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#!` | This encoder |

### unmappableCharacterAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unmappableCharacterAction(): CodingErrorAction!
```

Returns this encoder's current action for unmappable-character errors.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction!` | The current unmappable-character action, which is never `null` |

## Protected methods

### encodeLoop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun encodeLoop(
    in: CharBuffer!, 
    out: ByteBuffer!
): CoderResult!
```

Encodes one or more characters into one or more bytes.

This method encapsulates the basic encoding loop, encoding as many characters as possible until it either runs out of input, runs out of room in the output buffer, or encounters an encoding error. This method is invoked by the #encode method, which handles result interpretation and error recovery.

The buffers are read from, and written to, starting at their current positions. At most `https://developer.android.com/reference/kotlin/java/nio/Buffer.html#remaining()` characters will be read, and at most `https://developer.android.com/reference/kotlin/java/nio/Buffer.html#remaining()` bytes will be written. The buffers' positions will be advanced to reflect the characters read and the bytes written, but their marks and limits will not be modified.

This method returns a `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult` object to describe its reason for termination, in the same manner as the #encode method. Most implementations of this method will handle encoding errors by returning an appropriate result object for interpretation by the #encode method. An optimized implementation may instead examine the relevant error action and implement that action itself.

An implementation of this method may perform arbitrary lookahead by returning `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult#UNDERFLOW:java.nio.charset.CoderResult` until it receives sufficient input.

| Parameters ||
|---|---|
| `in` | [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#)!: The input character buffer |
| `out` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!: The output byte buffer |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult!` | A coder-result object describing the reason for termination |

### implFlush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun implFlush(out: ByteBuffer!): CoderResult!
```

Flushes this encoder.

The default implementation of this method does nothing, and always returns `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult#UNDERFLOW:java.nio.charset.CoderResult`. This method should be overridden by encoders that may need to write final bytes to the output buffer once the entire input sequence has been read.

| Parameters ||
|---|---|
| `out` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!: The output byte buffer |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult!` | A coder-result object, either `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult#UNDERFLOW:java.nio.charset.CoderResult` or `https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult#OVERFLOW:java.nio.charset.CoderResult` |

### implOnMalformedInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun implOnMalformedInput(newAction: CodingErrorAction!): Unit
```

Reports a change to this encoder's malformed-input action.

The default implementation of this method does nothing. This method should be overridden by encoders that require notification of changes to the malformed-input action.

| Parameters ||
|---|---|
| `newAction` | [CodingErrorAction](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction)!: The new action |

### implOnUnmappableCharacter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun implOnUnmappableCharacter(newAction: CodingErrorAction!): Unit
```

Reports a change to this encoder's unmappable-character action.

The default implementation of this method does nothing. This method should be overridden by encoders that require notification of changes to the unmappable-character action.

| Parameters ||
|---|---|
| `newAction` | [CodingErrorAction](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction)!: The new action |

### implReplaceWith

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun implReplaceWith(newReplacement: ByteArray!): Unit
```

Reports a change to this encoder's replacement value.

The default implementation of this method does nothing. This method should be overridden by encoders that require notification of changes to the replacement.

| Parameters ||
|---|---|
| `newReplacement` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The replacement value |

### implReset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun implReset(): Unit
```

Resets this encoder, clearing any charset-specific internal state.

The default implementation of this method does nothing. This method should be overridden by encoders that maintain internal state.
