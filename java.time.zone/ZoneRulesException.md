# ZoneRulesException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZoneRulesException

```
open class ZoneRulesException : DateTimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.time.DateTimeException](https://developer.android.com/reference/kotlin/java/time/DateTimeException.html#) ||
| | | | | ↳ | [java.time.zone.ZoneRulesException](https://developer.android.com/reference/kotlin/java/time/zone/ZoneRulesException#) |

Thrown to indicate a problem with time-zone configuration.

This exception is used to indicate a problems with the configured time-zone rules.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ZoneRulesException](https://developer.android.com/reference/kotlin/java/time/zone/ZoneRulesException#ZoneRulesException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new date-time exception with the specified message. |
| [ZoneRulesException](https://developer.android.com/reference/kotlin/java/time/zone/ZoneRulesException#ZoneRulesException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new date-time exception with the specified message and cause. |

## Public constructors

### ZoneRulesException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZoneRulesException(message: String!)
```

Constructs a new date-time exception with the specified message.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the message to use for this exception, may be null |

### ZoneRulesException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZoneRulesException(
    message: String!, 
    cause: Throwable!)
```

Constructs a new date-time exception with the specified message and cause.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the message to use for this exception, may be null |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause of the exception, may be null |
