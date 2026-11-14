# FileHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileHandler

```
open class FileHandler : StreamHandler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.logging.Handler](Handler.md) |||
| | ↳ | [java.util.logging.StreamHandler](StreamHandler.md) ||
| | | ↳ | [java.util.logging.FileHandler](FileHandler.md) |
| --- | --- | --- | --- |

Simple file logging Handler.

The FileHandler can either write to a specified file, or it can write to a rotating set of files.

For a rotating set of files, as each file reaches a given size limit, it is closed, rotated out, and a new file opened. Successively older files are named by adding "0", "1", "2", etc. into the base filename.

By default buffering is enabled in the IO libraries but each log record is flushed out when it is complete.

By default the XMLFormatter class is used for formatting.

**Configuration:**By default each FileHandler is initialized using the following LogManager configuration properties where \<handler-name\> refers to the fully-qualified class name of the handler. If properties are not defined (or have invalid values) then the specified default values are used.

- \<handler-name\>.level specifies the default level for the Handler (defaults to Level.ALL).
- \<handler-name\>.filter specifies the name of a Filter class to use (defaults to no Filter).
- \<handler-name\>.formatter specifies the name of a Formatter class to use (defaults to java.util.logging.XMLFormatter)
- \<handler-name\>.encoding the name of the character set encoding to use (defaults to the default platform encoding).
- \<handler-name\>.limit specifies an approximate maximum amount to write (in bytes) to any one file. If this is zero, then there is no limit. (Defaults to no limit).
- \<handler-name\>.count specifies how many output files to cycle through (defaults to 1).
- \<handler-name\>.pattern specifies a pattern for generating the output file name. See below for details. (Defaults to "%h/java%u.log").
- \<handler-name\>.append specifies whether the FileHandler should append onto any existing files (defaults to false).

For example, the properties for`FileHandler`would be:

- java.util.logging.FileHandler.level=INFO
- java.util.logging.FileHandler.formatter=java.util.logging.SimpleFormatter

For a custom handler, e.g. com.foo.MyHandler, the properties would be:

- com.foo.MyHandler.level=INFO
- com.foo.MyHandler.formatter=java.util.logging.SimpleFormatter

A pattern consists of a string that includes the following special components that will be replaced at runtime:

- "/" the local pathname separator
- "%t" the system temporary directory
- "%h" the value of the "user.home" system property
- "%g" the generation number to distinguish rotated logs
- "%u" a unique number to resolve conflicts
- "%%" translates to a single percent sign "%"

If no "%g" field has been specified and the file count is greater than one, then the generation number will be added to the end of the generated filename, after a dot.

Thus for example a pattern of "%t/java%g.log" with a count of 2 would typically cause log files to be written on Solaris to /var/tmp/java0.log and /var/tmp/java1.log whereas on Windows 95 they would be typically written to C:\\TEMP\\java0.log and C:\\TEMP\\java1.log

Generation numbers follow the sequence 0, 1, 2, etc.

Normally the "%u" unique field is set to 0. However, if the FileHandler tries to open the filename and finds the file is currently in use by another process it will increment the unique number field and try again. This will be repeated until FileHandler finds a file name that is not currently in use. If there is a conflict and no "%u" field has been specified, it will be added at the end of the filename after a dot. (This will be after any automatically added generation number.)

Thus if three processes were all trying to log to fred%u.%g.txt then they might end up using fred0.0.txt, fred1.0.txt, fred2.0.txt as the first file in their rotating sequences.

Note that the use of unique ids to avoid conflicts is only guaranteed to work reliably when using a local disk file system.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileHandler](FileHandler.md))`()` Construct a default FileHandler. |
| [FileHandler](FileHandler.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Initialize a FileHandler to write to the given filename. |
| [FileHandler](FileHandler.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `append:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Initialize a FileHandler to write to the given filename, with optional append. |
| [FileHandler](FileHandler.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initialize a FileHandler to write to a set of files. |
| [FileHandler](FileHandler.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `append:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Initialize a FileHandler to write to a set of files with optional append. |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](FileHandler.md))`()` Close all the files. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [publish](FileHandler.md))`(`record:` ` [LogRecord](LogRecord.md)!`)` Format and publish a LogRecord. |

| Inherited functions ||
|---|---|
| From class [StreamHandler](StreamHandler.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](StreamHandler.md))`()` <br /> Flush any buffered messages. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoggable](StreamHandler.md))`(`record:` ` [LogRecord](LogRecord.md)!`)` <br /> Check if this Handler would actually log a given LogRecord. This method checks if the LogRecord has an appropriate level and whether it satisfies any Filter. It will also return false if no output stream has been assigned yet or the LogRecord is null. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEncoding](StreamHandler.md))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Set (or change) the character encoding used by this Handler. The encoding should be set before any LogRecords are written to the Handler. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutputStream](StreamHandler.md))`(`out:` ` [OutputStream](../java.io/OutputStream.md)!`)` <br /> Change the output stream. If there is a current output stream then the Formatter's tail string is written and the stream is flushed and closed. Then the output stream is replaced with the new output stream. <br /> | ||
| From class [Handler](Handler.md) |------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](Handler.md))`()` <br /> Return the character encoding for this Handler. <br /> | | [ErrorManager](ErrorManager.md)! | [getErrorManager](Handler.md))`()` <br /> Retrieves the ErrorManager for this Handler. <br /> | | [Filter](Filter.md)! | [getFilter](Handler.md))`()` <br /> Get the current Filter for this Handler. <br /> | | [Formatter](Formatter.md)! | [getFormatter](Handler.md))`()` <br /> Return the Formatter for this Handler. <br /> | | [Level](Level.md)! | [getLevel](Handler.md))`()` <br /> Get the log level specifying which messages will be logged by this Handler. Message levels lower than this level will be discarded. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reportError](Handler.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ex:` ` [Exception](../java.lang/Exception.md)!`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Protected convenience method to report an error to this Handler's ErrorManager. Note that this method retrieves and uses the ErrorManager without doing a security check. It can therefore be used in environments where the caller may be non-privileged. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorManager](Handler.md))`(`em:` ` [ErrorManager](ErrorManager.md)!`)` <br /> Define an ErrorManager for this Handler. The ErrorManager's "error" method will be invoked if any errors occur while using this Handler. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilter](Handler.md))`(`newFilter:` ` [Filter](Filter.md)!`)` <br /> Set a Filter to control output on this Handler. For each call of publish the Handler will call this Filter (if it is non-null) to check if the LogRecord should be published or discarded. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormatter](Handler.md))`(`newFormatter:` ` [Formatter](Formatter.md)!`)` <br /> Set a Formatter. This Formatter will be used to format LogRecords for this Handler. Some Handlers may not use Formatters, in which case the Formatter will be remembered, but not used. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLevel](Handler.md))`(`newLevel:` ` [Level](Level.md)!`)` <br /> Set the log level specifying which message levels will be logged by this Handler. Message levels lower than this value will be discarded. The intention is to allow developers to turn on voluminous logging, but to limit the messages that are sent to certain Handlers. <br /> | ||

