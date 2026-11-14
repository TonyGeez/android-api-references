# UnknownFormatConversionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnknownFormatConversionException

```
open class UnknownFormatConversionException : IllegalFormatException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) |||
| | | | | ↳ | [java.util.IllegalFormatException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatException) ||
| | | | | | ↳ | [java.util.UnknownFormatConversionException](https://developer.android.com/reference/kotlin/java/util/UnknownFormatConversionException#) |
| --- | --- | --- | --- | --- | --- | --- |

Unchecked exception thrown when an unknown conversion is given.

Unless otherwise specified, passing a`null`argument to any method or constructor in this class will cause a [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#) to be thrown.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnknownFormatConversionException](https://developer.android.com/reference/kotlin/java/util/UnknownFormatConversionException#UnknownFormatConversionException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class with the unknown conversion. |

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getConversion](https://developer.android.com/reference/kotlin/java/util/UnknownFormatConversionException#getConversion())`()` Returns the unknown conversion. |

| Properties ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/java/util/UnknownFormatConversionException#message:kotlin.String) <br /> |

## Public constructors

### UnknownFormatConversionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnknownFormatConversionException(s: String!)
```

Constructs an instance of this class with the unknown conversion.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Unknown conversion |

## Public methods

### getConversion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConversion(): String!
```

Returns the unknown conversion.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The unknown conversion. |

## Properties

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |
