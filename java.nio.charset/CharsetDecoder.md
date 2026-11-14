# CharsetDecoder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CharsetDecoder

```
abstract class CharsetDecoder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.charset.CharsetDecoder](../java/nio/charset/CharsetDecoder.md) |

An engine that can transform a sequence of bytes in a specific charset into a sequence of sixteen-bit Unicode characters.

The input byte sequence is provided in a byte buffer or a series of such buffers. The output character sequence is written to a character buffer or a series of such buffers. A decoder should always be used by making the following sequence of method invocations, hereinafter referred to as a*decoding operation*:

1. Reset the decoder via the [reset](../java/nio/charset/CharsetDecoder.md))method, unless it has not been used before;
2. Invoke the #decode method zero or more times, as long as additional input may be available, passing`false`for the`endOfInput`argument and filling the input buffer and flushing the output buffer between invocations;
3. Invoke the #decode method one final time, passing`true`for the`endOfInput`argument; and then
4. Invoke the [flush](../java/nio/charset/CharsetDecoder.md))method so that the decoder can flush any internal state to the output buffer.

Each invocation of the #decode method will decode as many bytes as possible from the input buffer, writing the resulting characters to the output buffer. The #decode method returns when more input is required, when there is not enough room in the output buffer, or when a decoding error has occurred. In each case a [CoderResult](../java/nio/charset/CoderResult.md) object is returned to describe the reason for termination. An invoker can examine this object and fill the input buffer, flush the output buffer, or attempt to recover from a decoding error, as appropriate, and try again.

There are two general types of decoding errors. If the input byte sequence is not legal for this charset then the input is considered*malformed* . If the input byte sequence is legal but cannot be mapped to a valid Unicode character then an*unmappable character*has been encountered.

How a decoding error is handled depends upon the action requested for that type of error, which is described by an instance of the [CodingErrorAction](../java/nio/charset/CodingErrorAction.md) class. The possible error actions are to [ignore](../java/nio/charset/CodingErrorAction.md) the erroneous input, [report](../java/nio/charset/CodingErrorAction.md) the error to the invoker via the returned [CoderResult](../java/nio/charset/CoderResult.md) object, or [replace](../java/nio/charset/CodingErrorAction.md) the erroneous input with the current value of the replacement string. The replacement has the initial value`"\uFFFD"`; its value may be changed via the [replaceWith](../java/nio/charset/CharsetDecoder.md))method.

The default action for malformed-input and unmappable-character errors is to [report](../java/nio/charset/CodingErrorAction.md) them. The malformed-input error action may be changed via the [onMalformedInput](../java/nio/charset/CharsetDecoder.md))method; the unmappable-character action may be changed via the [onUnmappableCharacter](../java/nio/charset/CharsetDecoder.md))method.

This class is designed to handle many of the details of the decoding process, including the implementation of error actions. A decoder for a specific charset, which is a concrete subclass of this class, need only implement the abstract [decodeLoop](../java/nio/charset/CharsetDecoder.md))method, which encapsulates the basic decoding loop. A subclass that maintains internal state should, additionally, override the [implFlush](../java/nio/charset/CharsetDecoder.md))and [implReset](../java/nio/charset/CharsetDecoder.md))methods.

Instances of this class are not safe for use by multiple concurrent threads.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CharsetDecoder](../java/nio/charset/CharsetDecoder.md))`(`cs:` ` [Charset](../java/nio/charset/Charset.md)!`, `averageCharsPerByte:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `maxCharsPerByte:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Initializes a new decoder. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [averageCharsPerByte](../java/nio/charset/CharsetDecoder.md))`()` Returns the average number of characters that will be produced for each byte of input. |
| [Charset](../java/nio/charset/Charset.md)! | [charset](../java/nio/charset/CharsetDecoder.md))`()` Returns the charset that created this decoder. |
| [CharBuffer](../java/nio/CharBuffer.md)! | [decode](../java/nio/charset/CharsetDecoder.md))`(`in:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` Convenience method that decodes the remaining content of a single input byte buffer into a newly-allocated character buffer. |
| --- | --- |
| [CoderResult](../java/nio/charset/CoderResult.md)! | [decode](../java/nio/charset/CharsetDecoder.md))`(`in:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`, `out:` ` [CharBuffer](../java/nio/CharBuffer.md)!`, `endOfInput:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Decodes as many bytes as possible from the given input buffer, writing the results to the given output buffer. |
| open [Charset](../java/nio/charset/Charset.md)! | [detectedCharset](../java/nio/charset/CharsetDecoder.md))`()` Retrieves the charset that was detected by this decoder*(optional operation)*. |
| [CoderResult](../java/nio/charset/CoderResult.md)! | [flush](../java/nio/charset/CharsetDecoder.md))`(`out:` ` [CharBuffer](../java/nio/CharBuffer.md)!`)` Flushes this decoder. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoDetecting](../java/nio/charset/CharsetDecoder.md))`()` Tells whether or not this decoder implements an auto-detecting charset. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCharsetDetected](../java/nio/charset/CharsetDecoder.md))`()` Tells whether or not this decoder has yet detected a charset*(optional operation)*. |
| open [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)! | [malformedInputAction](../java/nio/charset/CharsetDecoder.md))`()` Returns this decoder's current action for malformed-input errors. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [maxCharsPerByte](../java/nio/charset/CharsetDecoder.md))`()` Returns the maximum number of characters that will be produced for each byte of input. |
| [CharsetDecoder](../java/nio/charset/CharsetDecoder.md)! | [onMalformedInput](../java/nio/charset/CharsetDecoder.md))`(`newAction:` ` [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)!`)` Changes this decoder's action for malformed-input errors. |
| [CharsetDecoder](../java/nio/charset/CharsetDecoder.md)! | [onUnmappableCharacter](../java/nio/charset/CharsetDecoder.md))`(`newAction:` ` [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)!`)` Changes this decoder's action for unmappable-character errors. |
| --- | --- |
| [CharsetDecoder](../java/nio/charset/CharsetDecoder.md)! | [replaceWith](../java/nio/charset/CharsetDecoder.md))`(`newReplacement:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Changes this decoder's replacement value. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [replacement](../java/nio/charset/CharsetDecoder.md))`()` Returns this decoder's replacement value. |
| [CharsetDecoder](../java/nio/charset/CharsetDecoder.md)! | [reset](../java/nio/charset/CharsetDecoder.md))`()` Resets this decoder, clearing any internal state. |
| --- | --- |
| open [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)! | [unmappableCharacterAction](../java/nio/charset/CharsetDecoder.md))`()` Returns this decoder's current action for unmappable-character errors. |

| Protected methods ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CoderResult](../java/nio/charset/CoderResult.md)! | [decodeLoop](../java/nio/charset/CharsetDecoder.md))`(`in:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`, `out:` ` [CharBuffer](../java/nio/CharBuffer.md)!`)` Decodes one or more bytes into one or more characters. |
| open [CoderResult](../java/nio/charset/CoderResult.md)! | [implFlush](../java/nio/charset/CharsetDecoder.md))`(`out:` ` [CharBuffer](../java/nio/CharBuffer.md)!`)` Flushes this decoder. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implOnMalformedInput](../java/nio/charset/CharsetDecoder.md))`(`newAction:` ` [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)!`)` Reports a change to this decoder's malformed-input action. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implOnUnmappableCharacter](../java/nio/charset/CharsetDecoder.md))`(`newAction:` ` [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)!`)` Reports a change to this decoder's unmappable-character action. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implReplaceWith](../java/nio/charset/CharsetDecoder.md))`(`newReplacement:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Reports a change to this decoder's replacement value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implReset](../java/nio/charset/CharsetDecoder.md))`()` Resets this decoder, clearing any charset-specific internal state. |
| --- | --- |

## Protected constructors

### CharsetDecoder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected CharsetDecoder(
    cs: Charset!, 
    averageCharsPerByte: Float, 
    maxCharsPerByte: Float)
```

Initializes a new decoder. The new decoder will have the given chars-per-byte values and its replacement will be the string`"\uFFFD"`.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cs` | [Charset](../java/nio/charset/Charset.md)!:The charset that created this decoder |
| `averageCharsPerByte` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A positive float value indicating the expected number of characters that will be produced for each input byte |
| `maxCharsPerByte` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A positive float value indicating the maximum number of characters that will be produced for each input byte |
| --- | --- |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on the parameters do not hold |

## Public methods

### averageCharsPerByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun averageCharsPerByte(): Float
```

Returns the average number of characters that will be produced for each byte of input. This heuristic value may be used to estimate the size of the output buffer required for a given input sequence.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The average number of characters produced per byte of input |

### charset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun charset(): Charset!
```

Returns the charset that created this decoder.

| Return ||
|-------------------------------------------------------------------------------------|------------------------|
| [Charset](../java/nio/charset/Charset.md)! | This decoder's charset |

### decode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun decode(in: ByteBuffer!): CharBuffer!
```

Convenience method that decodes the remaining content of a single input byte buffer into a newly-allocated character buffer.

This method implements an entire [decoding operation](../java/nio/charset/CharsetDecoder.md); that is, it resets this decoder, then it decodes the bytes in the given byte buffer, and finally it flushes this decoder. This method should therefore not be invoked if a decoding operation is already in progress.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------|
| `in` | [ByteBuffer](../java/nio/ByteBuffer.md)!:The input byte buffer |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharBuffer](../java/nio/CharBuffer.md)! | A newly-allocated character buffer containing the result of the decoding operation. The buffer's position will be zero and its limit will follow the last character written. |

| Exceptions ||
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If a decoding operation is already in progress |
| `java.nio.charset.MalformedInputException` | If the byte sequence starting at the input buffer's current position is not legal for this charset and the current malformed-input action is [CodingErrorAction.REPORT](../java/nio/charset/CodingErrorAction.md) |
| `java.nio.charset.UnmappableCharacterException` | If the byte sequence starting at the input buffer's current position cannot be mapped to an equivalent character sequence and the current unmappable-character action is [java.nio.charset.CodingErrorAction#REPORT](../java/nio/charset/CodingErrorAction.md) |
| --- | --- |
| `java.nio.charset.CoderMalfunctionError` | If an invocation of the decodeLoop method threw an unexpected exception |
| `java.lang.NullPointerException` | if input buffer is null |

### decode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun decode(
    in: ByteBuffer!, 
    out: CharBuffer!, 
    endOfInput: Boolean
): CoderResult!
```

Decodes as many bytes as possible from the given input buffer, writing the results to the given output buffer.

The buffers are read from, and written to, starting at their current positions. At most [in.remaining()](../java/nio/Buffer.md))bytes will be read and at most [out.remaining()](../java/nio/Buffer.md))characters will be written. The buffers' positions will be advanced to reflect the bytes read and the characters written, but their marks and limits will not be modified.

In addition to reading bytes from the input buffer and writing characters to the output buffer, this method returns a [CoderResult](../java/nio/charset/CoderResult.md) object to describe its reason for termination:

- [CoderResult.UNDERFLOW](../java/nio/charset/CoderResult.md) indicates that as much of the input buffer as possible has been decoded. If there is no further input then the invoker can proceed to the next step of the [decoding operation](../java/nio/charset/CharsetDecoder.md). Otherwise this method should be invoked again with further input.
- [CoderResult.OVERFLOW](../java/nio/charset/CoderResult.md) indicates that there is insufficient space in the output buffer to decode any more bytes. This method should be invoked again with an output buffer that has more [remaining](../java/nio/Buffer.md))characters. This is typically done by draining any decoded characters from the output buffer.
- A [malformed-input](../java/nio/charset/CoderResult.md))result indicates that a malformed-input error has been detected. The malformed bytes begin at the input buffer's (possibly incremented) position; the number of malformed bytes may be determined by invoking the result object's [length](../java/nio/charset/CoderResult.md))method. This case applies only if the [malformed action](../java/nio/charset/CharsetDecoder.md))of this decoder is [CodingErrorAction.REPORT](../java/nio/charset/CodingErrorAction.md); otherwise the malformed input will be ignored or replaced, as requested.
- An [unmappable-character](../java/nio/charset/CoderResult.md))result indicates that an unmappable-character error has been detected. The bytes that decode the unmappable character begin at the input buffer's (possibly incremented) position; the number of such bytes may be determined by invoking the result object's [length](../java/nio/charset/CoderResult.md))method. This case applies only if the [unmappable action](../java/nio/charset/CharsetDecoder.md))of this decoder is [java.nio.charset.CodingErrorAction#REPORT](../java/nio/charset/CodingErrorAction.md); otherwise the unmappable character will be ignored or replaced, as requested.

In any case, if this method is to be reinvoked in the same decoding operation then care should be taken to preserve any bytes remaining in the input buffer so that they are available to the next invocation.

The`endOfInput`parameter advises this method as to whether the invoker can provide further input beyond that contained in the given input buffer. If there is a possibility of providing additional input then the invoker should pass`false`for this parameter; if there is no possibility of providing further input then the invoker should pass`true`. It is not erroneous, and in fact it is quite common, to pass`false`in one invocation and later discover that no further input was actually available. It is critical, however, that the final invocation of this method in a sequence of invocations always pass`true`so that any remaining undecoded input will be treated as being malformed.

This method works by invoking the [decodeLoop](../java/nio/charset/CharsetDecoder.md))method, interpreting its results, handling error conditions, and reinvoking it as necessary.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [ByteBuffer](../java/nio/ByteBuffer.md)!:The input byte buffer |
| `out` | [CharBuffer](../java/nio/CharBuffer.md)!:The output character buffer |
| `endOfInput` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if, and only if, the invoker can provide no additional input bytes beyond those in the given buffer |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [CoderResult](../java/nio/charset/CoderResult.md)! | A coder-result object describing the reason for termination |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If a decoding operation is already in progress and the previous step was an invocation neither of the [reset](../java/nio/charset/CharsetDecoder.md))method, nor of this method with a value of`false`for the`endOfInput`parameter, nor of this method with a value of`true`for the`endOfInput`parameter but a return value indicating an incomplete decoding operation |
| `java.nio.charset.CoderMalfunctionError` | If an invocation of the decodeLoop method threw an unexpected exception |
| `java.lang.NullPointerException` | if input or output buffer is null |
| --- | --- |

### detectedCharset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun detectedCharset(): Charset!
```

Retrieves the charset that was detected by this decoder*(optional operation)*.

If this decoder implements an auto-detecting charset then this method returns the actual charset once it has been detected. After that point, this method returns the same value for the duration of the current decoding operation. If not enough input bytes have yet been read to determine the actual charset then this method throws an [IllegalStateException](../java/lang/IllegalStateException.md).

The default implementation of this method always throws an [UnsupportedOperationException](../java/lang/UnsupportedOperationException.md); it should be overridden by auto-detecting decoders to return the appropriate value.

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Charset](../java/nio/charset/Charset.md)! | The charset detected by this auto-detecting decoder, or`null`if the charset has not yet been determined |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------|
| `java.lang.IllegalStateException` | If insufficient bytes have been read to determine a charset |
| `java.lang.UnsupportedOperationException` | If this decoder does not implement an auto-detecting charset |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun flush(out: CharBuffer!): CoderResult!
```

Flushes this decoder.

Some decoders maintain internal state and may need to write some final characters to the output buffer once the overall input sequence has been read.

Any additional output is written to the output buffer beginning at its current position. At most [out.remaining()](../java/nio/Buffer.md))characters will be written. The buffer's position will be advanced appropriately, but its mark and limit will not be modified.

If this method completes successfully then it returns [java.nio.charset.CoderResult#UNDERFLOW](../java/nio/charset/CoderResult.md). If there is insufficient room in the output buffer then it returns [CoderResult.OVERFLOW](../java/nio/charset/CoderResult.md). If this happens then this method must be invoked again, with an output buffer that has more room, in order to complete the current [decoding operation](../java/nio/charset/CharsetDecoder.md).

If this decoder has already been flushed then invoking this method has no effect.

This method invokes the [implFlush](../java/nio/charset/CharsetDecoder.md))method to perform the actual flushing operation.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `out` | [CharBuffer](../java/nio/CharBuffer.md)!:The output character buffer |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CoderResult](../java/nio/charset/CoderResult.md)! | A coder-result object, either [CoderResult.UNDERFLOW](../java/nio/charset/CoderResult.md) or [CoderResult.OVERFLOW](../java/nio/charset/CoderResult.md) |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the previous step of the current decoding operation was an invocation neither of the [flush](../java/nio/charset/CharsetDecoder.md))method nor of the three-argument [decode](../java/nio/charset/CharsetDecoder.md))method with a value of`true`for the`endOfInput`parameter |

### isAutoDetecting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAutoDetecting(): Boolean
```

