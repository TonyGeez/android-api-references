# Logger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Logger

```
open class Logger
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.logging.Logger](../java/util/logging/Logger.md) |

A Logger object is used to log messages for a specific system or application component. Loggers are normally named, using a hierarchical dot-separated namespace. Logger names can be arbitrary strings, but they should normally be based on the package name or class name of the logged component, such as java.net or javax.swing. In addition it is possible to create "anonymous" Loggers that are not stored in the Logger namespace.

Logger objects may be obtained by calls on one of the getLogger factory methods. These will either create a new Logger or return a suitable existing Logger. It is important to note that the Logger returned by one of the`getLogger`factory methods may be garbage collected at any time if a strong reference to the Logger is not kept.

Logging messages will be forwarded to registered Handler objects, which can forward the messages to a variety of destinations, including consoles, files, OS logs, etc.

Each Logger keeps track of a "parent" Logger, which is its nearest existing ancestor in the Logger namespace.

Each Logger has a "Level" associated with it. This reflects a minimum Level that this logger cares about. If a Logger's level is set to null, then its effective level is inherited from its parent, which may in turn obtain it recursively from its parent, and so on up the tree.

The log level can be configured based on the properties from the logging configuration file, as described in the description of the LogManager class. However it may also be dynamically changed by calls on the Logger.setLevel method. If a logger's level is changed the change may also affect child loggers, since any child logger that has null as its level will inherit its effective level from its parent.

On each logging call the Logger initially performs a cheap check of the request level (e.g., SEVERE or FINE) against the effective log level of the logger. If the request level is lower than the log level, the logging call returns immediately.

After passing this initial (cheap) test, the Logger will allocate a LogRecord to describe the logging message. It will then call a Filter (if present) to do a more detailed check on whether the record should be published. If that passes it will then publish the LogRecord to its output Handlers. By default, loggers also publish to their parent's Handlers, recursively up the tree.

Each Logger may have a`ResourceBundle`associated with it. The`ResourceBundle`may be specified by name, using the [getLogger(java.lang.String,java.lang.String)](../java/util/logging/Logger.md))factory method, or by value - using the [setResourceBundle](../java/util/logging/Logger.md))method. This bundle will be used for localizing logging messages. If a Logger does not have its own`ResourceBundle`or resource bundle name, then it will inherit the`ResourceBundle`or resource bundle name from its parent, recursively up the tree.

Most of the logger output methods take a "msg" argument. This msg argument may be either a raw value or a localization key. During formatting, if the logger has (or inherits) a localization`ResourceBundle`and if the`ResourceBundle`has a mapping for the msg string, then the msg string is replaced by the localized value. Otherwise the original msg string is used. Typically, formatters use java.text.MessageFormat style formatting to format parameters, so for example a format string "{0} {1}" would format two parameters as strings.

A set of methods alternatively take a "msgSupplier" instead of a "msg" argument. These methods take a [Supplier](../java/util/function/Supplier.md)`<String>`function which is invoked to construct the desired log message only when the message actually is to be logged based on the effective log level thus eliminating unnecessary message construction. For example, if the developer wants to log system health status for diagnosis, with the String-accepting version, the code would look like: 

```kotlin
<code>
 
  class DiagnosisMessages {
    static String systemHealthStatus() {
      // collect system health information
      ...
    }
  }
  ...
  logger.log(Level.FINER, DiagnosisMessages.systemHealthStatus());
 </code>
```
With the above code, the health status is collected unnecessarily even when the log level FINER is disabled. With the Supplier-accepting version as below, the status will only be collected when the log level FINER is enabled. 

```kotlin
<code>
 
  logger.log(Level.FINER, DiagnosisMessages::systemHealthStatus);
 </code>
