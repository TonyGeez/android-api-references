# InputMismatchException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputMismatchException

```
open class InputMismatchException : NoSuchElementException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [java.util.NoSuchElementException](https://developer.android.com/reference/kotlin/java/util/NoSuchElementException) ||
| | | | | ↳ | [java.util.InputMismatchException](https://developer.android.com/reference/kotlin/java/util/InputMismatchException#) |

Thrown by a`Scanner`to indicate that the token retrieved does not match the pattern for the expected type, or that the token is out of range for the expected type.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InputMismatchException](https://developer.android.com/reference/kotlin/java/util/InputMismatchException#InputMismatchException())`()` Constructs an`InputMismatchException`with`null`as its error message string. |
| [InputMismatchException](https://developer.android.com/reference/kotlin/java/util/InputMismatchException#InputMismatchException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`InputMismatchException`, saving a reference to the error message string`s`for later retrieval by the`getMessage`method. |

## Public constructors

### InputMismatchException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputMismatchException()
```

Constructs an`InputMismatchException`with`null`as its error message string. 

### InputMismatchException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputMismatchException(s: String!)
```

Constructs an`InputMismatchException`, saving a reference to the error message string`s`for later retrieval by the`getMessage`method.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
