# IllegalChannelGroupException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalChannelGroupException

```
open class IllegalChannelGroupException : IllegalArgumentException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](../java/lang/IllegalArgumentException.md) ||
| | | | | ↳ | [java.nio.channels.IllegalChannelGroupException](../java/nio/channels/IllegalChannelGroupException.md) |

Unchecked exception thrown when an attempt is made to open a channel in a group that was not created by the same provider.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalChannelGroupException](../java/nio/channels/IllegalChannelGroupException.md))`()` Constructs an instance of this class. |

## Public constructors

### IllegalChannelGroupException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalChannelGroupException()
```

Constructs an instance of this class.
