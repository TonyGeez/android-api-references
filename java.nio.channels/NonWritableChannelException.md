# NonWritableChannelException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NonWritableChannelException

```
open class NonWritableChannelException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java/lang/IllegalStateException.md) ||
| | | | | ↳ | [java.nio.channels.NonWritableChannelException](../java/nio/channels/NonWritableChannelException.md) |

Unchecked exception thrown when an attempt is made to write to a channel that was not originally opened for writing.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NonWritableChannelException](../java/nio/channels/NonWritableChannelException.md))`()` Constructs an instance of this class. |

## Public constructors

### NonWritableChannelException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NonWritableChannelException()
```

Constructs an instance of this class.
