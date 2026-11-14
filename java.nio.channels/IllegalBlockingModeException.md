# IllegalBlockingModeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalBlockingModeException

```
open class IllegalBlockingModeException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) ||
| | | | | ↳ | [java.nio.channels.IllegalBlockingModeException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalBlockingModeException#) |

Unchecked exception thrown when a blocking-mode-specific operation is invoked upon a channel in the incorrect blocking mode.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalBlockingModeException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalBlockingModeException#IllegalBlockingModeException())`()` Constructs an instance of this class. |

## Public constructors

### IllegalBlockingModeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalBlockingModeException()
```

Constructs an instance of this class.