```

When looking for a`ResourceBundle`, the logger will first look at whether a bundle was specified using [setResourceBundle](../java/util/logging/Logger.md)), and then only whether a resource bundle name was specified through the [getLogger](../java/util/logging/Logger.md))factory method. If no`ResourceBundle`or no resource bundle name is found, then it will use the nearest`ResourceBundle`or resource bundle name inherited from its parent tree. 
When a`ResourceBundle`was inherited or specified through the [setResourceBundle](../java/util/logging/Logger.md))method, then that`ResourceBundle`will be used. Otherwise if the logger only has or inherited a resource bundle name, then that resource bundle name will be mapped to a`ResourceBundle`object, using the default Locale at the time of logging. 
When mapping resource bundle names to`ResourceBundle`objects, the logger will first try to use the Thread's [context class](../java/lang/Thread.md))to map the given resource bundle name to a`ResourceBundle`. If the thread context class loader is`null`, it will try the [system class loader](../java/lang/ClassLoader.md))instead. If the`ResourceBundle`is still not found, it will use the class loader of the first caller of the [getLogger](../java/util/logging/Logger.md))factory method.

Formatting (including localization) is the responsibility of the output Handler, which will typically call a Formatter.

Note that formatting need not occur synchronously. It may be delayed until a LogRecord is actually written to an external sink.

The logging methods are grouped in five main categories:

- There are a set of "log" methods that take a log level, a message string, and optionally some parameters to the message string.
- There are a set of "logp" methods (for "log precise") that are like the "log" methods, but also take an explicit source class name and method name.
- There are a set of "logrb" method (for "log with resource bundle") that are like the "logp" method, but also take an explicit resource bundle object for use in localizing the log message.
- There are convenience methods for tracing method entries (the "entering" methods), method returns (the "exiting" methods) and throwing exceptions (the "throwing" methods).
- Finally, there are a set of convenience methods for use in the very simplest cases, when a developer simply wants to log a simple string at a given log level. These methods are named after the standard Level names ("severe", "warning", "info", etc.) and take a single argument, a message string.

For the methods that do not take an explicit source name and method name, the Logging framework will make a "best effort" to determine which class and method called into the logging method. However, it is important to realize that this automatically inferred information may only be approximate (or may even be quite wrong!). Virtual machines are allowed to do extensive optimizations when JITing and may entirely remove stack frames, making it impossible to reliably locate the calling class and method.

All methods on Logger are multi-thread safe.

**Subclassing Information:**Note that a LogManager class may provide its own implementation of named Loggers for any point in the namespace. Therefore, any subclasses of Logger (unless they are implemented in conjunction with a new LogManager class) should take care to obtain a Logger instance from the LogManager class and should delegate operations such as "isLoggable" and "log(LogRecord)" to that instance. Note that in order to intercept all logging output, subclasses need only override the log(LogRecord) method. All the other logging methods are implemented as calls on this log(LogRecord) method.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [GLOBAL_LOGGER_NAME](../java/util/logging/Logger.md) GLOBAL_LOGGER_NAME is a name for the global logger. |

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Logger](../java/util/logging/Logger.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `resourceBundleName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Protected method to construct a logger for a named subsystem. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addHandler](../java/util/logging/Logger.md))`(`handler:` ` [Handler](../java/util/logging/Handler.md)`)` Add a log Handler to receive logging messages. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [config](../java/util/logging/Logger.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Log a CONFIG message. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [config](../java/util/logging/Logger.md))`(`msgSupplier:` ` [Supplier](../java/util/function/Supplier.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Log a CONFIG message, which is only to be constructed if the logging level is such that the message will actually be logged. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [entering](../java/util/logging/Logger.md))`(`sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Log a method entry. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [entering](../java/util/logging/Logger.md))`(`sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `param1:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Log a method entry, with one parameter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [entering](../java/util/logging/Logger.md))`(`sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `params:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>?`)` Log a method entry, with an array of parameters. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [exiting](../java/util/logging/Logger.md))`(`sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Log a method return. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [exiting](../java/util/logging/Logger.md))`(`sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `result:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Log a method return, with result object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fine](../java/util/logging/Logger.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Log a FINE message. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fine](../java/util/logging/Logger.md))`(`msgSupplier:` ` [Supplier](../java/util/function/Supplier.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Log a FINE message, which is only to be constructed if the logging level is such that the message will actually be logged. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finer](../java/util/logging/Logger.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Log a FINER message. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finer](../java/util/logging/Logger.md))`(`msgSupplier:` ` [Supplier](../java/util/function/Supplier.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Log a FINER message, which is only to be constructed if the logging level is such that the message will actually be logged. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finest](../java/util/logging/Logger.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Log a FINEST message. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finest](../java/util/logging/Logger.md))`(`msgSupplier:` ` [Supplier](../java/util/function/Supplier.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Log a FINEST message, which is only to be constructed if the logging level is such that the message will actually be logged. |
| openstatic [Logger](../java/util/logging/Logger.md) | [getAnonymousLogger](../java/util/logging/Logger.md))`()` Create an anonymous Logger. |
| --- | --- |
| openstatic [Logger](../java/util/logging/Logger.md) | [getAnonymousLogger](../java/util/logging/Logger.md))`(`resourceBundleName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create an anonymous Logger. |
| open [Filter](../java/util/logging/Filter.md)? | [getFilter](../java/util/logging/Logger.md))`()` Get the current filter for this Logger. |
| static [Logger](../java/util/logging/Logger.md) | [getGlobal](../java/util/logging/Logger.md))`()` Return global logger object with the name Logger. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Handler](../java/util/logging/Handler.md)!\> | [getHandlers](../java/util/logging/Logger.md))`()` Get the Handlers associated with this logger. |
| open [Level](../java/util/logging/Level.md)? | [getLevel](../java/util/logging/Logger.md))`()` Get the log Level that has been specified for this Logger. |
| openstatic [Logger](../java/util/logging/Logger.md) | [getLogger](../java/util/logging/Logger.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Find or create a logger for a named subsystem. |
| --- | --- |
| openstatic [Logger](../java/util/logging/Logger.md) | [getLogger](../java/util/logging/Logger.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `resourceBundleName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Find or create a logger for a named subsystem. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getName](../java/util/logging/Logger.md))`()` Get the name for this logger. |
| open [Logger](../java/util/logging/Logger.md)? | [getParent](../java/util/logging/Logger.md))`()` Return the parent for this Logger. |
| --- | --- |
| open [ResourceBundle](../java/util/ResourceBundle.md)? | [getResourceBundle](../java/util/logging/Logger.md))`()` Retrieve the localization resource bundle for this logger. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getResourceBundleName](../java/util/logging/Logger.md))`()` Retrieve the localization resource bundle name for this logger. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getUseParentHandlers](../java/util/logging/Logger.md))`()` Discover whether or not this logger is sending its output to its parent logger. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [info](../java/util/logging/Logger.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Log an INFO message. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [info](../java/util/logging/Logger.md))`(`msgSupplier:` ` [Supplier](../java/util/function/Supplier.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Log a INFO message, which is only to be constructed if the logging level is such that the message will actually be logged. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoggable](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`)` Check if a message of the given level would actually be logged by this logger. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [log](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Log a message, with no arguments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [log](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `param1:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Log a message, with one object parameter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [log](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `params:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>?`)` Log a message, with an array of object arguments. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [log](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `thrown:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Log a message, with associated Throwable information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [log](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `thrown:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`, `msgSupplier:` ` [Supplier](../java/util/function/Supplier.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Log a lazily constructed message, with associated Throwable information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [log](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `msgSupplier:` ` [Supplier](../java/util/function/Supplier.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Log a message, which is only to be constructed if the logging level is such that the message will actually be logged. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [log](../java/util/logging/Logger.md))`(`record:` ` [LogRecord](../java/util/logging/LogRecord.md)`)` Log a LogRecord. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logp](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Log a message, specifying source class and method, with no arguments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logp](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `param1:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Log a message, specifying source class and method, with a single object parameter to the log message. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logp](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `params:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>?`)` Log a message, specifying source class and method, with an array of object arguments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logp](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `thrown:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Log a message, specifying source class and method, with associated Throwable information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logp](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `thrown:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`, `msgSupplier:` ` [Supplier](../java/util/function/Supplier.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Log a lazily constructed message, specifying source class and method, with associated Throwable information. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logp](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msgSupplier:` ` [Supplier](../java/util/function/Supplier.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Log a lazily constructed message, specifying source class and method, with no arguments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logrb](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `bundleName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Log a message, specifying source class, method, and resource bundle name with no arguments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logrb](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `bundleName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `param1:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Log a message, specifying source class, method, and resource bundle name, with a single object parameter to the log message. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logrb](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `bundleName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `params:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>?`)` Log a message, specifying source class, method, and resource bundle name, with an array of object arguments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logrb](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `bundleName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `thrown:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Log a message, specifying source class, method, and resource bundle name, with associated Throwable information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logrb](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `bundle:` ` [ResourceBundle](../java/util/ResourceBundle.md)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `vararg` `params:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Log a message, specifying source class, method, and resource bundle, with an optional list of message parameters. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logrb](../java/util/logging/Logger.md))`(`level:` ` [Level](../java/util/logging/Level.md)`, `sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `bundle:` ` [ResourceBundle](../java/util/ResourceBundle.md)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `thrown:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Log a message, specifying source class, method, and resource bundle, with associated Throwable information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeHandler](../java/util/logging/Logger.md))`(`handler:` ` [Handler](../java/util/logging/Handler.md)?`)` Remove a log Handler. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilter](../java/util/logging/Logger.md))`(`newFilter:` ` [Filter](../java/util/logging/Filter.md)?`)` Set a filter to control output on this Logger. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLevel](../java/util/logging/Logger.md))`(`newLevel:` ` [Level](../java/util/logging/Level.md)?`)` Set the log level specifying which message levels will be logged by this logger. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParent](../java/util/logging/Logger.md))`(`parent:` ` [Logger](../java/util/logging/Logger.md)`)` Set the parent for this Logger. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceBundle](../java/util/logging/Logger.md))`(`bundle:` ` [ResourceBundle](../java/util/ResourceBundle.md)`)` Sets a resource bundle on this logger. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUseParentHandlers](../java/util/logging/Logger.md))`(`useParentHandlers:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Specify whether or not this logger should send its output to its parent Logger. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [severe](../java/util/logging/Logger.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Log a SEVERE message. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [severe](../java/util/logging/Logger.md))`(`msgSupplier:` ` [Supplier](../java/util/function/Supplier.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Log a SEVERE message, which is only to be constructed if the logging level is such that the message will actually be logged. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [throwing](../java/util/logging/Logger.md))`(`sourceClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `sourceMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `thrown:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Log throwing an exception. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [warning](../java/util/logging/Logger.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Log a WARNING message. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [warning](../java/util/logging/Logger.md))`(`msgSupplier:` ` [Supplier](../java/util/function/Supplier.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Log a WARNING message, which is only to be constructed if the logging level is such that the message will actually be logged. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Logger](../java/util/logging/Logger.md) | [global](../java/util/logging/Logger.md) The "global" Logger object is provided as a convenience to developers who are making casual use of the Logging package. |