## Public constructors

### FileHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileHandler()
```

Construct a default FileHandler. This will be configured entirely from LogManager properties (or their default values).

<br />

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------------------------|
| `java.io.IOException` | if there are IO problems opening the files. |
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control")). |
| `java.lang.NullPointerException` | if pattern property is an empty String. |
| --- | --- |

### FileHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileHandler(pattern: String!)
```

Initialize a FileHandler to write to the given filename.

The FileHandler is configured based on LogManager properties (or their default values) except that the given pattern argument is used as the filename pattern, the file limit is set to no limit, and the file count is set to one.

There is no limit on the amount of data that may be written, so use this with care.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the output file |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------|
| `java.io.IOException` | if there are IO problems opening the files. |
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |
| `java.lang.IllegalArgumentException` | if pattern is an empty string |
| --- | --- |

### FileHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileHandler(
    pattern: String!, 
    append: Boolean)
```

Initialize a FileHandler to write to the given filename, with optional append.

The FileHandler is configured based on LogManager properties (or their default values) except that the given pattern argument is used as the filename pattern, the file limit is set to no limit, the file count is set to one, and the append mode is set to the given append argument.

There is no limit on the amount of data that may be written, so use this with care.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the output file |
| `append` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):specifies append mode |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------|
| `java.io.IOException` | if there are IO problems opening the files. |
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |
| `java.lang.IllegalArgumentException` | if pattern is an empty string |
| --- | --- |

### FileHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileHandler(
    pattern: String!, 
    limit: Int, 
    count: Int)
```

Initialize a FileHandler to write to a set of files. When (approximately) the given limit has been written to one file, another file will be opened. The output will cycle through a set of count files.

The FileHandler is configured based on LogManager properties (or their default values) except that the given pattern argument is used as the filename pattern, the file limit is set to the limit argument, and the file count is set to the given count argument.

The count must be at least 1.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for naming the output file |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of bytes to write to any one file |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of files to use |
| --- | --- |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------|
| `java.io.IOException` | if there are IO problems opening the files. |
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |
| `java.lang.IllegalArgumentException` | if`limit < 0`, or`count < 1`. |
| --- | --- |
| `java.lang.IllegalArgumentException` | if pattern is an empty string |

### FileHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileHandler(
    pattern: String!, 
    limit: Int, 
    count: Int, 
    append: Boolean)
```

Initialize a FileHandler to write to a set of files with optional append. When (approximately) the given limit has been written to one file, another file will be opened. The output will cycle through a set of count files.

The FileHandler is configured based on LogManager properties (or their default values) except that the given pattern argument is used as the filename pattern, the file limit is set to the limit argument, and the file count is set to the given count argument, and the append mode is set to the given append argument.

The count must be at least 1.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for naming the output file |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of bytes to write to any one file |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of files to use |
| --- | --- |
| `append` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):specifies append mode |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------|
| `java.io.IOException` | if there are IO problems opening the files. |
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |
| `java.lang.IllegalArgumentException` | if`limit < 0`, or`count < 1`. |
| --- | --- |
| `java.lang.IllegalArgumentException` | if pattern is an empty string |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Close all the files.

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
