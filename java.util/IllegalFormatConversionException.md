# IllegalFormatConversionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalFormatConversionException

```
open class IllegalFormatConversionException : IllegalFormatException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||||
| | | | ↳ | [java.lang.IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) |||
| | | | | ↳ | [java.util.IllegalFormatException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatException) ||
| | | | | | ↳ | [java.util.IllegalFormatConversionException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatConversionException#) |

Unchecked exception thrown when the argument corresponding to the format specifier is of an incompatible type.

Unless otherwise specified, passing a`null`argument to any method or constructor in this class will cause a [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#) to be thrown.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalFormatConversionException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatConversionException#IllegalFormatConversionException(kotlin.Char,%20java.lang.Class))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `arg:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` Constructs an instance of this class with the mismatched conversion and the corresponding argument class. |

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>! | [getArgumentClass](https://developer.android.com/reference/kotlin/java/util/IllegalFormatConversionException#getArgumentClass())`()` Returns the class of the mismatched argument. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getConversion](https://developer.android.com/reference/kotlin/java/util/IllegalFormatConversionException#getConversion())`()` Returns the inapplicable conversion. |

| Properties ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/java/util/IllegalFormatConversionException#message:kotlin.String) <br /> |

## Public constructors

### IllegalFormatConversionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalFormatConversionException(
    c: Char, 
    arg: Class<*>!)
```

Constructs an instance of this class with the mismatched conversion and the corresponding argument class.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):Inapplicable conversion |
| `arg` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!:Class of the mismatched argument |

## Public methods

### getArgumentClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getArgumentClass(): Class<*>!
```

Returns the class of the mismatched argument.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------|
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>! | The class of the mismatched argument |

### getConversion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConversion(): Char
```

Returns the inapplicable conversion.

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | The inapplicable conversion |

## Properties

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |
