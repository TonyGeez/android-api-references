# ConnectionPendingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConnectionPendingException

```
open class ConnectionPendingException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) ||
| | | | | ↳ | [java.nio.channels.ConnectionPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/ConnectionPendingException#) |

Unchecked exception thrown when an attempt is made to connect a [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) for which a non-blocking connection operation is already in progress.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConnectionPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/ConnectionPendingException#ConnectionPendingException())`()` Constructs an instance of this class. |

## Public constructors

### ConnectionPendingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConnectionPendingException()
```

Constructs an instance of this class.
