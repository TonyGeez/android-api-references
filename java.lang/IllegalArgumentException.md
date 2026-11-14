# IllegalArgumentException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalArgumentException

```
open class IllegalArgumentException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](IllegalArgumentException.md) |

| Known Direct Subclasses [IllegalChannelGroupException](../java.nio.channels/IllegalChannelGroupException.md), [IllegalCharsetNameException](../java.nio.charset/IllegalCharsetNameException.md), [IllegalFormatException](../java.util/IllegalFormatException.md), [IllegalSelectorException](../java.nio.channels/IllegalSelectorException.md), [IllegalThreadStateException](IllegalThreadStateException.md), [InvalidParameterException](../java.security/InvalidParameterException.md), [InvalidPathException](../java.nio.file/InvalidPathException.md), [NumberFormatException](NumberFormatException.md), [PatternSyntaxException](../java.util.regex/PatternSyntaxException.md), [ProviderMismatchException](../java.nio.file/ProviderMismatchException.md), [SystemUpdatePolicy.ValidationFailedException](../android/app/admin/SystemUpdatePolicy.ValidationFailedException.md), [UnresolvedAddressException](../java.nio.channels/UnresolvedAddressException.md), and 2 others. |---------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [IllegalChannelGroupException](../java.nio.channels/IllegalChannelGroupException.md) | Unchecked exception thrown when an attempt is made to open a channel in a group that was not created by the same provider. | | [IllegalCharsetNameException](../java.nio.charset/IllegalCharsetNameException.md) | Unchecked exception thrown when a string that is not a [legal charset name](../java.nio.charset/Charset.md) is used as such. | | [IllegalFormatException](../java.util/IllegalFormatException.md) | Unchecked exception thrown when a format string contains an illegal syntax or a format specifier that is incompatible with the given arguments. | | [IllegalSelectorException](../java.nio.channels/IllegalSelectorException.md) | Unchecked exception thrown when an attempt is made to register a channel with a selector that was not created by the provider that created the channel. | | [IllegalThreadStateException](IllegalThreadStateException.md) | Thrown to indicate that a thread is not in an appropriate state for the requested operation. | | [InvalidParameterException](../java.security/InvalidParameterException.md) | This exception, designed for use by the JCA/JCE engine classes, is thrown when an invalid parameter is passed to a method. | | [InvalidPathException](../java.nio.file/InvalidPathException.md) | Unchecked exception thrown when path string cannot be converted into a [Path](../java.nio.file/Path.md) because the path string contains invalid characters, or the path string is invalid for other file system specific reasons. | | [NumberFormatException](NumberFormatException.md) | Thrown to indicate that the application has attempted to convert a string to one of the numeric types, but that the string does not have the appropriate format. | | [PatternSyntaxException](../java.util.regex/PatternSyntaxException.md) | Unchecked exception thrown to indicate a syntax error in a regular-expression pattern. | | [ProviderMismatchException](../java.nio.file/ProviderMismatchException.md) | Unchecked exception thrown when an attempt is made to invoke a method on an object created by one file system provider with a parameter created by a different file system provider. | | [SystemUpdatePolicy.ValidationFailedException](../android/app/admin/SystemUpdatePolicy.ValidationFailedException.md) | An exception class that represents various validation errors thrown from [SystemUpdatePolicy.setFreezePeriods](../android.app.admin/SystemUpdatePolicy.md))and [DevicePolicyManager.setSystemUpdatePolicy](../android.app.admin/DevicePolicyManager.md)) | | [UnresolvedAddressException](../java.nio.channels/UnresolvedAddressException.md) | Unchecked exception thrown when an attempt is made to invoke a network operation upon an unresolved socket address. | | [UnsupportedAddressTypeException](../java.nio.channels/UnsupportedAddressTypeException.md) | Unchecked exception thrown when an attempt is made to bind or connect to a socket address of a type that is not supported. | | [UnsupportedCharsetException](../java.nio.charset/UnsupportedCharsetException.md) | Unchecked exception thrown when no support is available for a requested charset. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DuplicateFormatFlagsException](../java.util/DuplicateFormatFlagsException.md), [FormatFlagsConversionMismatchException](../java.util/FormatFlagsConversionMismatchException.md), [IllegalFormatCodePointException](../java.util/IllegalFormatCodePointException.md), [IllegalFormatConversionException](../java.util/IllegalFormatConversionException.md), [IllegalFormatFlagsException](../java.util/IllegalFormatFlagsException.md), [IllegalFormatPrecisionException](../java.util/IllegalFormatPrecisionException.md), [IllegalFormatWidthException](../java.util/IllegalFormatWidthException.md), [MissingFormatArgumentException](../java.util/MissingFormatArgumentException.md), [MissingFormatWidthException](../java.util/MissingFormatWidthException.md), [UnknownFormatConversionException](../java.util/UnknownFormatConversionException.md), [UnknownFormatFlagsException](../java.util/UnknownFormatFlagsException.md) |-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DuplicateFormatFlagsException](../java.util/DuplicateFormatFlagsException.md) | Unchecked exception thrown when duplicate flags are provided in the format specifier. | | [FormatFlagsConversionMismatchException](../java.util/FormatFlagsConversionMismatchException.md) | Unchecked exception thrown when a conversion and flag are incompatible. | | [IllegalFormatCodePointException](../java.util/IllegalFormatCodePointException.md) | Unchecked exception thrown when a character with an invalid Unicode code point as defined by [Character.isValidCodePoint](Character.md))is passed to the [Formatter](../java.util/Formatter.md). | | [IllegalFormatConversionException](../java.util/IllegalFormatConversionException.md) | Unchecked exception thrown when the argument corresponding to the format specifier is of an incompatible type. | | [IllegalFormatFlagsException](../java.util/IllegalFormatFlagsException.md) | Unchecked exception thrown when an illegal combination flags is given. | | [IllegalFormatPrecisionException](../java.util/IllegalFormatPrecisionException.md) | Unchecked exception thrown when the precision is a negative value other than`-1`, the conversion does not support a precision, or the value is otherwise unsupported. | | [IllegalFormatWidthException](../java.util/IllegalFormatWidthException.md) | Unchecked exception thrown when the format width is a negative value other than`-1`or is otherwise unsupported. | | [MissingFormatArgumentException](../java.util/MissingFormatArgumentException.md) | Unchecked exception thrown when there is a format specifier which does not have a corresponding argument or if an argument index refers to an argument that does not exist. | | [MissingFormatWidthException](../java.util/MissingFormatWidthException.md) | Unchecked exception thrown when the format width is required. | | [UnknownFormatConversionException](../java.util/UnknownFormatConversionException.md) | Unchecked exception thrown when an unknown conversion is given. | | [UnknownFormatFlagsException](../java.util/UnknownFormatFlagsException.md) | Unchecked exception thrown when an unknown flag is given. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Thrown to indicate that a method has been passed an illegal or inappropriate argument.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalArgumentException](IllegalArgumentException.md))`()` Constructs an`IllegalArgumentException`with no detail message. |
| [IllegalArgumentException](IllegalArgumentException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`IllegalArgumentException`with the specified detail message. |
| [IllegalArgumentException](IllegalArgumentException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new exception with the specified detail message and cause. |
| [IllegalArgumentException](IllegalArgumentException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new exception with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### IllegalArgumentException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalArgumentException()
```

Constructs an`IllegalArgumentException`with no detail message. 

### IllegalArgumentException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalArgumentException(s: String!)
```

Constructs an`IllegalArgumentException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### IllegalArgumentException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalArgumentException(
    message: String!, 
    cause: Throwable!)
```

Constructs a new exception with the specified detail message and cause.

Note that the detail message associated with`cause`is*not*automatically incorporated in this exception's detail message.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [Throwable.getMessage()](Throwable.md))method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [Throwable.getCause()](Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### IllegalArgumentException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalArgumentException(cause: Throwable!)
```

Constructs a new exception with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). This constructor is useful for exceptions that are little more than wrappers for other throwables (for example, ).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [Throwable.getCause()](Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
