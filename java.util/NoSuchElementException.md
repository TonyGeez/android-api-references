# NoSuchElementException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NoSuchElementException

```
open class NoSuchElementException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| | | | ↳ | [java.util.NoSuchElementException](https://developer.android.com/reference/kotlin/java/util/NoSuchElementException#) |

| Known Direct Subclasses [InputMismatchException](https://developer.android.com/reference/kotlin/java/util/InputMismatchException) |-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputMismatchException](https://developer.android.com/reference/kotlin/java/util/InputMismatchException) | Thrown by a`Scanner`to indicate that the token retrieved does not match the pattern for the expected type, or that the token is out of range for the expected type. | |

Thrown by various accessor methods to indicate that the element being requested does not exist.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NoSuchElementException](https://developer.android.com/reference/kotlin/java/util/NoSuchElementException#NoSuchElementException())`()` Constructs a`NoSuchElementException`with`null`as its error message string. |
| [NoSuchElementException](https://developer.android.com/reference/kotlin/java/util/NoSuchElementException#NoSuchElementException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`NoSuchElementException`, saving a reference to the error message string`s`for later retrieval by the`getMessage`method. |
| [NoSuchElementException](https://developer.android.com/reference/kotlin/java/util/NoSuchElementException#NoSuchElementException(kotlin.String,%20kotlin.Throwable))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`NoSuchElementException`with the specified detail message and cause. |
| [NoSuchElementException](https://developer.android.com/reference/kotlin/java/util/NoSuchElementException#NoSuchElementException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`NoSuchElementException`with the specified cause. |

## Public constructors

### NoSuchElementException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchElementException()
```

Constructs a`NoSuchElementException`with`null`as its error message string. 

### NoSuchElementException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchElementException(s: String!)
```

Constructs a`NoSuchElementException`, saving a reference to the error message string`s`for later retrieval by the`getMessage`method.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### NoSuchElementException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchElementException(
    s: String!, 
    cause: Throwable!)
```

Constructs a`NoSuchElementException`with the specified detail message and cause.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message, or null |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method), or null |

### NoSuchElementException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchElementException(cause: Throwable!)
```

Constructs a`NoSuchElementException`with the specified cause. The detail message is set to`(cause == null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method) |
