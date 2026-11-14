# NonReadableChannelException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NonReadableChannelException

```
open class NonReadableChannelException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java/lang/IllegalStateException.md) ||
| | | | | ↳ | [java.nio.channels.NonReadableChannelException](../java/nio/channels/NonReadableChannelException.md) |

Unchecked exception thrown when an attempt is made to read from a channel that was not originally opened for reading.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NonReadableChannelException](../java/nio/channels/NonReadableChannelException.md))`()` Constructs an instance of this class. |

## Public constructors

### NonReadableChannelException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NonReadableChannelException()
```

Constructs an instance of this class.
