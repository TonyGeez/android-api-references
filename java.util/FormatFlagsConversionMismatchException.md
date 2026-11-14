# FormatFlagsConversionMismatchException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FormatFlagsConversionMismatchException

```
open class FormatFlagsConversionMismatchException : IllegalFormatException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](../java.lang/IllegalArgumentException.md) |||
| | | | | ↳ | [java.util.IllegalFormatException](IllegalFormatException.md) ||
| | | | | | ↳ | [java.util.FormatFlagsConversionMismatchException](FormatFlagsConversionMismatchException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Unchecked exception thrown when a conversion and flag are incompatible.

Unless otherwise specified, passing a`null`argument to any method or constructor in this class will cause a [NullPointerException](../java.lang/NullPointerException.md) to be thrown.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FormatFlagsConversionMismatchException](FormatFlagsConversionMismatchException.md))`(`f:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Constructs an instance of this class with the specified flag and conversion. |

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getConversion](FormatFlagsConversionMismatchException.md))`()` Returns the incompatible conversion. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFlags](FormatFlagsConversionMismatchException.md))`()` Returns the incompatible flag. |

| Properties ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](FormatFlagsConversionMismatchException.md) <br /> |

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
