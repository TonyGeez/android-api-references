# ReadPendingException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReadPendingException

```
open class ReadPendingException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java.lang/IllegalStateException.md) ||
| | | | | ↳ | [java.nio.channels.ReadPendingException](ReadPendingException.md) |

Unchecked exception thrown when an attempt is made to read from an asynchronous socket channel and a previous read has not completed.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ReadPendingException](ReadPendingException.md))`()` Constructs an instance of this class. |

## Public constructors

### ReadPendingException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReadPendingException()
```

Constructs an instance of this class.