## Constants

### GLOBAL_LOGGER_NAME

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GLOBAL_LOGGER_NAME: String
```

GLOBAL_LOGGER_NAME is a name for the global logger. 

 Value: "global"

## Protected constructors

### Logger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Logger(
    name: String?, 
    resourceBundleName: String?)
```

Protected method to construct a logger for a named subsystem.

The logger will be initially configured with a null Level and with useParentHandlers set to true.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A name for the logger. This should be a dot-separated name and should normally be based on the package name or class name of the subsystem, such as java.net or javax.swing. It may be null for anonymous Loggers. |
| `resourceBundleName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of ResourceBundle to be used for localizing messages for this logger. May be null if none of the messages require localization. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------|
| `java.util.MissingResourceException` | if the resourceBundleName is non-null and no corresponding resource can be found. |

## Public methods

### addHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addHandler(handler: Handler): Unit
```

Add a log Handler to receive logging messages.

By default, Loggers also send their output to their parent logger. Typically the root Logger is configured with a set of Handlers that essentially act as default handlers for all loggers.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `handler` | [Handler](../java/util/logging/Handler.md):a logging Handler |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists, this logger is not anonymous, and the caller does not have LoggingPermission("control"). |

### config

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun config(msg: String?): Unit
```

Log a CONFIG message.

If the logger is currently enabled for the CONFIG message level then the given message is forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |

### config

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun config(msgSupplier: Supplier<String!>): Unit
```

Log a CONFIG message, which is only to be constructed if the logging level is such that the message will actually be logged.

If the logger is currently enabled for the CONFIG message level then the message is constructed by invoking the provided supplier function and forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msgSupplier` | [Supplier](../java/util/function/Supplier.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:A function, which when called, produces the desired log message |

### entering

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun entering(
    sourceClass: String?, 
    sourceMethod: String?
): Unit
```

Log a method entry.