Tells whether or not this decoder implements an auto-detecting charset.

The default implementation of this method always returns`false`; it should be overridden by auto-detecting decoders to return`true`.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this decoder implements an auto-detecting charset |

### isCharsetDetected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCharsetDetected(): Boolean
```

Tells whether or not this decoder has yet detected a charset*(optional operation)*.

If this decoder implements an auto-detecting charset then at a single point during a decoding operation this method may start returning`true`to indicate that a specific charset has been detected in the input byte sequence. Once this occurs, the [detectedCharset](../java/nio/charset/CharsetDecoder.md))method may be invoked to retrieve the detected charset.

That this method returns`false`does not imply that no bytes have yet been decoded. Some auto-detecting decoders are capable of decoding some, or even all, of an input byte sequence without fixing on a particular charset.

The default implementation of this method always throws an [UnsupportedOperationException](../java/lang/UnsupportedOperationException.md); it should be overridden by auto-detecting decoders to return`true`once the input charset has been determined.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this decoder has detected a specific charset |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If this decoder does not implement an auto-detecting charset |

### malformedInputAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun malformedInputAction(): CodingErrorAction!
```

Returns this decoder's current action for malformed-input errors.

| Return ||
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)! | The current malformed-input action, which is never`null` |

### maxCharsPerByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun maxCharsPerByte(): Float
```

Returns the maximum number of characters that will be produced for each byte of input. This value may be used to compute the worst-case size of the output buffer required for a given input sequence. This value accounts for any necessary content-independent prefix or suffix characters.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The maximum number of characters that will be produced per byte of input |

### onMalformedInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onMalformedInput(newAction: CodingErrorAction!): CharsetDecoder!
```

