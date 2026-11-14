# BrokenBarrierException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BrokenBarrierException

```
open class BrokenBarrierException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [java.util.concurrent.BrokenBarrierException](../java/util/concurrent/BrokenBarrierException.md) |
| --- | --- | --- | --- |

Exception thrown when a thread tries to wait upon a barrier that is in a broken state, or which enters the broken state while the thread is waiting.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BrokenBarrierException](../java/util/concurrent/BrokenBarrierException.md))`()` Constructs a`BrokenBarrierException`with no specified detail message. |
| [BrokenBarrierException](../java/util/concurrent/BrokenBarrierException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`BrokenBarrierException`with the specified detail message. |

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