This is a convenience method that can be used to log entry to a method. A LogRecord with message "ENTRY", log level FINER, and the given sourceMethod and sourceClass is logged.

<br />

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of method that is being entered |

### entering

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun entering(
    sourceClass: String?, 
    sourceMethod: String?, 
    param1: Any?
): Unit
```

Log a method entry, with one parameter.

This is a convenience method that can be used to log entry to a method. A LogRecord with message "ENTRY {0}", log level FINER, and the given sourceMethod, sourceClass, and parameter is logged.

<br />

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of method that is being entered |
| `param1` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:parameter to the method being entered |
| --- | --- |

### entering

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun entering(
    sourceClass: String?, 
    sourceMethod: String?, 
    params: Array<Any!>?
): Unit
```

Log a method entry, with an array of parameters.

This is a convenience method that can be used to log entry to a method. A LogRecord with message "ENTRY" (followed by a format {N} indicator for each entry in the parameter array), log level FINER, and the given sourceMethod, sourceClass, and parameters is logged.

<br />

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of method that is being entered |
| `params` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>?:array of parameters to the method being entered |
| --- | --- |

### exiting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exiting(
    sourceClass: String?, 
    sourceMethod: String?
): Unit
```

Log a method return.

This is a convenience method that can be used to log returning from a method. A LogRecord with message "RETURN", log level FINER, and the given sourceMethod and sourceClass is logged.

<br />

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of the method |

### exiting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exiting(
    sourceClass: String?, 
    sourceMethod: String?, 
    result: Any?
): Unit
```

Log a method return, with result object.

This is a convenience method that can be used to log returning from a method. A LogRecord with message "RETURN {0}", log level FINER, and the gives sourceMethod, sourceClass, and result object is logged.

<br />

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of the method |
| `result` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:Object that is being returned |
| --- | --- |

### fine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fine(msg: String?): Unit
```

Log a FINE message.

If the logger is currently enabled for the FINE message level then the given message is forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |

### fine

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fine(msgSupplier: Supplier<String!>): Unit
```

Log a FINE message, which is only to be constructed if the logging level is such that the message will actually be logged.

If the logger is currently enabled for the FINE message level then the message is constructed by invoking the provided supplier function and forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msgSupplier` | [Supplier](../java/util/function/Supplier.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:A function, which when called, produces the desired log message |

### finer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finer(msg: String?): Unit
```

Log a FINER message.

If the logger is currently enabled for the FINER message level then the given message is forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |

### finer

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finer(msgSupplier: Supplier<String!>): Unit
```

Log a FINER message, which is only to be constructed if the logging level is such that the message will actually be logged.

If the logger is currently enabled for the FINER message level then the message is constructed by invoking the provided supplier function and forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msgSupplier` | [Supplier](../java/util/function/Supplier.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:A function, which when called, produces the desired log message |

### finest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finest(msg: String?): Unit
```

Log a FINEST message.

If the logger is currently enabled for the FINEST message level then the given message is forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |

### finest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finest(msgSupplier: Supplier<String!>): Unit
```

Log a FINEST message, which is only to be constructed if the logging level is such that the message will actually be logged.

If the logger is currently enabled for the FINEST message level then the message is constructed by invoking the provided supplier function and forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msgSupplier` | [Supplier](../java/util/function/Supplier.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:A function, which when called, produces the desired log message |

### getAnonymousLogger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAnonymousLogger(): Logger
```

Create an anonymous Logger. The newly created Logger is not registered in the LogManager namespace. There will be no access checks on updates to the logger.

This factory method is primarily intended for use from applets. Because the resulting Logger is anonymous it can be kept private by the creating class. This removes the need for normal security checks, which in turn allows untrusted applet code to update the control state of the Logger. For example an applet can do a setLevel or an addHandler on an anonymous Logger.

Even although the new logger is anonymous, it is configured to have the root logger ("") as its parent. This means that by default it inherits its effective level and handlers from the root logger. Changing its parent via the [setParent](../java/util/logging/Logger.md))method will still require the security permission specified by that method.

<br />

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Logger](../java/util/logging/Logger.md) | a newly created private Logger |

### getAnonymousLogger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAnonymousLogger(resourceBundleName: String?): Logger
```

Create an anonymous Logger. The newly created Logger is not registered in the LogManager namespace. There will be no access checks on updates to the logger.

This factory method is primarily intended for use from applets. Because the resulting Logger is anonymous it can be kept private by the creating class. This removes the need for normal security checks, which in turn allows untrusted applet code to update the control state of the Logger. For example an applet can do a setLevel or an addHandler on an anonymous Logger.

Even although the new logger is anonymous, it is configured to have the root logger ("") as its parent. This means that by default it inherits its effective level and handlers from the root logger. Changing its parent via the [setParent](../java/util/logging/Logger.md))method will still require the security permission specified by that method.

<br />

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resourceBundleName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of ResourceBundle to be used for localizing messages for this logger. May be null if none of the messages require localization. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Logger](../java/util/logging/Logger.md) | a newly created private Logger |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------|
| `java.util.MissingResourceException` | if the resourceBundleName is non-null and no corresponding resource can be found. |

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFilter(): Filter?
```

Get the current filter for this Logger.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Filter](../java/util/logging/Filter.md)? | a filter object (may be null) |

### getGlobal

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getGlobal(): Logger
```

Return global logger object with the name Logger.GLOBAL_LOGGER_NAME.

| Return ||
|------------------------------------------------------------------------------------|----------------------|
| [Logger](../java/util/logging/Logger.md) | global logger object |

### getHandlers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHandlers(): Array<Handler!>
```

Get the Handlers associated with this logger.

<br />

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Handler](../java/util/logging/Handler.md)!> | an array of all registered Handlers |

### getLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLevel(): Level?
```

Get the log Level that has been specified for this Logger. The result may be null, which means that this logger's effective level will be inherited from its parent.

| Return ||
|----------------------------------------------------------------------------------|---------------------|
| [Level](../java/util/logging/Level.md)? | this Logger's level |

### getLogger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLogger(name: String): Logger
```

Find or create a logger for a named subsystem. If a logger has already been created with the given name it is returned. Otherwise a new logger is created.

If a new logger is created its log level will be configured based on the LogManager configuration and it will configured to also send logging output to its parent's Handlers. It will be registered in the LogManager global namespace.

Note: The LogManager may only retain a weak reference to the newly created Logger. It is important to understand that a previously created Logger with the given name may be garbage collected at any time if there is no strong reference to the Logger. In particular, this means that two back-to-back calls like`getLogger("MyLogger").log(...)`may use different Logger objects named "MyLogger" if there is no strong reference to the Logger named "MyLogger" elsewhere in the program.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):A name for the logger. This should be a dot-separated name and should normally be based on the package name or class name of the subsystem, such as java.net or javax.swing |

| Return ||
|------------------------------------------------------------------------------------|-------------------|
| [Logger](../java/util/logging/Logger.md) | a suitable Logger |

| Exceptions ||
|----------------------------------|----------------------|
| `java.lang.NullPointerException` | if the name is null. |

### getLogger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLogger(
    name: String, 
    resourceBundleName: String?
): Logger
```

Find or create a logger for a named subsystem. If a logger has already been created with the given name it is returned. Otherwise a new logger is created.

If a new logger is created its log level will be configured based on the LogManager and it will configured to also send logging output to its parent's Handlers. It will be registered in the LogManager global namespace.

Note: The LogManager may only retain a weak reference to the newly created Logger. It is important to understand that a previously created Logger with the given name may be garbage collected at any time if there is no strong reference to the Logger. In particular, this means that two back-to-back calls like`getLogger("MyLogger", ...).log(...)`may use different Logger objects named "MyLogger" if there is no strong reference to the Logger named "MyLogger" elsewhere in the program.

If the named Logger already exists and does not yet have a localization resource bundle then the given resource bundle name is used. If the named Logger already exists and has a different resource bundle name then an IllegalArgumentException is thrown.

<br />

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):A name for the logger. This should be a dot-separated name and should normally be based on the package name or class name of the subsystem, such as java.net or javax.swing |
| `resourceBundleName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of ResourceBundle to be used for localizing messages for this logger. May be`null`if none of the messages require localization. |

| Return ||
|------------------------------------------------------------------------------------|-------------------|
| [Logger](../java/util/logging/Logger.md) | a suitable Logger |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.MissingResourceException` | if the resourceBundleName is non-null and no corresponding resource can be found. |
| `java.lang.IllegalArgumentException` | if the Logger already exists and uses a different resource bundle name; or if`resourceBundleName`is`null`but the named logger has a resource bundle set. |
| `java.lang.NullPointerException` | if the name is null. |
| --- | --- |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String?
```

Get the name for this logger.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | logger name. Will be null for anonymous Loggers. |

### getParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParent(): Logger?
```

Return the parent for this Logger.

This method returns the nearest extant parent in the namespace. Thus if a Logger is called "a.b.c.d", and a Logger called "a.b" has been created but no logger "a.b.c" exists, then a call of getParent on the Logger "a.b.c.d" will return the Logger "a.b".

The result will be null if it is called on the root Logger in the namespace.

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------|
| [Logger](../java/util/logging/Logger.md)? | nearest existing parent Logger |

### getResourceBundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResourceBundle(): ResourceBundle?
```

Retrieve the localization resource bundle for this logger. This method will return a`ResourceBundle`that was either set by the [setResourceBundle](../java/util/logging/Logger.md))method or [mapped from the the resource bundle name](../java/util/logging/Logger.md) set via the [getLogger](../java/util/logging/Logger.md))factory method for the current default locale. 
Note that if the result is`null`, then the Logger will use a resource bundle or resource bundle name inherited from its parent.

| Return ||
|--------------------------------------------------------------------------------------------------|------------------------------------|
| [ResourceBundle](../java/util/ResourceBundle.md)? | localization bundle (may be`null`) |

### getResourceBundleName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResourceBundleName(): String?
```

Retrieve the localization resource bundle name for this logger. This is either the name specified through the [getLogger](../java/util/logging/Logger.md))factory method, or the [base name](../java/util/ResourceBundle.md))of the ResourceBundle set through [setResourceBundle](../java/util/logging/Logger.md))method. 
Note that if the result is`null`, then the Logger will use a resource bundle or resource bundle name inherited from its parent.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | localization bundle name (may be`null`) |

### getUseParentHandlers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUseParentHandlers(): Boolean
```

Discover whether or not this logger is sending its output to its parent logger.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if output is to be sent to the logger's parent |

### info

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun info(msg: String?): Unit
```

Log an INFO message.

If the logger is currently enabled for the INFO message level then the given message is forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |

### info

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun info(msgSupplier: Supplier<String!>): Unit
```

Log a INFO message, which is only to be constructed if the logging level is such that the message will actually be logged.

If the logger is currently enabled for the INFO message level then the message is constructed by invoking the provided supplier function and forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msgSupplier` | [Supplier](../java/util/function/Supplier.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:A function, which when called, produces the desired log message |

### isLoggable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLoggable(level: Level): Boolean
```

Check if a message of the given level would actually be logged by this logger. This check is based on the Loggers effective level, which may be inherited from its parent.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):a message logging level |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the given message level is currently being logged. |

