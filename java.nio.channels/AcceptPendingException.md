# AcceptPendingException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AcceptPendingException

```
open class AcceptPendingException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java.lang/IllegalStateException.md) ||
| | | | | ↳ | [java.nio.channels.AcceptPendingException](AcceptPendingException.md) |

Unchecked exception thrown when an attempt is made to initiate an accept operation on a channel and a previous accept operation has not completed.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AcceptPendingException](AcceptPendingException.md))`()` Constructs an instance of this class. |

## Public constructors

### AcceptPendingException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AcceptPendingException()
```

Constructs an instance of this class.
