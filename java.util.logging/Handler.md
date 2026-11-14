# Handler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Handler

```
abstract class Handler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.logging.Handler](../java/util/logging/Handler.md) |

| Known Direct Subclasses [MemoryHandler](../java/util/logging/MemoryHandler.md), [StreamHandler](../java/util/logging/StreamHandler.md) |-------------------------------------------------------------------------------------------------|---------------------------------------------------------------| | [MemoryHandler](../java/util/logging/MemoryHandler.md) | Handler that buffers requests in a circular buffer in memory. | | [StreamHandler](../java/util/logging/StreamHandler.md) | Stream based logging Handler. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ConsoleHandler](../java/util/logging/ConsoleHandler.md), [FileHandler](../java/util/logging/FileHandler.md), [SocketHandler](../java/util/logging/SocketHandler.md) |---------------------------------------------------------------------------------------------------|---------------------------------------------------| | [ConsoleHandler](../java/util/logging/ConsoleHandler.md) | This Handler publishes log records to System.err. | | [FileHandler](../java/util/logging/FileHandler.md) | Simple file logging Handler. | | [SocketHandler](../java/util/logging/SocketHandler.md) | Simple network logging Handler. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A Handler object takes log messages from a Logger and exports them. It might for example, write them to a console or write them to a file, or send them to a network logging service, or forward them to an OS log, or whatever.

A Handler can be disabled by doing a setLevel(Level.OFF) and can be re-enabled by doing a setLevel with an appropriate level.

Handler classes typically use LogManager properties to set default values for the Handler's Filter, Formatter, and Level. See the specific documentation for each concrete Handler class.

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------|---|
| [Handler](../java/util/logging/Handler.md))`()` Default constructor. |

| Public methods ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/util/logging/Handler.md))`()` Close the Handler and free all associated resources. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](../java/util/logging/Handler.md))`()` Flush any buffered output. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](../java/util/logging/Handler.md))`()` Return the character encoding for this Handler. |
| --- | --- |
| open [ErrorManager](../java/util/logging/ErrorManager.md)! | [getErrorManager](../java/util/logging/Handler.md))`()` Retrieves the ErrorManager for this Handler. |
| open [Filter](../java/util/logging/Filter.md)! | [getFilter](../java/util/logging/Handler.md))`()` Get the current Filter for this Handler. |
| open [Formatter](../java/util/logging/Formatter.md)! | [getFormatter](../java/util/logging/Handler.md))`()` Return the Formatter for this Handler. |
| --- | --- |
| open [Level](../java/util/logging/Level.md)! | [getLevel](../java/util/logging/Handler.md))`()` Get the log level specifying which messages will be logged by this Handler. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoggable](../java/util/logging/Handler.md))`(`record:` ` [LogRecord](../java/util/logging/LogRecord.md)!`)` Check if this Handler would actually log a given LogRecord. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [publish](../java/util/logging/Handler.md))`(`record:` ` [LogRecord](../java/util/logging/LogRecord.md)!`)` Publish a LogRecord. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEncoding](../java/util/logging/Handler.md))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the character encoding used by this Handler. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorManager](../java/util/logging/Handler.md))`(`em:` ` [ErrorManager](../java/util/logging/ErrorManager.md)!`)` Define an ErrorManager for this Handler. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilter](../java/util/logging/Handler.md))`(`newFilter:` ` [Filter](../java/util/logging/Filter.md)!`)` Set a Filter to control output on this Handler. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormatter](../java/util/logging/Handler.md))`(`newFormatter:` ` [Formatter](../java/util/logging/Formatter.md)!`)` Set a Formatter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLevel](../java/util/logging/Handler.md))`(`newLevel:` ` [Level](../java/util/logging/Level.md)!`)` Set the log level specifying which message levels will be logged by this Handler. |

| Protected methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reportError](../java/util/logging/Handler.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ex:` ` [Exception](../java/lang/Exception.md)!`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Protected convenience method to report an error to this Handler's ErrorManager. |

## Protected constructors

