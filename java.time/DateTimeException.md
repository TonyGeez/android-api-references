# DateTimeException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateTimeException

```
open class DateTimeException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.time.DateTimeException](DateTimeException.md) |

| Known Direct Subclasses [DateTimeParseException](../java.time.format/DateTimeParseException.md), [UnsupportedTemporalTypeException](../java.time.temporal/UnsupportedTemporalTypeException.md), [ZoneRulesException](../java.time.zone/ZoneRulesException.md) |----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------| | [DateTimeParseException](../java.time.format/DateTimeParseException.md) | An exception thrown when an error occurs during parsing. | | [UnsupportedTemporalTypeException](../java.time.temporal/UnsupportedTemporalTypeException.md) | UnsupportedTemporalTypeException indicates that a ChronoField or ChronoUnit is not supported for a Temporal class. | | [ZoneRulesException](../java.time.zone/ZoneRulesException.md) | Thrown to indicate a problem with time-zone configuration. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Exception used to indicate a problem while calculating a date-time.

This exception is used to indicate problems with creating, querying and manipulating date-time objects.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DateTimeException](DateTimeException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new date-time exception with the specified message. |
| [DateTimeException](DateTimeException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new date-time exception with the specified message and cause. |

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
