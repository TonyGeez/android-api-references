# CancellationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CancellationException

```
open class CancellationException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) ||
| | | | | ↳ | [java.util.concurrent.CancellationException](https://developer.android.com/reference/kotlin/java/util/concurrent/CancellationException#) |

Exception indicating that the result of a value-producing task, such as a [FutureTask](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask), cannot be retrieved because the task was cancelled.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CancellationException](https://developer.android.com/reference/kotlin/java/util/concurrent/CancellationException#CancellationException())`()` Constructs a`CancellationException`with no detail message. |
| [CancellationException](https://developer.android.com/reference/kotlin/java/util/concurrent/CancellationException#CancellationException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`CancellationException`with the specified detail message. |

## Public constructors

### CancellationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CancellationException()
```

Constructs a`CancellationException`with no detail message. 

### CancellationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CancellationException(message: String!)
```

Constructs a`CancellationException`with the specified detail message.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
