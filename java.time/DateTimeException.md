# DateTimeException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateTimeException

```
open class DateTimeException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| | | | ↳ | [java.time.DateTimeException](https://developer.android.com/reference/kotlin/java/time/DateTimeException#) |

| Known Direct Subclasses [DateTimeParseException](https://developer.android.com/reference/kotlin/java/time/format/DateTimeParseException), [UnsupportedTemporalTypeException](https://developer.android.com/reference/kotlin/java/time/temporal/UnsupportedTemporalTypeException), [ZoneRulesException](https://developer.android.com/reference/kotlin/java/time/zone/ZoneRulesException) |----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------| | [DateTimeParseException](https://developer.android.com/reference/kotlin/java/time/format/DateTimeParseException) | An exception thrown when an error occurs during parsing. | | [UnsupportedTemporalTypeException](https://developer.android.com/reference/kotlin/java/time/temporal/UnsupportedTemporalTypeException) | UnsupportedTemporalTypeException indicates that a ChronoField or ChronoUnit is not supported for a Temporal class. | | [ZoneRulesException](https://developer.android.com/reference/kotlin/java/time/zone/ZoneRulesException) | Thrown to indicate a problem with time-zone configuration. | |

Exception used to indicate a problem while calculating a date-time.

This exception is used to indicate problems with creating, querying and manipulating date-time objects.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DateTimeException](https://developer.android.com/reference/kotlin/java/time/DateTimeException#DateTimeException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new date-time exception with the specified message. |
| [DateTimeException](https://developer.android.com/reference/kotlin/java/time/DateTimeException#DateTimeException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new date-time exception with the specified message and cause. |

## Public constructors

### DateTimeException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateTimeException(message: String!)
```

Constructs a new date-time exception with the specified message.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the message to use for this exception, may be null |

### DateTimeException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateTimeException(
    message: String!, 
    cause: Throwable!)
```

Constructs a new date-time exception with the specified message and cause.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the message to use for this exception, may be null |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause of the exception, may be null |