### log

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun log(
    level: Level, 
    msg: String?
): Unit
```

Log a message, with no arguments.

If the logger is currently enabled for the given message level then the given message is forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |

### log

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun log(
    level: Level, 
    msg: String?, 
    param1: Any?
): Unit
```

Log a message, with one object parameter.

If the logger is currently enabled for the given message level then a corresponding LogRecord is created and forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |
| `param1` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:parameter to the message |
| --- | --- |

### log

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun log(
    level: Level, 
    msg: String?, 
    params: Array<Any!>?
): Unit
```

Log a message, with an array of object arguments.

If the logger is currently enabled for the given message level then a corresponding LogRecord is created and forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |
| `params` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>?:array of parameters to the message |
| --- | --- |

### log

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun log(
    level: Level, 
    msg: String?, 
    thrown: Throwable?
): Unit
```

Log a message, with associated Throwable information.

If the logger is currently enabled for the given message level then the given arguments are stored in a LogRecord which is forwarded to all registered output handlers.

Note that the thrown argument is stored in the LogRecord thrown property, rather than the LogRecord parameters property. Thus it is processed specially by output Formatters and is not treated as a formatting parameter to the LogRecord message property.

<br />

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |
| `thrown` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:Throwable associated with log message. |
| --- | --- |

### log

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun log(
    level: Level, 
    thrown: Throwable?, 
    msgSupplier: Supplier<String!>
): Unit
```

Log a lazily constructed message, with associated Throwable information.

If the logger is currently enabled for the given message level then the message is constructed by invoking the provided supplier function. The message and the given [Throwable](../java/lang/Throwable.md) are then stored in a [LogRecord](../java/util/logging/LogRecord.md) which is forwarded to all registered output handlers.

Note that the thrown argument is stored in the LogRecord thrown property, rather than the LogRecord parameters property. Thus it is processed specially by output Formatters and is not treated as a formatting parameter to the LogRecord message property.

<br />

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `thrown` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:Throwable associated with log message. |
| `msgSupplier` | [Supplier](../java/util/function/Supplier.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:A function, which when called, produces the desired log message |
| --- | --- |

### log

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun log(
    level: Level, 
    msgSupplier: Supplier<String!>
): Unit
```

Log a message, which is only to be constructed if the logging level is such that the message will actually be logged.

If the logger is currently enabled for the given message level then the message is constructed by invoking the provided supplier function and forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `msgSupplier` | [Supplier](../java/util/function/Supplier.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:A function, which when called, produces the desired log message |

### log

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun log(record: LogRecord): Unit
```

Log a LogRecord.

All the other logging methods in this class call through this method to actually perform any logging. Subclasses can override this single method to capture all log activity.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------|
| `record` | [LogRecord](../java/util/logging/LogRecord.md):the LogRecord to be published |

### logp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logp(
    level: Level, 
    sourceClass: String?, 
    sourceMethod: String?, 
    msg: String?
): Unit
```

Log a message, specifying source class and method, with no arguments.

If the logger is currently enabled for the given message level then the given message is forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of method that issued the logging request |
| --- | --- |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |

### logp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logp(
    level: Level, 
    sourceClass: String?, 
    sourceMethod: String?, 
    msg: String?, 
    param1: Any?
): Unit
```

Log a message, specifying source class and method, with a single object parameter to the log message.

If the logger is currently enabled for the given message level then a corresponding LogRecord is created and forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of method that issued the logging request |
| --- | --- |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |
| `param1` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:Parameter to the log message. |

### logp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logp(
    level: Level, 
    sourceClass: String?, 
    sourceMethod: String?, 
    msg: String?, 
    params: Array<Any!>?
): Unit
```

Log a message, specifying source class and method, with an array of object arguments.

If the logger is currently enabled for the given message level then a corresponding LogRecord is created and forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of method that issued the logging request |
| --- | --- |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |
| `params` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>?:Array of parameters to the message |

### logp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logp(
    level: Level, 
    sourceClass: String?, 
    sourceMethod: String?, 
    msg: String?, 
    thrown: Throwable?
): Unit
```

Log a message, specifying source class and method, with associated Throwable information.

If the logger is currently enabled for the given message level then the given arguments are stored in a LogRecord which is forwarded to all registered output handlers.

Note that the thrown argument is stored in the LogRecord thrown property, rather than the LogRecord parameters property. Thus it is processed specially by output Formatters and is not treated as a formatting parameter to the LogRecord message property.

<br />

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of method that issued the logging request |
| --- | --- |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |
| `thrown` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:Throwable associated with log message. |

### logp

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logp(
    level: Level, 
    sourceClass: String?, 
    sourceMethod: String?, 
    thrown: Throwable?, 
    msgSupplier: Supplier<String!>
): Unit
```

Log a lazily constructed message, specifying source class and method, with associated Throwable information.

If the logger is currently enabled for the given message level then the message is constructed by invoking the provided supplier function. The message and the given [Throwable](../java/lang/Throwable.md) are then stored in a [LogRecord](../java/util/logging/LogRecord.md) which is forwarded to all registered output handlers.

Note that the thrown argument is stored in the LogRecord thrown property, rather than the LogRecord parameters property. Thus it is processed specially by output Formatters and is not treated as a formatting parameter to the LogRecord message property.

<br />

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of method that issued the logging request |
| --- | --- |
| `thrown` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:Throwable associated with log message. |
| `msgSupplier` | [Supplier](../java/util/function/Supplier.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:A function, which when called, produces the desired log message |

### logp

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logp(
    level: Level, 
    sourceClass: String?, 
    sourceMethod: String?, 
    msgSupplier: Supplier<String!>
): Unit
```

Log a lazily constructed message, specifying source class and method, with no arguments.

If the logger is currently enabled for the given message level then the message is constructed by invoking the provided supplier function and forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of method that issued the logging request |
| --- | --- |
| `msgSupplier` | [Supplier](../java/util/function/Supplier.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:A function, which when called, produces the desired log message |

### logrb

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logrb(
    level: Level, 
    sourceClass: String?, 
    sourceMethod: String?, 
    bundleName: String?, 
    msg: String?
): Unit
```

**Deprecated:** *Use [logrb(java.util.logging.Level,java.lang.String,java.lang.String,java.util.ResourceBundle,java.lang.String,java.lang.Object...)](../java/util/logging/Logger.md))instead.*

Log a message, specifying source class, method, and resource bundle name with no arguments.

If the logger is currently enabled for the given message level then the given message is forwarded to all the registered output Handler objects.

The msg string is localized using the named resource bundle. If the resource bundle name is null, or an empty String or invalid then the msg string is not localized.

<br />

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of method that issued the logging request |
| --- | --- |
| `bundleName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of resource bundle to localize msg, can be null |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |

### logrb

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logrb(
    level: Level, 
    sourceClass: String?, 
    sourceMethod: String?, 
    bundleName: String?, 
    msg: String?, 
    param1: Any?
): Unit
```

**Deprecated:** *Use [logrb(java.util.logging.Level,java.lang.String,java.lang.String,java.util.ResourceBundle,java.lang.String,java.lang.Object...)](../java/util/logging/Logger.md))instead*

Log a message, specifying source class, method, and resource bundle name, with a single object parameter to the log message.

If the logger is currently enabled for the given message level then a corresponding LogRecord is created and forwarded to all the registered output Handler objects.

The msg string is localized using the named resource bundle. If the resource bundle name is null, or an empty String or invalid then the msg string is not localized.

<br />

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of method that issued the logging request |
| --- | --- |
| `bundleName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of resource bundle to localize msg, can be null |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |
| `param1` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:Parameter to the log message. |
| --- | --- |

### logrb

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logrb(
    level: Level, 
    sourceClass: String?, 
    sourceMethod: String?, 
    bundleName: String?, 
    msg: String?, 
    params: Array<Any!>?
): Unit
```

**Deprecated:** *Use [logrb(java.util.logging.Level,java.lang.String,java.lang.String,java.util.ResourceBundle,java.lang.String,java.lang.Object...)](../java/util/logging/Logger.md))instead.*

Log a message, specifying source class, method, and resource bundle name, with an array of object arguments.

If the logger is currently enabled for the given message level then a corresponding LogRecord is created and forwarded to all the registered output Handler objects.

The msg string is localized using the named resource bundle. If the resource bundle name is null, or an empty String or invalid then the msg string is not localized.

<br />

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of method that issued the logging request |
| --- | --- |
| `bundleName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of resource bundle to localize msg, can be null. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |
| `params` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>?:Array of parameters to the message |
| --- | --- |

### logrb

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logrb(
    level: Level, 
    sourceClass: String?, 
    sourceMethod: String?, 
    bundleName: String?, 
    msg: String?, 
    thrown: Throwable?
): Unit
```

**Deprecated:** *Use [logrb(java.util.logging.Level,java.lang.String,java.lang.String,java.util.ResourceBundle,java.lang.String,java.lang.Throwable)](../java/util/logging/Logger.md))instead.*

Log a message, specifying source class, method, and resource bundle name, with associated Throwable information.

If the logger is currently enabled for the given message level then the given arguments are stored in a LogRecord which is forwarded to all registered output handlers.

The msg string is localized using the named resource bundle. If the resource bundle name is null, or an empty String or invalid then the msg string is not localized.

Note that the thrown argument is stored in the LogRecord thrown property, rather than the LogRecord parameters property. Thus it is processed specially by output Formatters and is not treated as a formatting parameter to the LogRecord message property.

<br />

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of method that issued the logging request |
| --- | --- |
| `bundleName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of resource bundle to localize msg, can be null |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |
| `thrown` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:Throwable associated with log message. |
| --- | --- |

### logrb

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logrb(
    level: Level, 
    sourceClass: String?, 
    sourceMethod: String?, 
    bundle: ResourceBundle?, 
    msg: String?, 
    vararg params: Any!
): Unit
```

Log a message, specifying source class, method, and resource bundle, with an optional list of message parameters.

If the logger is currently enabled for the given message level then a corresponding LogRecord is created and forwarded to all the registered output Handler objects.

The`msg`string is localized using the given resource bundle. If the resource bundle is`null`, then the`msg`string is not localized.

<br />

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Name of the class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Name of the method that issued the logging request |
| --- | --- |
| `bundle` | [ResourceBundle](../java/util/ResourceBundle.md)?:Resource bundle to localize`msg`, can be`null`. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |
| `params` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Parameters to the message (optional, may be none). |
| --- | --- |

### logrb

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logrb(
    level: Level, 
    sourceClass: String?, 
    sourceMethod: String?, 
    bundle: ResourceBundle?, 
    msg: String?, 
    thrown: Throwable?
): Unit
```

Log a message, specifying source class, method, and resource bundle, with associated Throwable information.

If the logger is currently enabled for the given message level then the given arguments are stored in a LogRecord which is forwarded to all registered output handlers.

The`msg`string is localized using the given resource bundle. If the resource bundle is`null`, then the`msg`string is not localized.

Note that the thrown argument is stored in the LogRecord thrown property, rather than the LogRecord parameters property. Thus it is processed specially by output Formatters and is not treated as a formatting parameter to the LogRecord message property.

<br />

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Level](../java/util/logging/Level.md):One of the message level identifiers, e.g., SEVERE |
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Name of the class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Name of the method that issued the logging request |
| --- | --- |
| `bundle` | [ResourceBundle](../java/util/ResourceBundle.md)?:Resource bundle to localize`msg`, can be`null` |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |
| `thrown` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:Throwable associated with the log message. |
| --- | --- |

### removeHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeHandler(handler: Handler?): Unit
```

Remove a log Handler.

Returns silently if the given Handler is not found or is null

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------|
| `handler` | [Handler](../java/util/logging/Handler.md)?:a logging Handler |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists, this logger is not anonymous, and the caller does not have LoggingPermission("control"). |

### setFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFilter(newFilter: Filter?): Unit
```

Set a filter to control output on this Logger.

After passing the initial "level" check, the Logger will call this Filter to check if a log record should really be published.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------|
| `newFilter` | [Filter](../java/util/logging/Filter.md)?:a filter object (may be null) |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists, this logger is not anonymous, and the caller does not have LoggingPermission("control"). |

### setLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLevel(newLevel: Level?): Unit
```

Set the log level specifying which message levels will be logged by this logger. Message levels lower than this value will be discarded. The level value Level.OFF can be used to turn off logging.

If the new level is null, it means that this node should inherit its level from its nearest ancestor with a specific (non-null) level value.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------|
| `newLevel` | [Level](../java/util/logging/Level.md)?:the new value for the log level (may be null) |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists, this logger is not anonymous, and the caller does not have LoggingPermission("control"). |

### setParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParent(parent: Logger): Unit
```

Set the parent for this Logger. This method is used by the LogManager to update a Logger when the namespace changes.

It should not be called from application code.

<br />

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `parent` | [Logger](../java/util/logging/Logger.md):the new parent logger |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |

### setResourceBundle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setResourceBundle(bundle: ResourceBundle): Unit
```

Sets a resource bundle on this logger. All messages will be logged using the given resource bundle for its specific [locale](../java/util/ResourceBundle.md)).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `bundle` | [ResourceBundle](../java/util/ResourceBundle.md):The resource bundle that this logger shall use. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the given bundle is`null`. |
| `java.lang.IllegalArgumentException` | if the given bundle doesn't have a [base name](../java/util/ResourceBundle.md)), or if this logger already has a resource bundle set but the given bundle has a different base name. |
| `java.lang.SecurityException` | if a security manager exists, this logger is not anonymous, and the caller does not have LoggingPermission("control"). |
| --- | --- |

### setUseParentHandlers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setUseParentHandlers(useParentHandlers: Boolean): Unit
```

Specify whether or not this logger should send its output to its parent Logger. This means that any LogRecords will also be written to the parent's Handlers, and potentially to its parent, recursively up the namespace.

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `useParentHandlers` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if output is to be sent to the logger's parent. |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists, this logger is not anonymous, and the caller does not have LoggingPermission("control"). |

### severe

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun severe(msg: String?): Unit
```

Log a SEVERE message.

If the logger is currently enabled for the SEVERE message level then the given message is forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |

### severe

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun severe(msgSupplier: Supplier<String!>): Unit
```

Log a SEVERE message, which is only to be constructed if the logging level is such that the message will actually be logged.

If the logger is currently enabled for the SEVERE message level then the message is constructed by invoking the provided supplier function and forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msgSupplier` | [Supplier](../java/util/function/Supplier.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:A function, which when called, produces the desired log message |

### throwing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun throwing(
    sourceClass: String?, 
    sourceMethod: String?, 
    thrown: Throwable?
): Unit
```

Log throwing an exception.

This is a convenience method to log that a method is terminating by throwing an exception. The logging is done using the FINER level.

If the logger is currently enabled for the given message level then the given arguments are stored in a LogRecord which is forwarded to all registered output handlers. The LogRecord's message is set to "THROW".

Note that the thrown argument is stored in the LogRecord thrown property, rather than the LogRecord parameters property. Thus it is processed specially by output Formatters and is not treated as a formatting parameter to the LogRecord message property.

<br />

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `sourceClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of class that issued the logging request |
| `sourceMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of the method. |
| `thrown` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:The Throwable that is being thrown. |
| --- | --- |

### warning

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun warning(msg: String?): Unit
```

Log a WARNING message.

If the logger is currently enabled for the WARNING message level then the given message is forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string message (or a key in the message catalog) |

### warning

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun warning(msgSupplier: Supplier<String!>): Unit
```

Log a WARNING message, which is only to be constructed if the logging level is such that the message will actually be logged.

If the logger is currently enabled for the WARNING message level then the message is constructed by invoking the provided supplier function and forwarded to all the registered output Handler objects.

<br />

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msgSupplier` | [Supplier](../java/util/function/Supplier.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:A function, which when called, produces the desired log message |

## Properties

### global

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val global: Logger
```

**Deprecated:** *Initialization of this field is prone to deadlocks. The field must be initialized by the Logger class initialization which may cause deadlocks with the LogManager class initialization. In such cases two class initialization wait for each other to complete. The preferred way to get the global logger object is via the call`Logger.getGlobal()`. For compatibility with old JDK versions where the`Logger.getGlobal()`is not available use the call`Logger.getLogger(Logger.GLOBAL_LOGGER_NAME)`or`Logger.getLogger("global")`.*

The "global" Logger object is provided as a convenience to developers who are making casual use of the Logging package. Developers who are making serious use of the logging package (for example in products) should create and use their own Logger objects, with appropriate names, so that logging can be controlled on a suitable per-Logger granularity. Developers also need to keep a strong reference to their Logger objects to prevent them from being garbage collected.

<br />
