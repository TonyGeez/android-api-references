# ExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExecutionException

```
open class ExecutionException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [java.util.concurrent.ExecutionException](../java/util/concurrent/ExecutionException.md) |
| --- | --- | --- | --- |

Exception thrown when attempting to retrieve the result of a task that aborted by throwing an exception. This exception can be inspected using the [getCause()](../java/lang/Throwable.md))method.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ExecutionException](../java/util/concurrent/ExecutionException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an`ExecutionException`with the specified detail message and cause. |
| [ExecutionException](../java/util/concurrent/ExecutionException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an`ExecutionException`with the specified cause. |

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ExecutionException](../java/util/concurrent/ExecutionException.md))`()` Constructs an`ExecutionException`with no detail message. |
| [ExecutionException](../java/util/concurrent/ExecutionException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`ExecutionException`with the specified detail message. |

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
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method) |

### ExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExecutionException(cause: Throwable!)
```

Constructs an`ExecutionException`with the specified cause. The detail message is set to`(cause == null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method) |

## Protected constructors

### ExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected ExecutionException()
```

Constructs an`ExecutionException`with no detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](../java/lang/Throwable.md)). 

### ExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected ExecutionException(message: String!)
```

Constructs an`ExecutionException`with the specified detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](../java/lang/Throwable.md)).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
