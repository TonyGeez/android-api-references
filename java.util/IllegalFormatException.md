# IllegalFormatException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalFormatException

```
open class IllegalFormatException : IllegalArgumentException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](../java.lang/IllegalArgumentException.md) ||
| | | | | ↳ | [java.util.IllegalFormatException](IllegalFormatException.md) |

| Known Direct Subclasses [DuplicateFormatFlagsException](DuplicateFormatFlagsException.md), [FormatFlagsConversionMismatchException](FormatFlagsConversionMismatchException.md), [IllegalFormatCodePointException](IllegalFormatCodePointException.md), [IllegalFormatConversionException](IllegalFormatConversionException.md), [IllegalFormatFlagsException](IllegalFormatFlagsException.md), [IllegalFormatPrecisionException](IllegalFormatPrecisionException.md), [IllegalFormatWidthException](IllegalFormatWidthException.md), [MissingFormatArgumentException](MissingFormatArgumentException.md), [MissingFormatWidthException](MissingFormatWidthException.md), [UnknownFormatConversionException](UnknownFormatConversionException.md), [UnknownFormatFlagsException](UnknownFormatFlagsException.md) |-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DuplicateFormatFlagsException](DuplicateFormatFlagsException.md) | Unchecked exception thrown when duplicate flags are provided in the format specifier. | | [FormatFlagsConversionMismatchException](FormatFlagsConversionMismatchException.md) | Unchecked exception thrown when a conversion and flag are incompatible. | | [IllegalFormatCodePointException](IllegalFormatCodePointException.md) | Unchecked exception thrown when a character with an invalid Unicode code point as defined by [Character.isValidCodePoint](../java.lang/Character.md))is passed to the [Formatter](Formatter.md). | | [IllegalFormatConversionException](IllegalFormatConversionException.md) | Unchecked exception thrown when the argument corresponding to the format specifier is of an incompatible type. | | [IllegalFormatFlagsException](IllegalFormatFlagsException.md) | Unchecked exception thrown when an illegal combination flags is given. | | [IllegalFormatPrecisionException](IllegalFormatPrecisionException.md) | Unchecked exception thrown when the precision is a negative value other than`-1`, the conversion does not support a precision, or the value is otherwise unsupported. | | [IllegalFormatWidthException](IllegalFormatWidthException.md) | Unchecked exception thrown when the format width is a negative value other than`-1`or is otherwise unsupported. | | [MissingFormatArgumentException](MissingFormatArgumentException.md) | Unchecked exception thrown when there is a format specifier which does not have a corresponding argument or if an argument index refers to an argument that does not exist. | | [MissingFormatWidthException](MissingFormatWidthException.md) | Unchecked exception thrown when the format width is required. | | [UnknownFormatConversionException](UnknownFormatConversionException.md) | Unchecked exception thrown when an unknown conversion is given. | | [UnknownFormatFlagsException](UnknownFormatFlagsException.md) | Unchecked exception thrown when an unknown flag is given. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Unchecked exception thrown when a format string contains an illegal syntax or a format specifier that is incompatible with the given arguments. Only explicit subtypes of this exception which correspond to specific errors should be instantiated.

## Summary
