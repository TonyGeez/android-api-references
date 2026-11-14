Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConsoleHandler

```
open class ConsoleHandler : StreamHandler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.logging.Handler](https://developer.android.com/reference/kotlin/java/util/logging/Handler) |||
| | ↳ | [java.util.logging.StreamHandler](https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler) ||
| | | ↳ | [java.util.logging.ConsoleHandler](https://developer.android.com/reference/kotlin/java/util/logging/ConsoleHandler#) |
| --- | --- | --- | --- |

This Handler publishes log records to System.err. By default the SimpleFormatter is used to generate brief summaries.

**Configuration:** By default each ConsoleHandler is initialized using the following LogManager configuration properties where `<handler-name>` refers to the fully-qualified class name of the handler. If properties are not defined (or have invalid values) then the specified default values are used.

- \<handler-name\>.level specifies the default level for the Handler (defaults to Level.INFO).
- \<handler-name\>.filter specifies the name of a Filter class to use (defaults to no Filter).
- \<handler-name\>.formatter specifies the name of a Formatter class to use (defaults to java.util.logging.SimpleFormatter).
- \<handler-name\>.encoding the name of the character set encoding to use (defaults to the default platform encoding).

For example, the properties for `ConsoleHandler` would be:

- java.util.logging.ConsoleHandler.level=INFO
- java.util.logging.ConsoleHandler.formatter=java.util.logging.SimpleFormatter

For a custom handler, e.g. com.foo.MyHandler, the properties would be:

- com.foo.MyHandler.level=INFO
- com.foo.MyHandler.formatter=java.util.logging.SimpleFormatter

<br />

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/logging/ConsoleHandler#ConsoleHandler()()` Create a ConsoleHandler for System.err. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/logging/ConsoleHandler#close()()` Override StreamHandler.close to do a flush but not to close the output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/logging/ConsoleHandler#publish(java.util.logging.LogRecord)(record: https://developer.android.com/reference/kotlin/java/util/logging/LogRecord!)` Publish a LogRecord. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler#flush()()` Flush any buffered messages. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler#isLoggable(java.util.logging.LogRecord)(record: https://developer.android.com/reference/kotlin/java/util/logging/LogRecord!)` Check if this Handler would actually log a given LogRecord. This method checks if the LogRecord has an appropriate level and whether it satisfies any Filter. It will also return false if no output stream has been assigned yet or the LogRecord is null. <br /> <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler#setEncoding(kotlin.String)(encoding: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Set (or change) the character encoding used by this Handler. The encoding should be set before any LogRecords are written to the Handler. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler#setOutputStream(java.io.OutputStream)(out: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!)` Change the output stream. If there is a current output stream then the Formatter's tail string is written and the stream is flushed and closed. Then the output stream is replaced with the new output stream. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/logging/Handler` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/util/logging/Handler#getEncoding()()` Return the character encoding for this Handler. <br /> | | `https://developer.android.com/reference/kotlin/java/util/logging/ErrorManager!` | `https://developer.android.com/reference/kotlin/java/util/logging/Handler#getErrorManager()()` Retrieves the ErrorManager for this Handler. <br /> | | `https://developer.android.com/reference/kotlin/java/util/logging/Filter!` | `https://developer.android.com/reference/kotlin/java/util/logging/Handler#getFilter()()` Get the current Filter for this Handler. <br /> | | `https://developer.android.com/reference/kotlin/java/util/logging/Formatter!` | `https://developer.android.com/reference/kotlin/java/util/logging/Handler#getFormatter()()` Return the Formatter for this Handler. <br /> | | `https://developer.android.com/reference/kotlin/java/util/logging/Level!` | `https://developer.android.com/reference/kotlin/java/util/logging/Handler#getLevel()()` Get the log level specifying which messages will be logged by this Handler. Message levels lower than this level will be discarded. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/logging/Handler#reportError(kotlin.String,%20java.lang.Exception,%20kotlin.Int)(msg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, ex: https://developer.android.com/reference/kotlin/java/lang/Exception.html#!, code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Protected convenience method to report an error to this Handler's ErrorManager. Note that this method retrieves and uses the ErrorManager without doing a security check. It can therefore be used in environments where the caller may be non-privileged. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/logging/Handler#setErrorManager(java.util.logging.ErrorManager)(em: https://developer.android.com/reference/kotlin/java/util/logging/ErrorManager!)` Define an ErrorManager for this Handler. The ErrorManager's "error" method will be invoked if any errors occur while using this Handler. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/logging/Handler#setFilter(java.util.logging.Filter)(newFilter: https://developer.android.com/reference/kotlin/java/util/logging/Filter!)` Set a Filter to control output on this Handler. For each call of publish the Handler will call this Filter (if it is non-null) to check if the LogRecord should be published or discarded. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/logging/Handler#setFormatter(java.util.logging.Formatter)(newFormatter: https://developer.android.com/reference/kotlin/java/util/logging/Formatter!)` Set a Formatter. This Formatter will be used to format LogRecords for this Handler. Some Handlers may not use Formatters, in which case the Formatter will be remembered, but not used. <br /> <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/logging/Handler#setLevel(java.util.logging.Level)(newLevel: https://developer.android.com/reference/kotlin/java/util/logging/Level!)` Set the log level specifying which message levels will be logged by this Handler. Message levels lower than this value will be discarded. The intention is to allow developers to turn on voluminous logging, but to limit the messages that are sent to certain Handlers. <br /> | ||

## Public constructors

### ConsoleHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ConsoleHandler()
```

Create a ConsoleHandler for System.err.

The ConsoleHandler is configured based on LogManager properties (or their default values).

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Override StreamHandler.close to do a flush but not to close the output stream. That is, we do **not** close System.err.

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |

### publish

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun publish(record: LogRecord!): Unit
```

Publish a LogRecord.

The logging request was made initially to a Logger object, which initialized the LogRecord and forwarded it here.

<br />

| Parameters ||
|---|---|
| `record` | [LogRecord](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord)!: description of the log event. A null record is silently ignored and is not published |