Changes this decoder's action for malformed-input errors.

This method invokes the [implOnMalformedInput](../java/nio/charset/CharsetDecoder.md))method, passing the new action.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `newAction` | [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)!:The new action; must not be`null` |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------|
| [CharsetDecoder](../java/nio/charset/CharsetDecoder.md)! | This decoder |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the precondition on the parameter does not hold |

### onUnmappableCharacter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onUnmappableCharacter(newAction: CodingErrorAction!): CharsetDecoder!
```

Changes this decoder's action for unmappable-character errors.

This method invokes the [implOnUnmappableCharacter](../java/nio/charset/CharsetDecoder.md))method, passing the new action.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `newAction` | [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)!:The new action; must not be`null` |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------|
| [CharsetDecoder](../java/nio/charset/CharsetDecoder.md)! | This decoder |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the precondition on the parameter does not hold |

### replaceWith

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun replaceWith(newReplacement: String!): CharsetDecoder!
```

Changes this decoder's replacement value.

This method invokes the [implReplaceWith](../java/nio/charset/CharsetDecoder.md))method, passing the new replacement, after checking that the new replacement is acceptable.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newReplacement` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The new replacement; must not be`null`, must have non-zero length, and must not be longer than the value returned by the [maxCharsPerByte](../java/nio/charset/CharsetDecoder.md))method |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------|
| [CharsetDecoder](../java/nio/charset/CharsetDecoder.md)! | This decoder |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on the parameter do not hold |

### replacement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun replacement(): String!
```

