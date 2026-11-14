# SocketHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketHandler

```
open class SocketHandler : StreamHandler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.logging.Handler](Handler.md) |||
| | ↳ | [java.util.logging.StreamHandler](StreamHandler.md) ||
| | | ↳ | [java.util.logging.SocketHandler](SocketHandler.md) |
| --- | --- | --- | --- |

Simple network logging Handler.

LogRecords are published to a network stream connection. By default the XMLFormatter class is used for formatting.

**Configuration:**By default each SocketHandler is initialized using the following LogManager configuration properties where \<handler-name\> refers to the fully-qualified class name of the handler. If properties are not defined (or have invalid values) then the specified default values are used.

- \<handler-name\>.level specifies the default level for the Handler (defaults to Level.ALL).
- \<handler-name\>.filter specifies the name of a Filter class to use (defaults to no Filter).
- \<handler-name\>.formatter specifies the name of a Formatter class to use (defaults to java.util.logging.XMLFormatter).
- \<handler-name\>.encoding the name of the character set encoding to use (defaults to the default platform encoding).
- \<handler-name\>.host specifies the target host name to connect to (no default).
- \<handler-name\>.port specifies the target TCP port to use (no default).

For example, the properties for`SocketHandler`would be:

- java.util.logging.SocketHandler.level=INFO
- java.util.logging.SocketHandler.formatter=java.util.logging.SimpleFormatter

For a custom handler, e.g. com.foo.MyHandler, the properties would be:

- com.foo.MyHandler.level=INFO
- com.foo.MyHandler.formatter=java.util.logging.SimpleFormatter

The output IO stream is buffered, but is flushed after each LogRecord is written.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SocketHandler](SocketHandler.md))`()` Create a SocketHandler, using only LogManager properties (or their defaults). |
| [SocketHandler](SocketHandler.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct a SocketHandler using a specified host and port. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](SocketHandler.md))`()` Close this output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [publish](SocketHandler.md))`(`record:` ` [LogRecord](LogRecord.md)!`)` Format and publish a LogRecord. |

| Inherited functions ||
|---|---|
| From class [StreamHandler](StreamHandler.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](StreamHandler.md))`()` <br /> Flush any buffered messages. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoggable](StreamHandler.md))`(`record:` ` [LogRecord](LogRecord.md)!`)` <br /> Check if this Handler would actually log a given LogRecord. This method checks if the LogRecord has an appropriate level and whether it satisfies any Filter. It will also return false if no output stream has been assigned yet or the LogRecord is null. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEncoding](StreamHandler.md))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Set (or change) the character encoding used by this Handler. The encoding should be set before any LogRecords are written to the Handler. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutputStream](StreamHandler.md))`(`out:` ` [OutputStream](../java.io/OutputStream.md)!`)` <br /> Change the output stream. If there is a current output stream then the Formatter's tail string is written and the stream is flushed and closed. Then the output stream is replaced with the new output stream. <br /> | ||
| From class [Handler](Handler.md) |------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](Handler.md))`()` <br /> Return the character encoding for this Handler. <br /> | | [ErrorManager](ErrorManager.md)! | [getErrorManager](Handler.md))`()` <br /> Retrieves the ErrorManager for this Handler. <br /> | | [Filter](Filter.md)! | [getFilter](Handler.md))`()` <br /> Get the current Filter for this Handler. <br /> | | [Formatter](Formatter.md)! | [getFormatter](Handler.md))`()` <br /> Return the Formatter for this Handler. <br /> | | [Level](Level.md)! | [getLevel](Handler.md))`()` <br /> Get the log level specifying which messages will be logged by this Handler. Message levels lower than this level will be discarded. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reportError](Handler.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ex:` ` [Exception](../java.lang/Exception.md)!`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Protected convenience method to report an error to this Handler's ErrorManager. Note that this method retrieves and uses the ErrorManager without doing a security check. It can therefore be used in environments where the caller may be non-privileged. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorManager](Handler.md))`(`em:` ` [ErrorManager](ErrorManager.md)!`)` <br /> Define an ErrorManager for this Handler. The ErrorManager's "error" method will be invoked if any errors occur while using this Handler. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilter](Handler.md))`(`newFilter:` ` [Filter](Filter.md)!`)` <br /> Set a Filter to control output on this Handler. For each call of publish the Handler will call this Filter (if it is non-null) to check if the LogRecord should be published or discarded. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormatter](Handler.md))`(`newFormatter:` ` [Formatter](Formatter.md)!`)` <br /> Set a Formatter. This Formatter will be used to format LogRecords for this Handler. Some Handlers may not use Formatters, in which case the Formatter will be remembered, but not used. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLevel](Handler.md))`(`newLevel:` ` [Level](Level.md)!`)` <br /> Set the log level specifying which message levels will be logged by this Handler. Message levels lower than this value will be discarded. The intention is to allow developers to turn on voluminous logging, but to limit the messages that are sent to certain Handlers. <br /> | ||

## Public constructors

### SocketHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SocketHandler()
```

Create a SocketHandler, using only LogManager properties (or their defaults).

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the host or port are invalid or are not specified as LogManager properties. |
| `java.io.IOException` | if we are unable to connect to the target host and port. |

### SocketHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SocketHandler(
    host: String!, 
    port: Int)
```

Construct a SocketHandler using a specified host and port. The SocketHandler is configured based on LogManager properties (or their default values) except that the given target host and port arguments are used. If the host argument is empty, but not null String then the localhost is used.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:target host. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):target port. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the host or port are invalid. |
| `java.io.IOException` | if we are unable to connect to the target host and port. |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Close this output stream.

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |

### publish

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun publish(record: LogRecord!): Unit
```

Format and publish a LogRecord.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `record` | [LogRecord](LogRecord.md)!:description of the log event. A null record is silently ignored and is not published |
