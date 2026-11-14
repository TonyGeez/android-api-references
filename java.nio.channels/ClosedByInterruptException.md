# ClosedByInterruptException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClosedByInterruptException

```
open class ClosedByInterruptException : AsynchronousCloseException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||||
| | | ↳ | [java.io.IOException](../java/io/IOException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.channels.ClosedChannelException](../java/nio/channels/ClosedChannelException.md) |||
| | | | | ↳ | [java.nio.channels.AsynchronousCloseException](../java/nio/channels/AsynchronousCloseException.md) ||
| | | | | | ↳ | [java.nio.channels.ClosedByInterruptException](../java/nio/channels/ClosedByInterruptException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Checked exception received by a thread when another thread interrupts it while it is blocked in an I/O operation upon a channel. Before this exception is thrown the channel will have been closed and the interrupt status of the previously-blocked thread will have been set.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClosedByInterruptException](../java/nio/channels/ClosedByInterruptException.md))`()` Constructs an instance of this class. |

## Public constructors

### ClosedByInterruptException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClosedByInterruptException()
```

Constructs an instance of this class.
