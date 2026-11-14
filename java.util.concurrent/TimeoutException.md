# TimeoutException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeoutException

```
open class TimeoutException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [java.util.concurrent.TimeoutException](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException#) |

Exception thrown when a blocking operation times out. Blocking operations for which a timeout is specified need a means to indicate that the timeout has occurred. For many such operations it is possible to return a value that indicates timeout; when that is not possible or desirable then`TimeoutException`should be declared and thrown.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TimeoutException](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException#TimeoutException())`()` Constructs a`TimeoutException`with no specified detail message. |
| [TimeoutException](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException#TimeoutException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`TimeoutException`with the specified detail message. |

## Public constructors

### TimeoutException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TimeoutException()
```

Constructs a`TimeoutException`with no specified detail message. 

### TimeoutException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TimeoutException(message: String!)
```

Constructs a`TimeoutException`with the specified detail message.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
