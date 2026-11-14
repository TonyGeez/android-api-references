# LimitExceededException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LimitExceededException

Kotlin| [Java](https://developer.android.com/reference/android/os/LimitExceededException "View this page in Java") 
| --- | --- |

```
open class LimitExceededException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) ||
| | | | | ↳ | [android.os.LimitExceededException](https://developer.android.com/reference/kotlin/android/os/LimitExceededException#) |

Indicates that the app has exceeded a limit set by the System.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LimitExceededException](https://developer.android.com/reference/kotlin/android/os/LimitExceededException#LimitExceededException())`()` Constructs a new`LimitExceededException`with`null`as its detail message. |
| [LimitExceededException](https://developer.android.com/reference/kotlin/android/os/LimitExceededException#LimitExceededException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a new`LimitExceededException`with the specified detail message. |

## Public constructors

### LimitExceededException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LimitExceededException()
```

Constructs a new`LimitExceededException`with`null`as its detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable)). 

### LimitExceededException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LimitExceededException(message: String)
```

Constructs a new`LimitExceededException`with the specified detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the detail message which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method. This value cannot be`null`. |
