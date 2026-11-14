# CodingErrorAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CodingErrorAction

```
open class CodingErrorAction
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.charset.CodingErrorAction](CodingErrorAction.md) |

A typesafe enumeration for coding-error actions.

Instances of this class are used to specify how malformed-input and unmappable-character errors are to be handled by charset [decoders](CharsetDecoder.md) and [encoders](CharsetEncoder.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](CodingErrorAction.md))`()` Returns a string describing this action. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [CodingErrorAction](CodingErrorAction.md)! | [IGNORE](CodingErrorAction.md) Action indicating that a coding error is to be handled by dropping the erroneous input and resuming the coding operation. |
| static [CodingErrorAction](CodingErrorAction.md)! | [REPLACE](CodingErrorAction.md) Action indicating that a coding error is to be handled by dropping the erroneous input, appending the coder's replacement value to the output buffer, and resuming the coding operation. |
| static [CodingErrorAction](CodingErrorAction.md)! | [REPORT](CodingErrorAction.md) Action indicating that a coding error is to be reported, either by returning a [CoderResult](CoderResult.md) object or by throwing a [CharacterCodingException](CharacterCodingException.md), whichever is appropriate for the method implementing the coding process. |
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

Action indicating that a coding error is to be reported, either by returning a [CoderResult](CoderResult.md) object or by throwing a [CharacterCodingException](CharacterCodingException.md), whichever is appropriate for the method implementing the coding process.
