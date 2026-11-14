# NonWritableChannelException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NonWritableChannelException

```
open class NonWritableChannelException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) ||
| | | | | ↳ | [java.nio.channels.NonWritableChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/NonWritableChannelException#) |

Unchecked exception thrown when an attempt is made to write to a channel that was not originally opened for writing.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NonWritableChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/NonWritableChannelException#NonWritableChannelException())`()` Constructs an instance of this class. |

## Public constructors

### NonWritableChannelException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NonWritableChannelException()
```

Constructs an instance of this class.
