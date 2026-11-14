# IllegalFormatConversionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalFormatConversionException

```
open class IllegalFormatConversionException : IllegalFormatException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](../java/lang/IllegalArgumentException.md) |||
| | | | | ↳ | [java.util.IllegalFormatException](../java/util/IllegalFormatException.md) ||
| | | | | | ↳ | [java.util.IllegalFormatConversionException](../java/util/IllegalFormatConversionException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Unchecked exception thrown when the argument corresponding to the format specifier is of an incompatible type.

Unless otherwise specified, passing a`null`argument to any method or constructor in this class will cause a [NullPointerException](../java/lang/NullPointerException.md) to be thrown.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalFormatConversionException](../java/util/IllegalFormatConversionException.md))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `arg:` ` [Class](../java/lang/Class.md)<*>!`)` Constructs an instance of this class with the mismatched conversion and the corresponding argument class. |

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Class](../java/lang/Class.md)\<\*\>! | [getArgumentClass](../java/util/IllegalFormatConversionException.md))`()` Returns the class of the mismatched argument. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getConversion](../java/util/IllegalFormatConversionException.md))`()` Returns the inapplicable conversion. |

| Properties ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](../java/util/IllegalFormatConversionException.md) <br /> |

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
| `arg` | [Class](../java/lang/Class.md)\<\*\>!:Class of the mismatched argument |

## Public methods

### getArgumentClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getArgumentClass(): Class<*>!
```

Returns the class of the mismatched argument.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------|
| [Class](../java/lang/Class.md)<*>! | The class of the mismatched argument |

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
