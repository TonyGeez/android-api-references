# ClosedChannelException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClosedChannelException

```
open class ClosedChannelException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java/io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.channels.ClosedChannelException](../java/nio/channels/ClosedChannelException.md) |

| Known Direct Subclasses [AsynchronousCloseException](../java/nio/channels/AsynchronousCloseException.md) |---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------| | [AsynchronousCloseException](../java/nio/channels/AsynchronousCloseException.md) | Checked exception received by a thread when another thread closes the channel or the part of the channel upon which it is blocked in an I/O operation. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ClosedByInterruptException](../java/nio/channels/ClosedByInterruptException.md) |---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------| | [ClosedByInterruptException](../java/nio/channels/ClosedByInterruptException.md) | Checked exception received by a thread when another thread interrupts it while it is blocked in an I/O operation upon a channel. | |
| --- | --- | --- | --- | --- | --- | --- |

Checked exception thrown when an attempt is made to invoke or complete an I/O operation upon channel that is closed, or at least closed to that operation. That this exception is thrown does not necessarily imply that the channel is completely closed. A socket channel whose write half has been shut down, for example, may still be open for reading.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClosedChannelException](../java/nio/channels/ClosedChannelException.md))`()` Constructs an instance of this class. |

## Public constructors

### ClosedChannelException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClosedChannelException()
```

Constructs an instance of this class.
