# CoderResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CoderResult

```
open class CoderResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.charset.CoderResult](../java/nio/charset/CoderResult.md) |

A description of the result state of a coder.

A charset coder, that is, either a decoder or an encoder, consumes bytes (or characters) from an input buffer, translates them, and writes the resulting characters (or bytes) to an output buffer. A coding process terminates for one of four categories of reasons, which are described by instances of this class:

- *Underflow* is reported when there is no more input to be processed, or there is insufficient input and additional input is required. This condition is represented by the unique result object [UNDERFLOW](../java/nio/charset/CoderResult.md), whose [isUnderflow](../java/nio/charset/CoderResult.md))method returns`true`.
- *Overflow* is reported when there is insufficient room remaining in the output buffer. This condition is represented by the unique result object [OVERFLOW](../java/nio/charset/CoderResult.md), whose [isOverflow](../java/nio/charset/CoderResult.md))method returns`true`.
- A*malformed-input error* is reported when a sequence of input units is not well-formed. Such errors are described by instances of this class whose [isMalformed](../java/nio/charset/CoderResult.md))method returns`true`and whose [length](../java/nio/charset/CoderResult.md))method returns the length of the malformed sequence. There is one unique instance of this class for all malformed-input errors of a given length.
- An*unmappable-character error* is reported when a sequence of input units denotes a character that cannot be represented in the output charset. Such errors are described by instances of this class whose [isUnmappable](../java/nio/charset/CoderResult.md))method returns`true`and whose [length](../java/nio/charset/CoderResult.md))method returns the length of the input sequence denoting the unmappable character. There is one unique instance of this class for all unmappable-character errors of a given length.

For convenience, the [isError](../java/nio/charset/CoderResult.md))method returns`true`for result objects that describe malformed-input and unmappable-character errors but`false`for those that describe underflow or overflow conditions.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isError](../java/nio/charset/CoderResult.md))`()` Tells whether or not this object describes an error condition. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMalformed](../java/nio/charset/CoderResult.md))`()` Tells whether or not this object describes a malformed-input error. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOverflow](../java/nio/charset/CoderResult.md))`()` Tells whether or not this object describes an overflow condition. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUnderflow](../java/nio/charset/CoderResult.md))`()` Tells whether or not this object describes an underflow condition. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUnmappable](../java/nio/charset/CoderResult.md))`()` Tells whether or not this object describes an unmappable-character error. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](../java/nio/charset/CoderResult.md))`()` Returns the length of the erroneous input described by this object*(optional operation)*. |
| --- | --- |
| openstatic [CoderResult](../java/nio/charset/CoderResult.md)! | [malformedForLength](../java/nio/charset/CoderResult.md))`(`length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Static factory method that returns the unique object describing a malformed-input error of the given length. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [throwException](../java/nio/charset/CoderResult.md))`()` Throws an exception appropriate to the result described by this object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/nio/charset/CoderResult.md))`()` Returns a string describing this coder result. |
| --- | --- |
| openstatic [CoderResult](../java/nio/charset/CoderResult.md)! | [unmappableForLength](../java/nio/charset/CoderResult.md))`(`length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Static factory method that returns the unique result object describing an unmappable-character error of the given length. |

| Properties ||
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [CoderResult](../java/nio/charset/CoderResult.md)! | [OVERFLOW](../java/nio/charset/CoderResult.md) Result object indicating overflow, meaning that there is insufficient room in the output buffer. |
| static [CoderResult](../java/nio/charset/CoderResult.md)! | [UNDERFLOW](../java/nio/charset/CoderResult.md) Result object indicating underflow, meaning that either the input buffer has been completely consumed or, if the input buffer is not yet empty, that additional input is required. |

## Public methods

### isError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isError(): Boolean
```

Tells whether or not this object describes an error condition.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this object denotes either a malformed-input error or an unmappable-character error |

### isMalformed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMalformed(): Boolean
```

Tells whether or not this object describes a malformed-input error.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this object denotes a malformed-input error |

### isOverflow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOverflow(): Boolean
```

Tells whether or not this object describes an overflow condition.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this object denotes overflow |

### isUnderflow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUnderflow(): Boolean
```

Tells whether or not this object describes an underflow condition.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this object denotes underflow |

### isUnmappable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUnmappable(): Boolean
```

Tells whether or not this object describes an unmappable-character error.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this object denotes an unmappable-character error |

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun length(): Int
```

Returns the length of the erroneous input described by this object*(optional operation)*.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The length of the erroneous input, a positive integer |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If this object does not describe an error condition, that is, if the [isError](../java/nio/charset/CoderResult.md))does not return`true` |

### malformedForLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun malformedForLength(length: Int): CoderResult!
```

Static factory method that returns the unique object describing a malformed-input error of the given length.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------|
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The given length |

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------|
| [CoderResult](../java/nio/charset/CoderResult.md)! | The requested coder-result object |

### throwException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun throwException(): Unit
```

Throws an exception appropriate to the result described by this object.

| Exceptions ||
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.BufferUnderflowException` | If this object is [UNDERFLOW](../java/nio/charset/CoderResult.md) |
| `java.nio.BufferOverflowException` | If this object is [OVERFLOW](../java/nio/charset/CoderResult.md) |
| `java.nio.charset.MalformedInputException` | If this object represents a malformed-input error; the exception's length value will be that of this object |
| --- | --- |
| `java.nio.charset.UnmappableCharacterException` | If this object represents an unmappable-character error; the exceptions length value will be that of this object |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string describing this coder result.

| Return ||
|----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A descriptive string |

### unmappableForLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun unmappableForLength(length: Int): CoderResult!
```

Static factory method that returns the unique result object describing an unmappable-character error of the given length.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------|
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The given length |

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------|
| [CoderResult](../java/nio/charset/CoderResult.md)! | The requested coder-result object |

## Properties

### OVERFLOW

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OVERFLOW: CoderResult!
```

Result object indicating overflow, meaning that there is insufficient room in the output buffer. 

### UNDERFLOW

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDERFLOW: CoderResult!
```

Result object indicating underflow, meaning that either the input buffer has been completely consumed or, if the input buffer is not yet empty, that additional input is required.
