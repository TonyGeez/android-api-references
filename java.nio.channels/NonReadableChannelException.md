# NonReadableChannelException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NonReadableChannelException

```
open class NonReadableChannelException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) ||
| | | | | ↳ | [java.nio.channels.NonReadableChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/NonReadableChannelException#) |

Unchecked exception thrown when an attempt is made to read from a channel that was not originally opened for reading.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NonReadableChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/NonReadableChannelException#NonReadableChannelException())`()` Constructs an instance of this class. |

## Public constructors

### NonReadableChannelException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NonReadableChannelException()
```

Constructs an instance of this class.
