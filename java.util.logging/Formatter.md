# Formatter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Formatter

```
abstract class Formatter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.logging.Formatter](Formatter.md) |

| Known Direct Subclasses [SimpleFormatter](SimpleFormatter.md), [XMLFormatter](XMLFormatter.md) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------| | [SimpleFormatter](SimpleFormatter.md) | Print a brief summary of the`LogRecord`in a human readable format. | | [XMLFormatter](XMLFormatter.md) | Format a LogRecord into a standard XML format. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A Formatter provides support for formatting LogRecords.

Typically each logging Handler will have a Formatter associated with it. The Formatter takes a LogRecord and converts it to a string.

Some formatters (such as the XMLFormatter) need to wrap head and tail strings around a set of formatted records. The getHeader and getTail methods can be used to obtain these strings.

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------|---|
| [Formatter](Formatter.md))`()` Construct a new formatter. |

| Public methods ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](Formatter.md))`(`record:` ` [LogRecord](LogRecord.md)!`)` Format the given log record and return the formatted string. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatMessage](Formatter.md))`(`record:` ` [LogRecord](LogRecord.md)!`)` Localize and format the message string from a log record. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHead](Formatter.md))`(`h:` ` [Handler](Handler.md)!`)` Return the header string for a set of formatted records. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTail](Formatter.md))`(`h:` ` [Handler](Handler.md)!`)` Return the tail string for a set of formatted records. |

## Protected constructors

### Formatter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Formatter()
```

Construct a new formatter.

## Public methods

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun format(record: LogRecord!): String!
```

Format the given log record and return the formatted string.

The resulting formatted String will normally include a localized and formatted version of the LogRecord's message field. It is recommended to use the [Formatter.formatMessage](Formatter.md))convenience method to localize and format the message field.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------|
| `record` | [LogRecord](LogRecord.md)!:the log record to be formatted. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the formatted log record |

### formatMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun formatMessage(record: LogRecord!): String!
```

Localize and format the message string from a log record. This method is provided as a convenience for Formatter subclasses to use when they are performing formatting.

The message string is first localized to a format string using the record's ResourceBundle. (If there is no ResourceBundle, or if the message key is not found, then the key is used as the format string.) The format String uses java.text style formatting.

- If there are no parameters, no formatter is used.
- Otherwise, if the string contains "{0" then java.text.MessageFormat is used to format the string.
- Otherwise no formatting is performed.

<br />

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `record` | [LogRecord](LogRecord.md)!:the log record containing the raw message |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a localized and formatted message |

### getHead

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHead(h: Handler!): String!
```

Return the header string for a set of formatted records.

This base class returns an empty string, but this may be overridden by subclasses.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------|
| `h` | [Handler](Handler.md)!:The target handler (can be null) |

| Return ||
|-----------------------------------------------------------------------------------|---------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | header string |

### getTail

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTail(h: Handler!): String!
```

Return the tail string for a set of formatted records.

This base class returns an empty string, but this may be overridden by subclasses.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------|
| `h` | [Handler](Handler.md)!:The target handler (can be null) |

| Return ||
|-----------------------------------------------------------------------------------|-------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | tail string |
