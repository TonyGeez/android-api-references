# LoggingMXBean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LoggingMXBean

```
interface LoggingMXBean
```

| [java.util.logging.LoggingMXBean](../java/util/logging/LoggingMXBean.md) |

The management interface for the logging facility.

There is a single global instance of the LoggingMXBean. The`javax.management.ObjectName ObjectName`that uniquely identifies the management interface for logging within the`MBeanServer`is: 

```kotlin
<code><a docref="java.util.logging.LogManager$LOGGING_MXBEAN_NAME">java.util.logging:type=Logging</a></code>
```

<br />

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLoggerLevel](../java/util/logging/LoggingMXBean.md))`(`loggerName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the name of the log level associated with the specified logger. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getLoggerNames](../java/util/logging/LoggingMXBean.md))`()` Returns the list of currently registered logger names. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getParentLoggerName](../java/util/logging/LoggingMXBean.md))`(`loggerName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the name of the parent for the specified logger. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLoggerLevel](../java/util/logging/LoggingMXBean.md))`(`loggerName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `levelName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the specified logger to the specified new level. |

## Public methods

### getLoggerLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLoggerLevel(loggerName: String!): String!
```

Gets the name of the log level associated with the specified logger. If the specified logger does not exist, null is returned. This method first finds the logger of the given name and then returns the name of the log level by calling: [Logger.getLevel()](../java/util/logging/Logger.md)). [getName()](../java/util/logging/Level.md));

If the Level of the specified logger is null, which means that this logger's effective level is inherited from its parent, an empty string will be returned.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| `loggerName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the Logger to be retrieved. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The name of the log level of the specified logger; or an empty string if the log level of the specified logger is null. If the specified logger does not exist, null is returned. |

**See Also**

- [java.util.logging.Logger#getLevel](../java/util/logging/Logger.md)) 

### getLoggerNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLoggerNames(): MutableList<String!>!
```

Returns the list of currently registered logger names. This method calls [LogManager.getLoggerNames](../java/util/logging/LogManager.md))and returns a list of the logger names.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | A list of String each of which is a currently registered Logger name. |

### getParentLoggerName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParentLoggerName(loggerName: String!): String!
```

Returns the name of the parent for the specified logger. If the specified logger does not exist, null is returned. If the specified logger is the root Logger in the namespace, the result will be an empty string.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------|
| `loggerName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of a Logger. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the nearest existing parent logger; an empty string if the specified logger is the root logger. If the specified logger does not exist, null is returned. |

### setLoggerLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setLoggerLevel(
    loggerName: String!, 
    levelName: String!
): Unit
```

Sets the specified logger to the specified new level. If the levelName is not null, the level of the specified logger is set to the parsed Level matching the levelName. If the levelName is null, the level of the specified logger is set to null and the effective level of the logger is inherited from its nearest ancestor with a specific (non-null) level value.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `loggerName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the Logger to be set. Must be non-null. |
| `levelName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the level to set on the specified logger, or null if setting the level to inherit from its nearest ancestor. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified logger does not exist, or levelName is not a valid level name. |
| `java.lang.SecurityException` | if a security manager exists and if the caller does not have LoggingPermission("control"). |

**See Also**

- [java.util.logging.Logger#setLevel](../java/util/logging/Logger.md))
