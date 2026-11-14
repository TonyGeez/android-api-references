# ConnectionPendingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConnectionPendingException

```
open class ConnectionPendingException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java.lang/IllegalStateException.md) ||
| | | | | ↳ | [java.nio.channels.ConnectionPendingException](ConnectionPendingException.md) |

Unchecked exception thrown when an attempt is made to connect a [SocketChannel](SocketChannel.md) for which a non-blocking connection operation is already in progress.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConnectionPendingException](ConnectionPendingException.md))`()` Constructs an instance of this class. |

## Public constructors

### ConnectionPendingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConnectionPendingException()
```

Constructs an instance of this class.
