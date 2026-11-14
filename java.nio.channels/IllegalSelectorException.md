# IllegalSelectorException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalSelectorException

```
open class IllegalSelectorException : IllegalArgumentException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](../java/lang/IllegalArgumentException.md) ||
| | | | | ↳ | [java.nio.channels.IllegalSelectorException](../java/nio/channels/IllegalSelectorException.md) |

Unchecked exception thrown when an attempt is made to register a channel with a selector that was not created by the provider that created the channel.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalSelectorException](../java/nio/channels/IllegalSelectorException.md))`()` Constructs an instance of this class. |

## Public constructors

### IllegalSelectorException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalSelectorException()
```

Constructs an instance of this class.
