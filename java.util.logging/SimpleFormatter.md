# SimpleFormatter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimpleFormatter

```
open class SimpleFormatter : Formatter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.logging.Formatter](Formatter.md) ||
| | ↳ | [java.util.logging.SimpleFormatter](SimpleFormatter.md) |

Print a brief summary of the`LogRecord`in a human readable format. The summary will typically be 1 or 2 lines.

**Configuration:**The`SimpleFormatter`is initialized with the [format string](../java.util/Formatter.md) specified in the`java.util.logging.SimpleFormatter.format`property to [format](SimpleFormatter.md))the log messages. This property can be defined in the [logging properties](LogManager.md))configuration file or as a system property. If this property is set in both the logging properties and system properties, the format string specified in the system property will be used. If this property is not defined or the given format string is [illegal](../java.util/IllegalFormatException.md), the default format is implementation-specific.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------|---|
| [SimpleFormatter](SimpleFormatter.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](SimpleFormatter.md))`(`record:` ` [LogRecord](LogRecord.md)!`)` Format the given LogRecord. |

| Inherited functions ||
|---|---|
| From class [Formatter](Formatter.md) |-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatMessage](Formatter.md))`(`record:` ` [LogRecord](LogRecord.md)!`)` <br /> Localize and format the message string from a log record. This method is provided as a convenience for Formatter subclasses to use when they are performing formatting. The message string is first localized to a format string using the record's ResourceBundle. (If there is no ResourceBundle, or if the message key is not found, then the key is used as the format string.) The format String uses java.text style formatting. - If there are no parameters, no formatter is used. - Otherwise, if the string contains "{0" then java.text.MessageFormat is used to format the string. - Otherwise no formatting is performed. <br /> <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHead](Formatter.md))`(`h:` ` [Handler](Handler.md)!`)` <br /> Return the header string for a set of formatted records. This base class returns an empty string, but this may be overridden by subclasses. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTail](Formatter.md))`(`h:` ` [Handler](Handler.md)!`)` <br /> Return the tail string for a set of formatted records. This base class returns an empty string, but this may be overridden by subclasses. <br /> | ||

## Public constructors

### SimpleFormatter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleFormatter()
```

## Public methods

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(record: LogRecord!): String!
```

Format the given LogRecord.

The formatting can be customized by specifying the [format string](../java.util/Formatter.md) in the [`java.util.logging.SimpleFormatter.format`](SimpleFormatter.md) property. The given`LogRecord`will be formatted as if by calling: 

```kotlin
java.lang.String#format(format, date, source, logger, level, message, thrown);
  
```
where the arguments are: 

1. `format`- the [java.util.Formatter](../java.util/Formatter.md) format string specified in the`java.util.logging.SimpleFormatter.format`property or the default format.
2. `date`- a [Date](../java.util/Date.md) object representing [event time](LogRecord.md))of the log record.
3. `source`- a string representing the caller, if available; otherwise, the logger's name.
4. `logger`- the logger's name.
5. `level`- the [log level](Level.md)).
6. `message`- the formatted log message returned from the [Formatter.formatMessage(LogRecord)](Formatter.md))method. It uses [java.text](../java.text/MessageFormat.md) formatting and does not use the`java.util.Formatter format`argument.
7. `thrown`- a string representing the [throwable](LogRecord.md))associated with the log record and its backtrace beginning with a newline character, if any; otherwise, an empty string.

Some example formats: 

- `java.util.logging.SimpleFormatter.format="%4$s: %5$s [%1$tc]%n"`

 This prints 1 line with the log level (`4$`), the log message (`5$`) and the timestamp (`1$`) in a square bracket. 

  ```kotlin
  WARNING: warning message [Tue Mar 22 13:11:31 PDT 2011]
        
  ```
- `java.util.logging.SimpleFormatter.format="%1$tc %2$s%n%4$s: %5$s%6$s%n"`

 This prints 2 lines where the first line includes the timestamp (`1$`) and the source (`2$`); the second line includes the log level (`4$`) and the log message (`5$`) followed with the throwable and its backtrace (`6$`), if any: 

  ```kotlin
  Tue Mar 22 13:11:31 PDT 2011 MyClass fatal
        SEVERE: several message with an exception
        java.lang.IllegalArgumentException: invalid argument
                at MyClass.mash(MyClass.java:9)
                at MyClass.crunch(MyClass.java:6)
                at MyClass.main(MyClass.java:3)
        
  ```
- `java.util.logging.SimpleFormatter.format="%1$tb %1$td, %1$tY %1$tl:%1$tM:%1$tS %1$Tp %2$s%n%4$s: %5$s%n"`

 This prints 2 lines similar to the example above with a different date/time formatting and does not print the throwable and its backtrace: 

  ```kotlin
  Mar 22, 2011 1:11:31 PM MyClass fatal
        SEVERE: several message with an exception
        
  ```

This method can also be overridden in a subclass. It is recommended to use the [Formatter.formatMessage](Formatter.md))convenience method to localize and format the message field.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------|
| `record` | [LogRecord](LogRecord.md)!:the log record to be formatted. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a formatted log record |