### Handler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Handler()
```

Default constructor. The resulting Handler has a log level of Level.ALL, no Formatter, and no Filter. A default ErrorManager instance is installed as the ErrorManager.

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Close the Handler and free all associated resources.

The close method will perform a flush and then close the Handler. After close has been called this Handler should no longer be used. Method calls may either be silently ignored or may throw runtime exceptions.

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun flush(): Unit
```

Flush any buffered output. 

### getEncoding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEncoding(): String!
```

Return the character encoding for this Handler.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The encoding name. May be null, which indicates the default encoding should be used. |

### getErrorManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorManager(): ErrorManager!
```

Retrieves the ErrorManager for this Handler.

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------|
| [ErrorManager](../java/util/logging/ErrorManager.md)! | the ErrorManager for this Handler |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFilter(): Filter!
```

Get the current Filter for this Handler.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Filter](../java/util/logging/Filter.md)! | a Filter object (may be null) |

### getFormatter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFormatter(): Formatter!
```

Return the Formatter for this Handler.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------|
| [Formatter](../java/util/logging/Formatter.md)! | the Formatter (may be null). |

### getLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLevel(): Level!
```

Get the log level specifying which messages will be logged by this Handler. Message levels lower than this level will be discarded.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------|
| [Level](../java/util/logging/Level.md)! | the level of messages being logged. |

### isLoggable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLoggable(record: LogRecord!): Boolean
```

Check if this Handler would actually log a given LogRecord.

This method checks if the LogRecord has an appropriate Level and whether it satisfies any Filter. It also may make other Handler specific checks that might prevent a handler from logging the LogRecord. It will return false if the LogRecord is null.

<br />

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `record` | [LogRecord](../java/util/logging/LogRecord.md)!:a LogRecord |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the LogRecord would be logged. |

### publish

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun publish(record: LogRecord!): Unit
```

Publish a LogRecord.

The logging request was made initially to a Logger object, which initialized the LogRecord and forwarded it here.

The Handler is responsible for formatting the message, when and if necessary. The formatting should include localization.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `record` | [LogRecord](../java/util/logging/LogRecord.md)!:description of the log event. A null record is silently ignored and is not published |

### setEncoding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEncoding(encoding: String!): Unit
```

Set the character encoding used by this Handler.

The encoding should be set before any LogRecords are written to the Handler.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `encoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of a supported character encoding. May be null, to indicate the default platform encoding. |

| Exceptions ||
|----------------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |
| `java.io.UnsupportedEncodingException` | if the named encoding is not supported. |

### setErrorManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setErrorManager(em: ErrorManager!): Unit
```

Define an ErrorManager for this Handler.

The ErrorManager's "error" method will be invoked if any errors occur while using this Handler.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------|
| `em` | [ErrorManager](../java/util/logging/ErrorManager.md)!:the new ErrorManager |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |

### setFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFilter(newFilter: Filter!): Unit
```

Set a Filter to control output on this Handler.

For each call of publish the Handler will call this Filter (if it is non-null) to check if the LogRecord should be published or discarded.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------|
| `newFilter` | [Filter](../java/util/logging/Filter.md)!:a Filter object (may be null) |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |

### setFormatter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFormatter(newFormatter: Formatter!): Unit
```

Set a Formatter. This Formatter will be used to format LogRecords for this Handler.

Some Handlers may not use Formatters, in which case the Formatter will be remembered, but not used.

<br />

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `newFormatter` | [Formatter](../java/util/logging/Formatter.md)!:the Formatter to use (may not be null) |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |

### setLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLevel(newLevel: Level!): Unit
```

Set the log level specifying which message levels will be logged by this Handler. Message levels lower than this value will be discarded.

The intention is to allow developers to turn on voluminous logging, but to limit the messages that are sent to certain Handlers.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------|
| `newLevel` | [Level](../java/util/logging/Level.md)!:the new value for the log level |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |

## Protected methods

### reportError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun reportError(
    msg: String!, 
    ex: Exception!, 
    code: Int
): Unit
```

Protected convenience method to report an error to this Handler's ErrorManager. Note that this method retrieves and uses the ErrorManager without doing a security check. It can therefore be used in environments where the caller may be non-privileged.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a descriptive string (may be null) |
| `ex` | [Exception](../java/lang/Exception.md)!:an exception (may be null) |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an error code defined in ErrorManager |
| --- | --- |
