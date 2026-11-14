# ExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExecutionException

```
open class ExecutionException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [java.util.concurrent.ExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutionException#) |

Exception thrown when attempting to retrieve the result of a task that aborted by throwing an exception. This exception can be inspected using the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutionException#ExecutionException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an`ExecutionException`with the specified detail message and cause. |
| [ExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutionException#ExecutionException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an`ExecutionException`with the specified cause. |

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutionException#ExecutionException())`()` Constructs an`ExecutionException`with no detail message. |
| [ExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutionException#ExecutionException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`ExecutionException`with the specified detail message. |

## Public constructors

### ExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExecutionException(
    message: String!, 
    cause: Throwable!)
```

Constructs an`ExecutionException`with the specified detail message and cause.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method) |

### ExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExecutionException(cause: Throwable!)
```

Constructs an`ExecutionException`with the specified cause. The detail message is set to`(cause == null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method) |

## Protected constructors

### ExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected ExecutionException()
```

Constructs an`ExecutionException`with no detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable)). 

### ExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected ExecutionException(message: String!)
```

Constructs an`ExecutionException`with the specified detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable)).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
