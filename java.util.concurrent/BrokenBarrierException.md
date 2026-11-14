# BrokenBarrierException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BrokenBarrierException

```
open class BrokenBarrierException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [java.util.concurrent.BrokenBarrierException](https://developer.android.com/reference/kotlin/java/util/concurrent/BrokenBarrierException#) |

Exception thrown when a thread tries to wait upon a barrier that is in a broken state, or which enters the broken state while the thread is waiting.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BrokenBarrierException](https://developer.android.com/reference/kotlin/java/util/concurrent/BrokenBarrierException#BrokenBarrierException())`()` Constructs a`BrokenBarrierException`with no specified detail message. |
| [BrokenBarrierException](https://developer.android.com/reference/kotlin/java/util/concurrent/BrokenBarrierException#BrokenBarrierException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`BrokenBarrierException`with the specified detail message. |

## Public constructors

### BrokenBarrierException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BrokenBarrierException()
```

Constructs a`BrokenBarrierException`with no specified detail message. 

### BrokenBarrierException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BrokenBarrierException(message: String!)
```

Constructs a`BrokenBarrierException`with the specified detail message.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
