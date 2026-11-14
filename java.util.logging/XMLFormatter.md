# XMLFormatter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XMLFormatter

```
open class XMLFormatter : Formatter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.logging.Formatter](../java/util/logging/Formatter.md) ||
| | ↳ | [java.util.logging.XMLFormatter](../java/util/logging/XMLFormatter.md) |

Format a LogRecord into a standard XML format.

The DTD specification is provided as Appendix A to the Java Logging APIs specification.

The XMLFormatter can be used with arbitrary character encodings, but it is recommended that it normally be used with UTF-8. The character encoding can be set on the output Handler.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------|---|
| [XMLFormatter](../java/util/logging/XMLFormatter.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../java/util/logging/XMLFormatter.md))`(`record:` ` [LogRecord](../java/util/logging/LogRecord.md)!`)` Format the given message to XML. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHead](../java/util/logging/XMLFormatter.md))`(`h:` ` [Handler](../java/util/logging/Handler.md)!`)` Return the header string for a set of XML formatted records. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTail](../java/util/logging/XMLFormatter.md))`(`h:` ` [Handler](../java/util/logging/Handler.md)!`)` Return the tail string for a set of XML formatted records. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Formatter](../java/util/logging/Formatter.md) |-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatMessage](../java/util/logging/Formatter.md))`(`record:` ` [LogRecord](../java/util/logging/LogRecord.md)!`)` <br /> Localize and format the message string from a log record. This method is provided as a convenience for Formatter subclasses to use when they are performing formatting. The message string is first localized to a format string using the record's ResourceBundle. (If there is no ResourceBundle, or if the message key is not found, then the key is used as the format string.) The format String uses java.text style formatting. - If there are no parameters, no formatter is used. - Otherwise, if the string contains "{0" then java.text.MessageFormat is used to format the string. - Otherwise no formatting is performed. <br /> <br /> | ||

## Public constructors

### XMLFormatter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
XMLFormatter()
```

## Public methods

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(record: LogRecord!): String!
```

Format the given message to XML.

This method can be overridden in a subclass. It is recommended to use the [Formatter.formatMessage](../java/util/logging/Formatter.md))convenience method to localize and format the message field.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------|
| `record` | [LogRecord](../java/util/logging/LogRecord.md)!:the log record to be formatted. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a formatted log record |

### getHead

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHead(h: Handler!): String!
```

Return the header string for a set of XML formatted records.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------|
| `h` | [Handler](../java/util/logging/Handler.md)!:The target handler (can be null) |

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a valid XML string |

### getTail

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTail(h: Handler!): String!
```

Return the tail string for a set of XML formatted records.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------|
| `h` | [Handler](../java/util/logging/Handler.md)!:The target handler (can be null) |

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a valid XML string |
