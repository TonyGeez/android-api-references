# UnsupportedTemporalTypeException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsupportedTemporalTypeException

```
open class UnsupportedTemporalTypeException : DateTimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [java.time.DateTimeException](https://developer.android.com/reference/kotlin/java/time/DateTimeException.html#) ||
| | | | | ↳ | [java.time.temporal.UnsupportedTemporalTypeException](https://developer.android.com/reference/kotlin/java/time/temporal/UnsupportedTemporalTypeException#) |

UnsupportedTemporalTypeException indicates that a ChronoField or ChronoUnit is not supported for a Temporal class.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnsupportedTemporalTypeException](https://developer.android.com/reference/kotlin/java/time/temporal/UnsupportedTemporalTypeException#UnsupportedTemporalTypeException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new UnsupportedTemporalTypeException with the specified message. |
| [UnsupportedTemporalTypeException](https://developer.android.com/reference/kotlin/java/time/temporal/UnsupportedTemporalTypeException#UnsupportedTemporalTypeException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new UnsupportedTemporalTypeException with the specified message and cause. |

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
