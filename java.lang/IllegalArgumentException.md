# IllegalArgumentException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalArgumentException

```
open class IllegalArgumentException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) ||
| | | | ↳ | [java.lang.IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException#) |

| Known Direct Subclasses [IllegalChannelGroupException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalChannelGroupException.html#), [IllegalCharsetNameException](https://developer.android.com/reference/kotlin/java/nio/charset/IllegalCharsetNameException.html#), [IllegalFormatException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatException.html#), [IllegalSelectorException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalSelectorException.html#), [IllegalThreadStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalThreadStateException), [InvalidParameterException](https://developer.android.com/reference/kotlin/java/security/InvalidParameterException.html#), [InvalidPathException](https://developer.android.com/reference/kotlin/java/nio/file/InvalidPathException.html#), [NumberFormatException](https://developer.android.com/reference/kotlin/java/lang/NumberFormatException), [PatternSyntaxException](https://developer.android.com/reference/kotlin/java/util/regex/PatternSyntaxException.html#), [ProviderMismatchException](https://developer.android.com/reference/kotlin/java/nio/file/ProviderMismatchException.html#), [SystemUpdatePolicy.ValidationFailedException](https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy.ValidationFailedException.html#), [UnresolvedAddressException](https://developer.android.com/reference/kotlin/java/nio/channels/UnresolvedAddressException.html#), and 2 others. |---------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [IllegalChannelGroupException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalChannelGroupException.html#) | Unchecked exception thrown when an attempt is made to open a channel in a group that was not created by the same provider. | | [IllegalCharsetNameException](https://developer.android.com/reference/kotlin/java/nio/charset/IllegalCharsetNameException.html#) | Unchecked exception thrown when a string that is not a [legal charset name](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#names) is used as such. | | [IllegalFormatException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatException.html#) | Unchecked exception thrown when a format string contains an illegal syntax or a format specifier that is incompatible with the given arguments. | | [IllegalSelectorException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalSelectorException.html#) | Unchecked exception thrown when an attempt is made to register a channel with a selector that was not created by the provider that created the channel. | | [IllegalThreadStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalThreadStateException) | Thrown to indicate that a thread is not in an appropriate state for the requested operation. | | [InvalidParameterException](https://developer.android.com/reference/kotlin/java/security/InvalidParameterException.html#) | This exception, designed for use by the JCA/JCE engine classes, is thrown when an invalid parameter is passed to a method. | | [InvalidPathException](https://developer.android.com/reference/kotlin/java/nio/file/InvalidPathException.html#) | Unchecked exception thrown when path string cannot be converted into a [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#) because the path string contains invalid characters, or the path string is invalid for other file system specific reasons. | | [NumberFormatException](https://developer.android.com/reference/kotlin/java/lang/NumberFormatException) | Thrown to indicate that the application has attempted to convert a string to one of the numeric types, but that the string does not have the appropriate format. | | [PatternSyntaxException](https://developer.android.com/reference/kotlin/java/util/regex/PatternSyntaxException.html#) | Unchecked exception thrown to indicate a syntax error in a regular-expression pattern. | | [ProviderMismatchException](https://developer.android.com/reference/kotlin/java/nio/file/ProviderMismatchException.html#) | Unchecked exception thrown when an attempt is made to invoke a method on an object created by one file system provider with a parameter created by a different file system provider. | | [SystemUpdatePolicy.ValidationFailedException](https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy.ValidationFailedException.html#) | An exception class that represents various validation errors thrown from [SystemUpdatePolicy.setFreezePeriods](https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy.html#setFreezePeriods(kotlin.collections.MutableList))and [DevicePolicyManager.setSystemUpdatePolicy](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#setSystemUpdatePolicy(android.content.ComponentName,%20android.app.admin.SystemUpdatePolicy)) | | [UnresolvedAddressException](https://developer.android.com/reference/kotlin/java/nio/channels/UnresolvedAddressException.html#) | Unchecked exception thrown when an attempt is made to invoke a network operation upon an unresolved socket address. | | [UnsupportedAddressTypeException](https://developer.android.com/reference/kotlin/java/nio/channels/UnsupportedAddressTypeException.html#) | Unchecked exception thrown when an attempt is made to bind or connect to a socket address of a type that is not supported. | | [UnsupportedCharsetException](https://developer.android.com/reference/kotlin/java/nio/charset/UnsupportedCharsetException.html#) | Unchecked exception thrown when no support is available for a requested charset. | |

| Known Indirect Subclasses [DuplicateFormatFlagsException](https://developer.android.com/reference/kotlin/java/util/DuplicateFormatFlagsException.html#), [FormatFlagsConversionMismatchException](https://developer.android.com/reference/kotlin/java/util/FormatFlagsConversionMismatchException.html#), [IllegalFormatCodePointException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatCodePointException.html#), [IllegalFormatConversionException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatConversionException.html#), [IllegalFormatFlagsException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatFlagsException.html#), [IllegalFormatPrecisionException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatPrecisionException.html#), [IllegalFormatWidthException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatWidthException.html#), [MissingFormatArgumentException](https://developer.android.com/reference/kotlin/java/util/MissingFormatArgumentException.html#), [MissingFormatWidthException](https://developer.android.com/reference/kotlin/java/util/MissingFormatWidthException.html#), [UnknownFormatConversionException](https://developer.android.com/reference/kotlin/java/util/UnknownFormatConversionException.html#), [UnknownFormatFlagsException](https://developer.android.com/reference/kotlin/java/util/UnknownFormatFlagsException.html#) |-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DuplicateFormatFlagsException](https://developer.android.com/reference/kotlin/java/util/DuplicateFormatFlagsException.html#) | Unchecked exception thrown when duplicate flags are provided in the format specifier. | | [FormatFlagsConversionMismatchException](https://developer.android.com/reference/kotlin/java/util/FormatFlagsConversionMismatchException.html#) | Unchecked exception thrown when a conversion and flag are incompatible. | | [IllegalFormatCodePointException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatCodePointException.html#) | Unchecked exception thrown when a character with an invalid Unicode code point as defined by [Character.isValidCodePoint](https://developer.android.com/reference/kotlin/java/lang/Character#isValidCodePoint(kotlin.Int))is passed to the [Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#). | | [IllegalFormatConversionException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatConversionException.html#) | Unchecked exception thrown when the argument corresponding to the format specifier is of an incompatible type. | | [IllegalFormatFlagsException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatFlagsException.html#) | Unchecked exception thrown when an illegal combination flags is given. | | [IllegalFormatPrecisionException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatPrecisionException.html#) | Unchecked exception thrown when the precision is a negative value other than`-1`, the conversion does not support a precision, or the value is otherwise unsupported. | | [IllegalFormatWidthException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatWidthException.html#) | Unchecked exception thrown when the format width is a negative value other than`-1`or is otherwise unsupported. | | [MissingFormatArgumentException](https://developer.android.com/reference/kotlin/java/util/MissingFormatArgumentException.html#) | Unchecked exception thrown when there is a format specifier which does not have a corresponding argument or if an argument index refers to an argument that does not exist. | | [MissingFormatWidthException](https://developer.android.com/reference/kotlin/java/util/MissingFormatWidthException.html#) | Unchecked exception thrown when the format width is required. | | [UnknownFormatConversionException](https://developer.android.com/reference/kotlin/java/util/UnknownFormatConversionException.html#) | Unchecked exception thrown when an unknown conversion is given. | | [UnknownFormatFlagsException](https://developer.android.com/reference/kotlin/java/util/UnknownFormatFlagsException.html#) | Unchecked exception thrown when an unknown flag is given. | |

Thrown to indicate that a method has been passed an illegal or inappropriate argument.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException#IllegalArgumentException())`()` Constructs an`IllegalArgumentException`with no detail message. |
| [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException#IllegalArgumentException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`IllegalArgumentException`with the specified detail message. |
| [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException#IllegalArgumentException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new exception with the specified detail message and cause. |
| [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException#IllegalArgumentException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new exception with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

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
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [Throwable.getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage())method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [Throwable.getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### IllegalArgumentException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalArgumentException(cause: Throwable!)
```

Constructs a new exception with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). This constructor is useful for exceptions that are little more than wrappers for other throwables (for example, ).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [Throwable.getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
