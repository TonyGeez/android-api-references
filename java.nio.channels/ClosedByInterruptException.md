# ClosedByInterruptException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClosedByInterruptException

```
open class ClosedByInterruptException : AsynchronousCloseException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||||
| | | | ↳ | [java.nio.channels.ClosedChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException) |||
| | | | | ↳ | [java.nio.channels.AsynchronousCloseException](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousCloseException) ||
| | | | | | ↳ | [java.nio.channels.ClosedByInterruptException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedByInterruptException#) |

Checked exception received by a thread when another thread interrupts it while it is blocked in an I/O operation upon a channel. Before this exception is thrown the channel will have been closed and the interrupt status of the previously-blocked thread will have been set.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClosedByInterruptException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedByInterruptException#ClosedByInterruptException())`()` Constructs an instance of this class. |

## Public constructors

### ClosedByInterruptException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClosedByInterruptException()
```

Constructs an instance of this class.
