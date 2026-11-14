# ShutdownChannelGroupException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ShutdownChannelGroupException

```
open class ShutdownChannelGroupException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) ||
| | | | | ↳ | [java.nio.channels.ShutdownChannelGroupException](https://developer.android.com/reference/kotlin/java/nio/channels/ShutdownChannelGroupException#) |

Unchecked exception thrown when an attempt is made to construct a channel in a group that is shutdown or the completion handler for an I/O operation cannot be invoked because the channel group has terminated.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ShutdownChannelGroupException](https://developer.android.com/reference/kotlin/java/nio/channels/ShutdownChannelGroupException#ShutdownChannelGroupException())`()` Constructs an instance of this class. |

## Public constructors

### ShutdownChannelGroupException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ShutdownChannelGroupException()
```

Constructs an instance of this class.
