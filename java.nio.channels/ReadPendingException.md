# ReadPendingException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReadPendingException

```
open class ReadPendingException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) ||
| | | | | ↳ | [java.nio.channels.ReadPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/ReadPendingException#) |

Unchecked exception thrown when an attempt is made to read from an asynchronous socket channel and a previous read has not completed.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ReadPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/ReadPendingException#ReadPendingException())`()` Constructs an instance of this class. |

## Public constructors

### ReadPendingException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReadPendingException()
```

Constructs an instance of this class.
