# StreamHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StreamHandler

```
open class StreamHandler : Handler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.util.logging.Handler](https://developer.android.com/reference/kotlin/java/util/logging/Handler) ||
| | ↳ | [java.util.logging.StreamHandler](https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler#) |

| Known Direct Subclasses [ConsoleHandler](https://developer.android.com/reference/kotlin/java/util/logging/ConsoleHandler), [FileHandler](https://developer.android.com/reference/kotlin/java/util/logging/FileHandler), [SocketHandler](https://developer.android.com/reference/kotlin/java/util/logging/SocketHandler) |---------------------------------------------------------------------------------------------------|---------------------------------------------------| | [ConsoleHandler](https://developer.android.com/reference/kotlin/java/util/logging/ConsoleHandler) | This Handler publishes log records to System.err. | | [FileHandler](https://developer.android.com/reference/kotlin/java/util/logging/FileHandler) | Simple file logging Handler. | | [SocketHandler](https://developer.android.com/reference/kotlin/java/util/logging/SocketHandler) | Simple network logging Handler. | |

Stream based logging Handler.

This is primarily intended as a base class or support class to be used in implementing other logging Handlers.

LogRecords are published to a given java.io.OutputStream.

**Configuration:**By default each StreamHandler is initialized using the following LogManager configuration properties where \<handler-name\> refers to the fully-qualified class name of the handler. If properties are not defined (or have invalid values) then the specified default values are used.

- \<handler-name\>.level specifies the default level for the Handler (defaults to Level.INFO).
- \<handler-name\>.filter specifies the name of a Filter class to use (defaults to no Filter).
- \<handler-name\>.formatter specifies the name of a Formatter class to use (defaults to java.util.logging.SimpleFormatter).
- \<handler-name\>.encoding the name of the character set encoding to use (defaults to the default platform encoding).

For example, the properties for`StreamHandler`would be:

- java.util.logging.StreamHandler.level=INFO
- java.util.logging.StreamHandler.formatter=java.util.logging.SimpleFormatter

For a custom handler, e.g. com.foo.MyHandler, the properties would be:

- com.foo.MyHandler.level=INFO
- com.foo.MyHandler.formatter=java.util.logging.SimpleFormatter

<br />

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StreamHandler](https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler#StreamHandler())`()` Create a StreamHandler, with no current output stream. |
| [StreamHandler](https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler#StreamHandler(java.io.OutputStream,%20java.util.logging.Formatter))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`, `formatter:` ` [Formatter](https://developer.android.com/reference/kotlin/java/util/logging/Formatter)!`)` Create a StreamHandler with a given Formatter and output stream. |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler#close())`()` Close the current output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler#flush())`()` Flush any buffered messages. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoggable](https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler#isLoggable(java.util.logging.LogRecord))`(`record:` ` [LogRecord](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord)!`)` Check if this Handler would actually log a given LogRecord. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [publish](https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler#publish(java.util.logging.LogRecord))`(`record:` ` [LogRecord](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord)!`)` Format and publish a LogRecord. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEncoding](https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler#setEncoding(kotlin.String))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set (or change) the character encoding used by this Handler. |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutputStream](https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler#setOutputStream(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` Change the output stream. |

