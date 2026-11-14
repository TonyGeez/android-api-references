# CodingErrorAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CodingErrorAction

```
open class CodingErrorAction
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.charset.CodingErrorAction](../java/nio/charset/CodingErrorAction.md) |

A typesafe enumeration for coding-error actions.

Instances of this class are used to specify how malformed-input and unmappable-character errors are to be handled by charset [decoders](../java/nio/charset/CharsetDecoder.md) and [encoders](../java/nio/charset/CharsetEncoder.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/nio/charset/CodingErrorAction.md))`()` Returns a string describing this action. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)! | [IGNORE](../java/nio/charset/CodingErrorAction.md) Action indicating that a coding error is to be handled by dropping the erroneous input and resuming the coding operation. |
| static [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)! | [REPLACE](../java/nio/charset/CodingErrorAction.md) Action indicating that a coding error is to be handled by dropping the erroneous input, appending the coder's replacement value to the output buffer, and resuming the coding operation. |
| static [CodingErrorAction](../java/nio/charset/CodingErrorAction.md)! | [REPORT](../java/nio/charset/CodingErrorAction.md) Action indicating that a coding error is to be reported, either by returning a [CoderResult](../java/nio/charset/CoderResult.md) object or by throwing a [CharacterCodingException](../java/nio/charset/CharacterCodingException.md), whichever is appropriate for the method implementing the coding process. |
| --- | --- |

## Public methods

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string describing this action.

| Return ||
|----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A descriptive string |

## Properties

### IGNORE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IGNORE: CodingErrorAction!
```

Action indicating that a coding error is to be handled by dropping the erroneous input and resuming the coding operation. 

### REPLACE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPLACE: CodingErrorAction!
```

Action indicating that a coding error is to be handled by dropping the erroneous input, appending the coder's replacement value to the output buffer, and resuming the coding operation. 

### REPORT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT: CodingErrorAction!
```

Action indicating that a coding error is to be reported, either by returning a [CoderResult](../java/nio/charset/CoderResult.md) object or by throwing a [CharacterCodingException](../java/nio/charset/CharacterCodingException.md), whichever is appropriate for the method implementing the coding process.
