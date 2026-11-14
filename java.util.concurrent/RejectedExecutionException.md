# RejectedExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RejectedExecutionException

```
open class RejectedExecutionException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.concurrent.RejectedExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionException#) |

| Known Direct Subclasses [InlineExecutionProhibitedException](https://developer.android.com/reference/kotlin/android/net/http/InlineExecutionProhibitedException.html#) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InlineExecutionProhibitedException](https://developer.android.com/reference/kotlin/android/net/http/InlineExecutionProhibitedException.html#) | Thrown when an executor runs a submitted runnable inline in [java.util.concurrent.Executor#execute(Runnable)](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor#execute(java.lang.Runnable)) and [android.net.http.UrlRequest.Builder#setDirectExecutorAllowed](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder.html#setDirectExecutorAllowed(kotlin.Boolean)) was not called. | |
| --- | --- | --- | --- | --- | --- | --- |

Exception thrown by an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor) when a task cannot be accepted for execution.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RejectedExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionException#RejectedExecutionException())`()` Constructs a `RejectedExecutionException` with no detail message. |
| [RejectedExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionException#RejectedExecutionException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a `RejectedExecutionException` with the specified detail message. |
| [RejectedExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionException#RejectedExecutionException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a `RejectedExecutionException` with the specified detail message and cause. |
| [RejectedExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionException#RejectedExecutionException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a `RejectedExecutionException` with the specified cause. |

## Public constructors

### RejectedExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RejectedExecutionException()
```

Constructs a `RejectedExecutionException` with no detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable)). 

### RejectedExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RejectedExecutionException(message: String!)
```

Constructs a `RejectedExecutionException` with the specified detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable)).

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
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()) method) |

### RejectedExecutionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RejectedExecutionException(cause: Throwable!)
```

Constructs a `RejectedExecutionException` with the specified cause. The detail message is set to `(cause == null ? null : cause.toString())` (which typically contains the class and detail message of `cause`).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()) method) |
