# MemoryHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MemoryHandler

```
open class MemoryHandler : Handler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.logging.Handler](Handler.md) ||
| | ↳ | [java.util.logging.MemoryHandler](MemoryHandler.md) |

Handler that buffers requests in a circular buffer in memory.

Normally this Handler simply stores incoming LogRecords into its memory buffer and discards earlier records. This buffering is very cheap and avoids formatting costs. On certain trigger conditions, the MemoryHandler will push out its current buffer contents to a target Handler, which will typically publish them to the outside world.

There are three main models for triggering a push of the buffer:

- An incoming LogRecord has a type that is greater than a pre-defined level, the pushLevel.
- An external class calls the push method explicitly.
- A subclass overrides the log method and scans each incoming LogRecord and calls push if a record matches some desired criteria.

**Configuration:**By default each MemoryHandler is initialized using the following LogManager configuration properties where \<handler-name\> refers to the fully-qualified class name of the handler. If properties are not defined (or have invalid values) then the specified default values are used. If no default value is defined then a RuntimeException is thrown.

- \<handler-name\>.level specifies the level for the Handler (defaults to Level.ALL).
- \<handler-name\>.filter specifies the name of a Filter class to use (defaults to no Filter).
- \<handler-name\>.size defines the buffer size (defaults to 1000).
- \<handler-name\>.push defines the pushLevel (defaults to level.SEVERE).
- \<handler-name\>.target specifies the name of the target Handler class. (no default).

For example, the properties for`MemoryHandler`would be:

- java.util.logging.MemoryHandler.level=INFO
- java.util.logging.MemoryHandler.formatter=java.util.logging.SimpleFormatter

For a custom handler, e.g. com.foo.MyHandler, the properties would be:

- com.foo.MyHandler.level=INFO
- com.foo.MyHandler.formatter=java.util.logging.SimpleFormatter

<br />

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MemoryHandler](MemoryHandler.md))`()` Create a MemoryHandler and configure it based on LogManager configuration properties. |
| [MemoryHandler](MemoryHandler.md))`(`target:` ` [Handler](Handler.md)!`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pushLevel:` ` [Level](Level.md)!`)` Create a MemoryHandler. |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](MemoryHandler.md))`()` Close the Handler and free all associated resources. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](MemoryHandler.md))`()` Causes a flush on the target Handler. |
| open [Level](Level.md)! | [getPushLevel](MemoryHandler.md))`()` Get the pushLevel. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoggable](MemoryHandler.md))`(`record:` ` [LogRecord](LogRecord.md)!`)` Check if this Handler would actually log a given LogRecord into its internal buffer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [publish](MemoryHandler.md))`(`record:` ` [LogRecord](LogRecord.md)!`)` Store a LogRecord in an internal buffer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [push](MemoryHandler.md))`()` Push any buffered output to the target Handler. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPushLevel](MemoryHandler.md))`(`newLevel:` ` [Level](Level.md)!`)` Set the pushLevel. |

| Inherited functions ||
|---|---|
| From class [Handler](Handler.md) |------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](Handler.md))`()` <br /> Return the character encoding for this Handler. <br /> | | [ErrorManager](ErrorManager.md)! | [getErrorManager](Handler.md))`()` <br /> Retrieves the ErrorManager for this Handler. <br /> | | [Filter](Filter.md)! | [getFilter](Handler.md))`()` <br /> Get the current Filter for this Handler. <br /> | | [Formatter](Formatter.md)! | [getFormatter](Handler.md))`()` <br /> Return the Formatter for this Handler. <br /> | | [Level](Level.md)! | [getLevel](Handler.md))`()` <br /> Get the log level specifying which messages will be logged by this Handler. Message levels lower than this level will be discarded. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reportError](Handler.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ex:` ` [Exception](../java.lang/Exception.md)!`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Protected convenience method to report an error to this Handler's ErrorManager. Note that this method retrieves and uses the ErrorManager without doing a security check. It can therefore be used in environments where the caller may be non-privileged. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEncoding](Handler.md))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Set the character encoding used by this Handler. The encoding should be set before any LogRecords are written to the Handler. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorManager](Handler.md))`(`em:` ` [ErrorManager](ErrorManager.md)!`)` <br /> Define an ErrorManager for this Handler. The ErrorManager's "error" method will be invoked if any errors occur while using this Handler. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilter](Handler.md))`(`newFilter:` ` [Filter](Filter.md)!`)` <br /> Set a Filter to control output on this Handler. For each call of publish the Handler will call this Filter (if it is non-null) to check if the LogRecord should be published or discarded. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormatter](Handler.md))`(`newFormatter:` ` [Formatter](Formatter.md)!`)` <br /> Set a Formatter. This Formatter will be used to format LogRecords for this Handler. Some Handlers may not use Formatters, in which case the Formatter will be remembered, but not used. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLevel](Handler.md))`(`newLevel:` ` [Level](Level.md)!`)` <br /> Set the log level specifying which message levels will be logged by this Handler. Message levels lower than this value will be discarded. The intention is to allow developers to turn on voluminous logging, but to limit the messages that are sent to certain Handlers. <br /> | ||

## Public constructors

### MemoryHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MemoryHandler()
```

Create a MemoryHandler and configure it based on LogManager configuration properties. 

### MemoryHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MemoryHandler(
    target: Handler!, 
    size: Int, 
    pushLevel: Level!)
```

Create a MemoryHandler.

The MemoryHandler is configured based on LogManager properties (or their default values) except that the given pushLevel argument and buffer size argument are used.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Handler](Handler.md)!:the Handler to which to publish output. |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of log records to buffer (must be greater than zero) |
| `pushLevel` | [Level](Level.md)!:message level to push on |
| --- | --- |

| Exceptions ||
|--------------------------------------|------------------|
| `java.lang.IllegalArgumentException` | if`size is <= 0` |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Close the Handler and free all associated resources. This will also close the target Handler.

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Causes a flush on the target Handler.

Note that the current contents of the MemoryHandler buffer are**not**written out. That requires a "push". 

### getPushLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPushLevel(): Level!
```

Get the pushLevel.

| Return ||
|----------------------------------------------------------------------------------|----------------------------|
| [Level](Level.md)! | the value of the pushLevel |

### isLoggable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLoggable(record: LogRecord!): Boolean
```

Check if this Handler would actually log a given LogRecord into its internal buffer.

This method checks if the LogRecord has an appropriate level and whether it satisfies any Filter. However it does**not**check whether the LogRecord would result in a "push" of the buffer contents. It will return false if the LogRecord is null.

<br />

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `record` | [LogRecord](LogRecord.md)!:a LogRecord |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the LogRecord would be logged. |

### publish

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun publish(record: LogRecord!): Unit
```

Store a LogRecord in an internal buffer.

If there is a Filter, its isLoggable method is called to check if the given log record is loggable. If not we return. Otherwise the given record is copied into an internal circular buffer. Then the record's level property is compared with the pushLevel. If the given level is greater than or equal to the pushLevel then push is called to write all buffered records to the target output Handler.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `record` | [LogRecord](LogRecord.md)!:description of the log event. A null record is silently ignored and is not published |

### push

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun push(): Unit
```

Push any buffered output to the target Handler.

The buffer is then cleared. 

### setPushLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPushLevel(newLevel: Level!): Unit
```

Set the pushLevel. After a LogRecord is copied into our internal buffer, if its level is greater than or equal to the pushLevel, then push will be called.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------|
| `newLevel` | [Level](Level.md)!:the new value of the pushLevel |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |
