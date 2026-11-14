# AsynchronousCloseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsynchronousCloseException

```
open class AsynchronousCloseException : ClosedChannelException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.channels.ClosedChannelException](ClosedChannelException.md) ||
| | | | | ↳ | [java.nio.channels.AsynchronousCloseException](AsynchronousCloseException.md) |

| Known Direct Subclasses [ClosedByInterruptException](ClosedByInterruptException.md) |---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------| | [ClosedByInterruptException](ClosedByInterruptException.md) | Checked exception received by a thread when another thread interrupts it while it is blocked in an I/O operation upon a channel. | |
| --- | --- | --- | --- | --- | --- | --- |

Checked exception received by a thread when another thread closes the channel or the part of the channel upon which it is blocked in an I/O operation.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AsynchronousCloseException](AsynchronousCloseException.md))`()` Constructs an instance of this class. |

## Public constructors

### AsynchronousCloseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AsynchronousCloseException()
```

Constructs an instance of this class.
