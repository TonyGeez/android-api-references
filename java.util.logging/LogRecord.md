# LogRecord

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LogRecord

```
open class LogRecord : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.logging.LogRecord](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#) |

LogRecord objects are used to pass logging requests between the logging framework and individual log Handlers.

When a LogRecord is passed into the logging framework it logically belongs to the framework and should no longer be used or updated by the client application.

Note that if the client application has not specified an explicit source method name and source class name, then the LogRecord class will infer them automatically when they are first accessed (due to a call on getSourceMethodName or getSourceClassName) by analyzing the call stack. Therefore, if a logging Handler wants to pass off a LogRecord to another thread, or to transmit it over RMI, and if it wishes to subsequently obtain method name or class name information it should call one of getSourceClassName or getSourceMethodName to force the values to be filled in.

**Serialization notes:**

- The LogRecord class is serializable.
- Because objects in the parameters array may not be serializable, during serialization all objects in the parameters array are written as the corresponding Strings (using Object.toString).
- The ResourceBundle is not transmitted as part of the serialized form, but the resource bundle name is, and the recipient object's readObject method will attempt to locate a suitable resource bundle.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LogRecord](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#LogRecord(java.util.logging.Level,%20kotlin.String))`(`level:` ` [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level)!`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct a LogRecord with the given level and message values. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level)! | [getLevel](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#getLevel())`()` Get the logging message level, for example Level. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLoggerName](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#getLoggerName())`()` Get the source Logger's name. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMessage](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#getMessage())`()` Get the "raw" log message, before localization or formatting. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMillis](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#getMillis())`()` Get event time in milliseconds since 1970. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [getParameters](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#getParameters())`()` Get the parameters to the log message. |
| open [ResourceBundle](https://developer.android.com/reference/kotlin/java/util/ResourceBundle.html#)! | [getResourceBundle](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#getResourceBundle())`()` Get the localization resource bundle |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResourceBundleName](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#getResourceBundleName())`()` Get the localization resource bundle name |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSequenceNumber](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#getSequenceNumber())`()` Get the sequence number. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSourceClassName](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#getSourceClassName())`()` Get the name of the class that (allegedly) issued the logging request. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSourceMethodName](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#getSourceMethodName())`()` Get the name of the method that (allegedly) issued the logging request. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getThreadID](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#getThreadID())`()` Get an identifier for the thread where the message originated. |
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [getThrown](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#getThrown())`()` Get any throwable associated with the log record. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLevel](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#setLevel(java.util.logging.Level))`(`level:` ` [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level)!`)` Set the logging message level, for example Level. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLoggerName](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#setLoggerName(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the source Logger's name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMessage](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#setMessage(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the "raw" log message, before localization or formatting. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMillis](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#setMillis(kotlin.Long))`(`millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Set event time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParameters](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#setParameters(kotlin.Array))`(`parameters:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Set the parameters to the log message. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceBundle](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#setResourceBundle(java.util.ResourceBundle))`(`bundle:` ` [ResourceBundle](https://developer.android.com/reference/kotlin/java/util/ResourceBundle.html#)!`)` Set the localization resource bundle. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceBundleName](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#setResourceBundleName(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the localization resource bundle name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSequenceNumber](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#setSequenceNumber(kotlin.Long))`(`seq:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Set the sequence number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSourceClassName](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#setSourceClassName(kotlin.String))`(`sourceClassName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the name of the class that (allegedly) issued the logging request. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSourceMethodName](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#setSourceMethodName(kotlin.String))`(`sourceMethodName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the name of the method that (allegedly) issued the logging request. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setThreadID](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#setThreadID(kotlin.Int))`(`threadID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set an identifier for the thread where the message originated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setThrown](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord#setThrown(kotlin.Throwable))`(`thrown:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Set a throwable associated with the log event. |

## Public constructors

### LogRecord

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LogRecord(
    level: Level!, 
    msg: String!)
```

Construct a LogRecord with the given level and message values.

The sequence property will be initialized with a new unique value. These sequence values are allocated in increasing order within a VM.

The millis property will be initialized to the current time.

The thread ID property will be initialized with a unique ID for the current thread.

All other properties will be initialized to "null".

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level)!:a logging level value |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the raw non-localized logging message (may be null) |

## Public methods

### getLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLevel(): Level!
```

Get the logging message level, for example Level.SEVERE.

| Return ||
|----------------------------------------------------------------------------------|---------------------------|
| [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level)! | the logging message level |

### getLoggerName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLoggerName(): String!
```

Get the source Logger's name.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | source logger name (may be null) |

### getMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMessage(): String!
```

Get the "raw" log message, before localization or formatting.

May be null, which is equivalent to the empty string "".

This message may be either the final text or a localization key.

During formatting, if the source logger has a localization ResourceBundle and if that ResourceBundle has an entry for this message string, then the message string is replaced with the localized value.

| Return ||
|-----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the raw message string |

### getMillis

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMillis(): Long
```

Get event time in milliseconds since 1970.

| Return ||
|------------------------------------------------------------------------------|---------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | event time in millis since 1970 |

### getParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParameters(): Array<Any!>!
```

Get the parameters to the log message.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | the log message parameters. May be null if there are no parameters. |

### getResourceBundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResourceBundle(): ResourceBundle!
```

Get the localization resource bundle

This is the ResourceBundle that should be used to localize the message string before formatting it. The result may be null if the message is not localizable, or if no suitable ResourceBundle is available.

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------|
| [ResourceBundle](https://developer.android.com/reference/kotlin/java/util/ResourceBundle.html#)! | the localization resource bundle |

### getResourceBundleName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResourceBundleName(): String!
```

Get the localization resource bundle name

This is the name for the ResourceBundle that should be used to localize the message string before formatting it. The result may be null if the message is not localizable.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localization resource bundle name |

### getSequenceNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSequenceNumber(): Long
```

Get the sequence number.

Sequence numbers are normally assigned in the LogRecord constructor, which assigns unique sequence numbers to each new LogRecord in increasing order.

| Return ||
|------------------------------------------------------------------------------|---------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the sequence number |

### getSourceClassName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSourceClassName(): String!
```

Get the name of the class that (allegedly) issued the logging request.

Note that this sourceClassName is not verified and may be spoofed. This information may either have been provided as part of the logging call, or it may have been inferred automatically by the logging framework. In the latter case, the information may only be approximate and may in fact describe an earlier call on the stack frame.

May be null if no information could be obtained.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the source class name |

### getSourceMethodName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSourceMethodName(): String!
```

Get the name of the method that (allegedly) issued the logging request.

Note that this sourceMethodName is not verified and may be spoofed. This information may either have been provided as part of the logging call, or it may have been inferred automatically by the logging framework. In the latter case, the information may only be approximate and may in fact describe an earlier call on the stack frame.

May be null if no information could be obtained.

| Return ||
|-----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the source method name |

### getThreadID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getThreadID(): Int
```

Get an identifier for the thread where the message originated.

This is a thread identifier within the Java VM and may or may not map to any operating system ID.

| Return ||
|----------------------------------------------------------------------------|-----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | thread ID |

### getThrown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getThrown(): Throwable!
```

Get any throwable associated with the log record.

If the event involved an exception, this will be the exception object. Otherwise null.

| Return ||
|-----------------------------------------------------------------------------------------|-------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | a throwable |

### setLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLevel(level: Level!): Unit
```

Set the logging message level, for example Level.SEVERE.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `level` | [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level)!:the logging message level |

### setLoggerName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLoggerName(name: String!): Unit
```

Set the source Logger's name.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the source logger name (may be null) |

### setMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMessage(message: String!): Unit
```

Set the "raw" log message, before localization or formatting.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the raw message string (may be null) |

### setMillis

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMillis(millis: Long): Unit
```

Set event time.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):event time in millis since 1970 |

### setParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParameters(parameters: Array<Any!>!): Unit
```

Set the parameters to the log message.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:the log message parameters. (may be null) |

### setResourceBundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setResourceBundle(bundle: ResourceBundle!): Unit
```

Set the localization resource bundle.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `bundle` | [ResourceBundle](https://developer.android.com/reference/kotlin/java/util/ResourceBundle.html#)!:localization bundle (may be null) |

### setResourceBundleName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setResourceBundleName(name: String!): Unit
```

Set the localization resource bundle name.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:localization bundle name (may be null) |

### setSequenceNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSequenceNumber(seq: Long): Unit
```

Set the sequence number.

Sequence numbers are normally assigned in the LogRecord constructor, so it should not normally be necessary to use this method.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------|
| `seq` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the sequence number |

### setSourceClassName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSourceClassName(sourceClassName: String!): Unit
```

Set the name of the class that (allegedly) issued the logging request.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------|
| `sourceClassName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the source class name (may be null) |

### setSourceMethodName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSourceMethodName(sourceMethodName: String!): Unit
```

Set the name of the method that (allegedly) issued the logging request.

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------|
| `sourceMethodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the source method name (may be null) |

### setThreadID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setThreadID(threadID: Int): Unit
```

Set an identifier for the thread where the message originated.

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `threadID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the thread ID |

### setThrown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setThrown(thrown: Throwable!): Unit
```

Set a throwable associated with the log event.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `thrown` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:a throwable (may be null) |