Returns this decoder's replacement value.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | This decoder's current replacement, which is never`null`and is never empty |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reset(): CharsetDecoder!
```

Resets this decoder, clearing any internal state.

This method resets charset-independent state and also invokes the [implReset](../java/nio/charset/CharsetDecoder.md))method in order to perform any charset-specific reset actions.

| Return ||
|----------------------------------------------------------------------------------------------------|--------------|
| [CharsetDecoder](../java/nio/charset/CharsetDecoder.md)! | This decoder |

### unmappableCharacterAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unmappableCharacterAction(): CodingErrorAction!
```

Returns this decoder's current action for unmappable-character errors.

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)! | The current unmappable-character action, which is never`null` |

## Protected methods

### decodeLoop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun decodeLoop(
    in: ByteBuffer!, 
    out: CharBuffer!
): CoderResult!
```

Decodes one or more bytes into one or more characters.

This method encapsulates the basic decoding loop, decoding as many bytes as possible until it either runs out of input, runs out of room in the output buffer, or encounters a decoding error. This method is invoked by the #decode method, which handles result interpretation and error recovery.

The buffers are read from, and written to, starting at their current positions. At most [in.remaining()](../java/nio/Buffer.md))bytes will be read, and at most [out.remaining()](../java/nio/Buffer.md))characters will be written. The buffers' positions will be advanced to reflect the bytes read and the characters written, but their marks and limits will not be modified.

This method returns a [CoderResult](../java/nio/charset/CoderResult.md) object to describe its reason for termination, in the same manner as the #decode method. Most implementations of this method will handle decoding errors by returning an appropriate result object for interpretation by the #decode method. An optimized implementation may instead examine the relevant error action and implement that action itself.

An implementation of this method may perform arbitrary lookahead by returning [CoderResult.UNDERFLOW](../java/nio/charset/CoderResult.md) until it receives sufficient input.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `in` | [ByteBuffer](../java/nio/ByteBuffer.md)!:The input byte buffer |
| `out` | [CharBuffer](../java/nio/CharBuffer.md)!:The output character buffer |

| Return ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [CoderResult](../java/nio/charset/CoderResult.md)! | A coder-result object describing the reason for termination |

### implFlush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun implFlush(out: CharBuffer!): CoderResult!
```

Flushes this decoder.

The default implementation of this method does nothing, and always returns [CoderResult.UNDERFLOW](../java/nio/charset/CoderResult.md). This method should be overridden by decoders that may need to write final characters to the output buffer once the entire input sequence has been read.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `out` | [CharBuffer](../java/nio/CharBuffer.md)!:The output character buffer |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CoderResult](../java/nio/charset/CoderResult.md)! | A coder-result object, either [CoderResult.UNDERFLOW](../java/nio/charset/CoderResult.md) or [CoderResult.OVERFLOW](../java/nio/charset/CoderResult.md) |

### implOnMalformedInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun implOnMalformedInput(newAction: CodingErrorAction!): Unit
```

Reports a change to this decoder's malformed-input action.

The default implementation of this method does nothing. This method should be overridden by decoders that require notification of changes to the malformed-input action.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------|
| `newAction` | [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)!:The new action |

### implOnUnmappableCharacter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun implOnUnmappableCharacter(newAction: CodingErrorAction!): Unit
```

Reports a change to this decoder's unmappable-character action.

The default implementation of this method does nothing. This method should be overridden by decoders that require notification of changes to the unmappable-character action.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------|
| `newAction` | [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)!:The new action |

### implReplaceWith

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun implReplaceWith(newReplacement: String!): Unit
```

Reports a change to this decoder's replacement value.

The default implementation of this method does nothing. This method should be overridden by decoders that require notification of changes to the replacement.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------|
| `newReplacement` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The replacement value |

### implReset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun implReset(): Unit
```

Resets this decoder, clearing any charset-specific internal state.

The default implementation of this method does nothing. This method should be overridden by decoders that maintain internal state.
