# LimitExceededException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LimitExceededException

Kotlin| [Java](../android/os/LimitExceededException.md) 
| --- | --- |

```
open class LimitExceededException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java/lang/IllegalStateException.md) ||
| | | | | ↳ | [android.os.LimitExceededException](../android/os/LimitExceededException.md) |

Indicates that the app has exceeded a limit set by the System.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LimitExceededException](../android/os/LimitExceededException.md))`()` Constructs a new`LimitExceededException`with`null`as its detail message. |
| [LimitExceededException](../android/os/LimitExceededException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a new`LimitExceededException`with the specified detail message. |

## Public constructors

### LimitExceededException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LimitExceededException()
```

Constructs a new`LimitExceededException`with`null`as its detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](../java/lang/Throwable.md)). 

### LimitExceededException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LimitExceededException(message: String)
```

Constructs a new`LimitExceededException`with the specified detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](../java/lang/Throwable.md)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the detail message which is saved for later retrieval by the [getMessage()](../java/lang/Throwable.md))method. This value cannot be`null`. |
