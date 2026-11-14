# AsynchronousCloseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsynchronousCloseException

```
open class AsynchronousCloseException : ClosedChannelException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) |||
| | | | ↳ | [java.nio.channels.ClosedChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException) ||
| | | | | ↳ | [java.nio.channels.AsynchronousCloseException](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousCloseException#) |

| Known Direct Subclasses [ClosedByInterruptException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedByInterruptException) |---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------| | [ClosedByInterruptException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedByInterruptException) | Checked exception received by a thread when another thread interrupts it while it is blocked in an I/O operation upon a channel. | |

Checked exception received by a thread when another thread closes the channel or the part of the channel upon which it is blocked in an I/O operation.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AsynchronousCloseException](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousCloseException#AsynchronousCloseException())`()` Constructs an instance of this class. |

## Public constructors

### AsynchronousCloseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AsynchronousCloseException()
```

Constructs an instance of this class.
