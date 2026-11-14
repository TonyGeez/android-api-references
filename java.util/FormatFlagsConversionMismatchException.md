# FormatFlagsConversionMismatchException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FormatFlagsConversionMismatchException

```
open class FormatFlagsConversionMismatchException : IllegalFormatException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) |||
| | | | | ↳ | [java.util.IllegalFormatException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatException) ||
| | | | | | ↳ | [java.util.FormatFlagsConversionMismatchException](https://developer.android.com/reference/kotlin/java/util/FormatFlagsConversionMismatchException#) |
| --- | --- | --- | --- | --- | --- | --- |

Unchecked exception thrown when a conversion and flag are incompatible.

Unless otherwise specified, passing a`null`argument to any method or constructor in this class will cause a [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#) to be thrown.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FormatFlagsConversionMismatchException](https://developer.android.com/reference/kotlin/java/util/FormatFlagsConversionMismatchException#FormatFlagsConversionMismatchException(kotlin.String,%20kotlin.Char))`(`f:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Constructs an instance of this class with the specified flag and conversion. |

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getConversion](https://developer.android.com/reference/kotlin/java/util/FormatFlagsConversionMismatchException#getConversion())`()` Returns the incompatible conversion. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFlags](https://developer.android.com/reference/kotlin/java/util/FormatFlagsConversionMismatchException#getFlags())`()` Returns the incompatible flag. |

| Properties ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/java/util/FormatFlagsConversionMismatchException#message:kotlin.String) <br /> |

## Public constructors

### FormatFlagsConversionMismatchException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FormatFlagsConversionMismatchException(
    f: String!, 
    c: Char)
```

Constructs an instance of this class with the specified flag and conversion.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------|
| `f` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The flag |
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The conversion |

## Public methods

### getConversion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConversion(): Char
```

Returns the incompatible conversion.

| Return ||
|------------------------------------------------------------------------------|----------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | The conversion |

### getFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFlags(): String!
```

Returns the incompatible flag.

| Return ||
|-----------------------------------------------------------------------------------|----------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The flag |

## Properties

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |
