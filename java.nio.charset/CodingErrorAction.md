# CodingErrorAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CodingErrorAction

```
open class CodingErrorAction
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.nio.charset.CodingErrorAction](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#) |

A typesafe enumeration for coding-error actions.

Instances of this class are used to specify how malformed-input and unmappable-character errors are to be handled by charset [decoders](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder#cae) and [encoders](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#cae).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#toString())`()` Returns a string describing this action. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [CodingErrorAction](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#)! | [IGNORE](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#IGNORE:java.nio.charset.CodingErrorAction) Action indicating that a coding error is to be handled by dropping the erroneous input and resuming the coding operation. |
| static [CodingErrorAction](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#)! | [REPLACE](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#REPLACE:java.nio.charset.CodingErrorAction) Action indicating that a coding error is to be handled by dropping the erroneous input, appending the coder's replacement value to the output buffer, and resuming the coding operation. |
| static [CodingErrorAction](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#)! | [REPORT](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction#REPORT:java.nio.charset.CodingErrorAction) Action indicating that a coding error is to be reported, either by returning a [CoderResult](https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult) object or by throwing a [CharacterCodingException](https://developer.android.com/reference/kotlin/java/nio/charset/CharacterCodingException), whichever is appropriate for the method implementing the coding process. |

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

Action indicating that a coding error is to be reported, either by returning a [CoderResult](https://developer.android.com/reference/kotlin/java/nio/charset/CoderResult) object or by throwing a [CharacterCodingException](https://developer.android.com/reference/kotlin/java/nio/charset/CharacterCodingException), whichever is appropriate for the method implementing the coding process.
