# RejectedExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RejectedExecutionException

```
open class RejectedExecutionException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.concurrent.RejectedExecutionException](RejectedExecutionException.md) |

| Known Direct Subclasses [InlineExecutionProhibitedException](../android.net.http/InlineExecutionProhibitedException.md) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InlineExecutionProhibitedException](../android.net.http/InlineExecutionProhibitedException.md) | Thrown when an executor runs a submitted runnable inline in [java.util.concurrent.Executor#execute(Runnable)](Executor.md)) and [android.net.http.UrlRequest.Builder#setDirectExecutorAllowed](../android/net/http/UrlRequest.Builder.md)) was not called. | |
| --- | --- | --- | --- | --- | --- | --- |

Exception thrown by an [Executor](Executor.md) when a task cannot be accepted for execution.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RejectedExecutionException](RejectedExecutionException.md))`()` Constructs a `RejectedExecutionException` with no detail message. |
| [RejectedExecutionException](RejectedExecutionException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a `RejectedExecutionException` with the specified detail message. |
| [RejectedExecutionException](RejectedExecutionException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a `RejectedExecutionException` with the specified detail message and cause. |
| [RejectedExecutionException](RejectedExecutionException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a `RejectedExecutionException` with the specified cause. |

## Public constructors

### RejectedExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RejectedExecutionException()
```

Constructs a `RejectedExecutionException` with no detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](../java.lang/Throwable.md)). 

### RejectedExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RejectedExecutionException(message: String!)
```

Constructs a `RejectedExecutionException` with the specified detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](../java.lang/Throwable.md)).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message |

### RejectedExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RejectedExecutionException(
    message: String!, 
    cause: Throwable!)
```

Constructs a `RejectedExecutionException` with the specified detail message and cause.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md)) method) |

### RejectedExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RejectedExecutionException(cause: Throwable!)
```

Constructs a `RejectedExecutionException` with the specified cause. The detail message is set to `(cause == null ? null : cause.toString())` (which typically contains the class and detail message of `cause`).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md)) method) |