| Inherited functions ||
|---|---|
| From class [Handler](https://developer.android.com/reference/kotlin/java/util/logging/Handler) |------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](https://developer.android.com/reference/kotlin/java/util/logging/Handler#getEncoding())`()` <br /> Return the character encoding for this Handler. <br /> | | [ErrorManager](https://developer.android.com/reference/kotlin/java/util/logging/ErrorManager)! | [getErrorManager](https://developer.android.com/reference/kotlin/java/util/logging/Handler#getErrorManager())`()` <br /> Retrieves the ErrorManager for this Handler. <br /> | | [Filter](https://developer.android.com/reference/kotlin/java/util/logging/Filter)! | [getFilter](https://developer.android.com/reference/kotlin/java/util/logging/Handler#getFilter())`()` <br /> Get the current Filter for this Handler. <br /> | | [Formatter](https://developer.android.com/reference/kotlin/java/util/logging/Formatter)! | [getFormatter](https://developer.android.com/reference/kotlin/java/util/logging/Handler#getFormatter())`()` <br /> Return the Formatter for this Handler. <br /> | | [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level)! | [getLevel](https://developer.android.com/reference/kotlin/java/util/logging/Handler#getLevel())`()` <br /> Get the log level specifying which messages will be logged by this Handler. Message levels lower than this level will be discarded. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reportError](https://developer.android.com/reference/kotlin/java/util/logging/Handler#reportError(kotlin.String,%20java.lang.Exception,%20kotlin.Int))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ex:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Protected convenience method to report an error to this Handler's ErrorManager. Note that this method retrieves and uses the ErrorManager without doing a security check. It can therefore be used in environments where the caller may be non-privileged. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorManager](https://developer.android.com/reference/kotlin/java/util/logging/Handler#setErrorManager(java.util.logging.ErrorManager))`(`em:` ` [ErrorManager](https://developer.android.com/reference/kotlin/java/util/logging/ErrorManager)!`)` <br /> Define an ErrorManager for this Handler. The ErrorManager's "error" method will be invoked if any errors occur while using this Handler. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilter](https://developer.android.com/reference/kotlin/java/util/logging/Handler#setFilter(java.util.logging.Filter))`(`newFilter:` ` [Filter](https://developer.android.com/reference/kotlin/java/util/logging/Filter)!`)` <br /> Set a Filter to control output on this Handler. For each call of publish the Handler will call this Filter (if it is non-null) to check if the LogRecord should be published or discarded. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormatter](https://developer.android.com/reference/kotlin/java/util/logging/Handler#setFormatter(java.util.logging.Formatter))`(`newFormatter:` ` [Formatter](https://developer.android.com/reference/kotlin/java/util/logging/Formatter)!`)` <br /> Set a Formatter. This Formatter will be used to format LogRecords for this Handler. Some Handlers may not use Formatters, in which case the Formatter will be remembered, but not used. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLevel](https://developer.android.com/reference/kotlin/java/util/logging/Handler#setLevel(java.util.logging.Level))`(`newLevel:` ` [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level)!`)` <br /> Set the log level specifying which message levels will be logged by this Handler. Message levels lower than this value will be discarded. The intention is to allow developers to turn on voluminous logging, but to limit the messages that are sent to certain Handlers. <br /> | ||

## Public constructors

### StreamHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StreamHandler()
```

Create a StreamHandler, with no current output stream. 

### StreamHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StreamHandler(
    out: OutputStream!, 
    formatter: Formatter!)
```

Create a StreamHandler with a given Formatter and output stream.

<br />

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:the target output stream |
| `formatter` | [Formatter](https://developer.android.com/reference/kotlin/java/util/logging/Formatter)!:Formatter to be used to format output |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Close the current output stream.

The Formatter's "tail" string is written to the stream before it is closed. In addition, if the Formatter's "head" string has not yet been written to the stream, it will be written before the "tail" string.

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Flush any buffered messages. 

### isLoggable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLoggable(record: LogRecord!): Boolean
```

Check if this Handler would actually log a given LogRecord.

This method checks if the LogRecord has an appropriate level and whether it satisfies any Filter. It will also return false if no output stream has been assigned yet or the LogRecord is null.

<br />

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `record` | [LogRecord](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord)!:a LogRecord |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the LogRecord would be logged. |

### publish

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun publish(record: LogRecord!): Unit
```

Format and publish a LogRecord.

The StreamHandler first checks if there is an OutputStream and if the given LogRecord has at least the required log level. If not it silently returns. If so, it calls any associated Filter to check if the record should be published. If so, it calls its Formatter to format the record and then writes the result to the current output stream.

If this is the first LogRecord to be written to a given OutputStream, the Formatter's "head" string is written to the stream before the LogRecord is written.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `record` | [LogRecord](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord)!:description of the log event. A null record is silently ignored and is not published |

### setEncoding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEncoding(encoding: String!): Unit
```

Set (or change) the character encoding used by this Handler.

The encoding should be set before any LogRecords are written to the Handler.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `encoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of a supported character encoding. May be null, to indicate the default platform encoding. |

| Exceptions ||
|----------------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |
| `java.io.UnsupportedEncodingException` | if the named encoding is not supported. |

## Protected methods

### setOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setOutputStream(out: OutputStream!): Unit
```

Change the output stream.

If there is a current output stream then the Formatter's tail string is written and the stream is flushed and closed. Then the output stream is replaced with the new output stream.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:New output stream. May not be null. |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |
