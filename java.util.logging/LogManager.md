# LogManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LogManager

```
open class LogManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.logging.LogManager](LogManager.md) |

There is a single global LogManager object that is used to maintain a set of shared state about Loggers and log services.

This LogManager object:

- Manages a hierarchical namespace of Logger objects. All named Loggers are stored in this namespace.
- Manages a set of logging control properties. These are simple key-value pairs that can be used by Handlers and other logging objects to configure themselves.

The global LogManager object can be retrieved using LogManager.getLogManager(). The LogManager object is created during class initialization and cannot subsequently be changed.

At startup the LogManager class is located using the java.util.logging.manager system property.

The LogManager defines two optional system properties that allow control over the initial configuration:

- "java.util.logging.config.class"
- "java.util.logging.config.file"

These two properties may be specified on the command line to the "java" command, or as system property definitions passed to JNI_CreateJavaVM.

If the "java.util.logging.config.class" property is set, then the property value is treated as a class name. The given class will be loaded, an object will be instantiated, and that object's constructor is responsible for reading in the initial configuration. (That object may use other system properties to control its configuration.) The alternate configuration class can use readConfiguration(InputStream) to define properties in the LogManager.

If "java.util.logging.config.class" property is**not**set, then the "java.util.logging.config.file" system property can be used to specify a properties file (in java.util.Properties format). The initial logging configuration will be read from this file.

If neither of these properties is defined then the LogManager uses its default configuration. The default configuration is typically loaded from the properties file "`lib/logging.properties`" in the Java installation directory.

The properties for loggers and Handlers will have names starting with the dot-separated name for the handler or logger.

The global logging properties may include:

- A property "handlers". This defines a whitespace or comma separated list of class names for handler classes to load and register as handlers on the root Logger (the Logger named ""). Each class name must be for a Handler class which has a default constructor. Note that these Handlers may be created lazily, when they are first used.
- A property "\<logger\>.handlers". This defines a whitespace or comma separated list of class names for handlers classes to load and register as handlers to the specified logger. Each class name must be for a Handler class which has a default constructor. Note that these Handlers may be created lazily, when they are first used.
- A property "\<logger\>.useParentHandlers". This defines a boolean value. By default every logger calls its parent in addition to handling the logging message itself, this often result in messages being handled by the root logger as well. When setting this property to false a Handler needs to be configured for this logger otherwise no logging messages are delivered.
- A property "config". This property is intended to allow arbitrary configuration code to be run. The property defines a whitespace or comma separated list of class names. A new instance will be created for each named class. The default constructor of each class may execute arbitrary code to update the logging configuration, such as setting logger levels, adding handlers, adding filters, etc.

Note that all classes loaded during LogManager configuration are first searched on the system class path before any user class path. That includes the LogManager class, any config classes, and any handler classes.

Loggers are organized into a naming hierarchy based on their dot separated names. Thus "a.b.c" is a child of "a.b", but "a.b1" and a.b2" are peers.

All properties whose names end with ".level" are assumed to define log levels for Loggers. Thus "foo.level" defines a log level for the logger called "foo" and (recursively) for any of its children in the naming hierarchy. Log Levels are applied in the order they are defined in the properties file. Thus level settings for child nodes in the tree should come after settings for their parents. The property name ".level" can be used to set the level for the root of the tree.

All methods on the LogManager object are multi-thread safe.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LOGGING_MXBEAN_NAME](LogManager.md) String representation of the`ObjectName`for the management interface for the logging facility. |

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------|---|
| [LogManager](LogManager.md))`()` Protected constructor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addLogger](LogManager.md))`(`logger:` ` [Logger](Logger.md)!`)` Add a named logger. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPropertyChangeListener](LogManager.md))`(`l:` ` [PropertyChangeListener](../java.beans/PropertyChangeListener.md)!`)` Adds an event listener to be invoked when the logging properties are re-read. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkAccess](LogManager.md))`()` Check that the current context is trusted to modify the logging configuration. |
| --- | --- |
| openstatic [LogManager](LogManager.md)! | [getLogManager](LogManager.md))`()` Returns the global LogManager object. |
| open [Logger](Logger.md)! | [getLogger](LogManager.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Method to find a named logger. |
| open [Enumeration](../java.util/Enumeration.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getLoggerNames](LogManager.md))`()` Get an enumeration of known logger names. |
| --- | --- |
| openstatic [LoggingMXBean](LoggingMXBean.md)! | [getLoggingMXBean](LogManager.md))`()` Returns LoggingMXBean for managing loggers. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getProperty](LogManager.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the value of a logging property. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readConfiguration](LogManager.md))`()` Reinitialize the logging properties and reread the logging configuration. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readConfiguration](LogManager.md))`(`ins:` ` [InputStream](../java.io/InputStream.md)!`)` Reinitialize the logging properties and reread the logging configuration from the given stream, which should be in java. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePropertyChangeListener](LogManager.md))`(`l:` ` [PropertyChangeListener](../java.beans/PropertyChangeListener.md)!`)` Removes an event listener for property change events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](LogManager.md))`()` Reset the logging configuration. |
| --- | --- |

## Constants

### LOGGING_MXBEAN_NAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOGGING_MXBEAN_NAME: String
```

String representation of the`ObjectName`for the management interface for the logging facility. 

 Value: "java.util.logging:type=Logging"

**See Also**

- [java.util.logging.LoggingMXBean](LoggingMXBean.md)

## Protected constructors

### LogManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected LogManager()
```

Protected constructor. This is protected so that container applications (such as J2EE containers) can subclass the object. It is non-public as it is intended that there only be one LogManager object, whose value is retrieved by calling LogManager.getLogManager.

## Public methods

### addLogger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addLogger(logger: Logger!): Boolean
```

Add a named logger. This does nothing and returns false if a logger with the same name is already registered.

The Logger factory methods call this method to register each newly created Logger.

The application should retain its own reference to the Logger object to avoid it being garbage collected. The LogManager may only retain a weak reference.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------|
| `logger` | [Logger](Logger.md)!:the new logger. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the argument logger was registered successfully, false if a logger of that name already exists. |

| Exceptions ||
|----------------------------------|-----------------------------|
| `java.lang.NullPointerException` | if the logger name is null. |

### addPropertyChangeListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addPropertyChangeListener(l: PropertyChangeListener!): Unit
```

**Deprecated:** *The dependency on`PropertyChangeListener`creates a significant impediment to future modularization of the Java platform. This method will be removed in a future release. The global`LogManager`can detect changes to the logging configuration by overridding the #readConfiguration method.*

Adds an event listener to be invoked when the logging properties are re-read. Adding multiple instances of the same event Listener results in multiple entries in the property event listener table.

**WARNING:** This method is omitted from this class in all subset Profiles of Java SE that do not include the`java.beans`package.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------|
| `l` | [PropertyChangeListener](../java.beans/PropertyChangeListener.md)!:event listener |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |
| `java.lang.NullPointerException` | if the PropertyChangeListener is null. |

### checkAccess

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkAccess(): Unit
```

Check that the current context is trusted to modify the logging configuration. This requires LoggingPermission("control").

If the check fails we throw a SecurityException, otherwise we return normally.

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |

### getLogManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLogManager(): LogManager!
```

Returns the global LogManager object.

| Return ||
|---------------------------------------------------------------------------------------------|------------------------------|
| [LogManager](LogManager.md)! | the global LogManager object |

### getLogger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLogger(name: String!): Logger!
```

Method to find a named logger.

Note that since untrusted code may create loggers with arbitrary names this method should not be relied on to find Loggers for security sensitive logging. It is also important to note that the Logger associated with the String`name`may be garbage collected at any time if there is no strong reference to the Logger. The caller of this method must check the return value for null in order to properly handle the case where the Logger has been garbage collected.

<br />

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:name of the logger |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Logger](Logger.md)! | matching logger or null if none is found |

### getLoggerNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLoggerNames(): Enumeration<String!>!
```

Get an enumeration of known logger names.

Note: Loggers may be added dynamically as new classes are loaded. This method only reports on the loggers that are currently registered. It is also important to note that this method only returns the name of a Logger, not a strong reference to the Logger itself. The returned String does nothing to prevent the Logger from being garbage collected. In particular, if the returned name is passed to`LogManager.getLogger()`, then the caller must check the return value from`LogManager.getLogger()`for null to properly handle the case where the Logger has been garbage collected in the time since its name was returned by this method.

<br />

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| [Enumeration](../java.util/Enumeration.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | enumeration of logger name strings |

### getLoggingMXBean

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLoggingMXBean(): LoggingMXBean!
```

Returns LoggingMXBean for managing loggers.

| Return ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [LoggingMXBean](LoggingMXBean.md)! | a [LoggingMXBean](LoggingMXBean.md) object. |

### getProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProperty(name: String!): String!
```

Get the value of a logging property. The method returns null if the property is not found.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:property name |

| Return ||
|-----------------------------------------------------------------------------------|----------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | property value |

### readConfiguration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readConfiguration(): Unit
```

Reinitialize the logging properties and reread the logging configuration.

The same rules are used for locating the configuration properties as are used at startup. So normally the logging properties will be re-read from the same file that was used at startup.

Any log level definitions in the new configuration file will be applied using Logger.setLevel(), if the target Logger exists.

A PropertyChangeEvent will be fired after the properties are read.

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |
| `java.io.IOException` | if there are IO problems reading the configuration. |

### readConfiguration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readConfiguration(ins: InputStream!): Unit
```

Reinitialize the logging properties and reread the logging configuration from the given stream, which should be in java.util.Properties format. A PropertyChangeEvent will be fired after the properties are read.

Any log level definitions in the new configuration file will be applied using Logger.setLevel(), if the target Logger exists.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------|
| `ins` | [InputStream](../java.io/InputStream.md)!:stream to read properties from |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |
| `java.io.IOException` | if there are problems reading from the stream. |

### removePropertyChangeListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removePropertyChangeListener(l: PropertyChangeListener!): Unit
```

**Deprecated:** *The dependency on`PropertyChangeListener`creates a significant impediment to future modularization of the Java platform. This method will be removed in a future release. The global`LogManager`can detect changes to the logging configuration by overridding the #readConfiguration method.*

Removes an event listener for property change events. If the same listener instance has been added to the listener table through multiple invocations of`addPropertyChangeListener`, then an equivalent number of`removePropertyChangeListener`invocations are required to remove all instances of that listener from the listener table.

Returns silently if the given listener is not found.

**WARNING:** This method is omitted from this class in all subset Profiles of Java SE that do not include the`java.beans`package.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------|
| `l` | [PropertyChangeListener](../java.beans/PropertyChangeListener.md)!:event listener (can be null) |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Reset the logging configuration.

For all named loggers, the reset operation removes and closes all Handlers and (except for the root logger) sets the level to null. The root logger's level is set to Level.INFO.

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |
