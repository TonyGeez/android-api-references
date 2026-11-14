# UnsupportedTemporalTypeException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsupportedTemporalTypeException

```
open class UnsupportedTemporalTypeException : DateTimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.time.DateTimeException](../java.time/DateTimeException.md) ||
| | | | | ↳ | [java.time.temporal.UnsupportedTemporalTypeException](UnsupportedTemporalTypeException.md) |

UnsupportedTemporalTypeException indicates that a ChronoField or ChronoUnit is not supported for a Temporal class.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnsupportedTemporalTypeException](UnsupportedTemporalTypeException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new UnsupportedTemporalTypeException with the specified message. |
| [UnsupportedTemporalTypeException](UnsupportedTemporalTypeException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new UnsupportedTemporalTypeException with the specified message and cause. |

## Public constructors

### UnsupportedTemporalTypeException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnsupportedTemporalTypeException(message: String!)
```

Constructs a new UnsupportedTemporalTypeException with the specified message.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the message to use for this exception, may be null |

### UnsupportedTemporalTypeException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnsupportedTemporalTypeException(
    message: String!, 
    cause: Throwable!)
```

Constructs a new UnsupportedTemporalTypeException with the specified message and cause.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the message to use for this exception, may be null |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause of the exception, may be null |
