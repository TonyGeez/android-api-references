# WritePendingException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WritePendingException

```
open class WritePendingException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) ||
| | | | | ↳ | [java.nio.channels.WritePendingException](https://developer.android.com/reference/kotlin/java/nio/channels/WritePendingException#) |

Unchecked exception thrown when an attempt is made to write to an asynchronous socket channel and a previous write has not completed.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WritePendingException](https://developer.android.com/reference/kotlin/java/nio/channels/WritePendingException#WritePendingException())`()` Constructs an instance of this class. |

## Public constructors

### WritePendingException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WritePendingException()
```

Constructs an instance of this class.
