# Level

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Level

```
open class Level : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.logging.Level](https://developer.android.com/reference/kotlin/java/util/logging/Level#) |

The Level class defines a set of standard logging levels that can be used to control logging output. The logging Level objects are ordered and are specified by ordered integers. Enabling logging at a given level also enables logging at all higher levels.

Clients should normally use the predefined Level constants such as Level.SEVERE.

The levels in descending order are:

- SEVERE (highest value)
- WARNING
- INFO
- CONFIG
- FINE
- FINER
- FINEST (lowest value)

In addition there is a level OFF that can be used to turn off logging, and a level ALL that can be used to enable logging of all messages.

It is possible for third parties to define additional logging levels by subclassing Level. In such cases subclasses should take care to chose unique integer level values and to ensure that they maintain the Object uniqueness property across serialization by defining a suitable readResolve method.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level#Level(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a named Level with a given integer value. |
| [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level#Level(kotlin.String,%20kotlin.Int,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resourceBundleName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a named Level with a given integer value and a given localization resource name. |

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/util/logging/Level#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compare two objects for value equality. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getLocalizedName](https://developer.android.com/reference/kotlin/java/util/logging/Level#getLocalizedName())`()` Return the localized string name of the Level, for the current default locale. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](https://developer.android.com/reference/kotlin/java/util/logging/Level#getName())`()` Return the non-localized string name of the Level. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getResourceBundleName](https://developer.android.com/reference/kotlin/java/util/logging/Level#getResourceBundleName())`()` Return the level's localization resource bundle name, or null if no localization bundle is defined. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/util/logging/Level#hashCode())`()` Generate a hashcode. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [intValue](https://developer.android.com/reference/kotlin/java/util/logging/Level#intValue())`()` Get the integer value for this level. |
| --- | --- |
| openstatic [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level#) | [parse](https://developer.android.com/reference/kotlin/java/util/logging/Level#parse(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Parse a level name string into a Level. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/logging/Level#toString())`()` Returns a string representation of this Level. |

| Properties ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level#) | [ALL](https://developer.android.com/reference/kotlin/java/util/logging/Level#ALL:java.util.logging.Level) ALL indicates that all messages should be logged. |
| static [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level#) | [CONFIG](https://developer.android.com/reference/kotlin/java/util/logging/Level#CONFIG:java.util.logging.Level) CONFIG is a message level for static configuration messages. |
| static [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level#) | [FINE](https://developer.android.com/reference/kotlin/java/util/logging/Level#FINE:java.util.logging.Level) FINE is a message level providing tracing information. |
| --- | --- |
| static [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level#) | [FINER](https://developer.android.com/reference/kotlin/java/util/logging/Level#FINER:java.util.logging.Level) FINER indicates a fairly detailed tracing message. |
| static [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level#) | [FINEST](https://developer.android.com/reference/kotlin/java/util/logging/Level#FINEST:java.util.logging.Level) FINEST indicates a highly detailed tracing message. |
| static [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level#) | [INFO](https://developer.android.com/reference/kotlin/java/util/logging/Level#INFO:java.util.logging.Level) INFO is a message level for informational messages. |
| --- | --- |
| static [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level#) | [OFF](https://developer.android.com/reference/kotlin/java/util/logging/Level#OFF:java.util.logging.Level) OFF is a special level that can be used to turn off logging. |
| static [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level#) | [SEVERE](https://developer.android.com/reference/kotlin/java/util/logging/Level#SEVERE:java.util.logging.Level) SEVERE is a message level indicating a serious failure. |
| static [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level#) | [WARNING](https://developer.android.com/reference/kotlin/java/util/logging/Level#WARNING:java.util.logging.Level) WARNING is a message level indicating a potential problem. |
| --- | --- |

## Protected constructors

### Level

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Level(
    name: String, 
    value: Int)
```

Create a named Level with a given integer value.

Note that this constructor is "protected" to allow subclassing. In general clients of logging should use one of the constant Level objects such as SEVERE or FINEST. However, if clients need to add new logging levels, they may subclass Level and define new constants.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the Level, for example "SEVERE". |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer value for the level. |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if the name is null |

### Level

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Level(
    name: String, 
    value: Int, 
    resourceBundleName: String?)
```

Create a named Level with a given integer value and a given localization resource name.

<br />

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the Level, for example "SEVERE". |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer value for the level. |
| `resourceBundleName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:name of a resource bundle to use in localizing the given name. If the resourceBundleName is null or an empty string, it is ignored. |
| --- | --- |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if the name is null |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compare two objects for value equality.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if and only if the two objects have the same level value. |

### getLocalizedName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalizedName(): String
```

Return the localized string name of the Level, for the current default locale.

If no localization information is available, the non-localized name is returned.

| Return ||
|----------------------------------------------------------------------------------|----------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | localized name |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String
```

Return the non-localized string name of the Level.

| Return ||
|----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | non-localized name |

### getResourceBundleName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResourceBundleName(): String?
```

Return the level's localization resource bundle name, or null if no localization bundle is defined.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | localization resource bundle name |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Generate a hashcode.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hashcode based on the level value |

### intValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun intValue(): Int
```

Get the integer value for this level. This integer value can be used for efficient ordering comparisons between Level objects.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the integer value for this level. |

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parse(name: String): Level
```

Parse a level name string into a Level.

The argument string may consist of either a level name or an integer value.

For example:

- "SEVERE"
- "1000"

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):string to be parsed |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level#) | The parsed value. Passing an integer that corresponds to a known name (e.g., 700) will return the associated name (e.g.,`CONFIG`). Passing an integer that does not (e.g., 1) will return a new level name initialized to that value. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the name is null |
| `java.lang.IllegalArgumentException` | if the value is not valid. Valid values are integers between`Integer.MIN_VALUE`and`Integer.MAX_VALUE`, and all known level names. Known names are the levels defined by this class (e.g.,`FINE`,`FINER`,`FINEST`), or created by this class with appropriate package access, or new levels defined or created by subclasses. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of this Level.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the non-localized name of the Level, for example "INFO". |

## Properties

### ALL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALL: Level
```

ALL indicates that all messages should be logged. This level is initialized to`Integer.MIN_VALUE`. 

### CONFIG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONFIG: Level
```

CONFIG is a message level for static configuration messages.

CONFIG messages are intended to provide a variety of static configuration information, to assist in debugging problems that may be associated with particular configurations. For example, CONFIG message might include the CPU type, the graphics depth, the GUI look-and-feel, etc. This level is initialized to`700`. 

### FINE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FINE: Level
```

FINE is a message level providing tracing information.

All of FINE, FINER, and FINEST are intended for relatively detailed tracing. The exact meaning of the three levels will vary between subsystems, but in general, FINEST should be used for the most voluminous detailed output, FINER for somewhat less detailed output, and FINE for the lowest volume (and most important) messages.

In general the FINE level should be used for information that will be broadly interesting to developers who do not have a specialized interest in the specific subsystem.

FINE messages might include things like minor (recoverable) failures. Issues indicating potential performance problems are also worth logging as FINE. This level is initialized to`500`. 

### FINER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FINER: Level
```

FINER indicates a fairly detailed tracing message. By default logging calls for entering, returning, or throwing an exception are traced at this level. This level is initialized to`400`. 

### FINEST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FINEST: Level
```

FINEST indicates a highly detailed tracing message. This level is initialized to`300`. 

### INFO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INFO: Level
```

INFO is a message level for informational messages.

Typically INFO messages will be written to the console or its equivalent. So the INFO level should only be used for reasonably significant messages that will make sense to end users and system administrators. This level is initialized to`800`. 

### OFF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OFF: Level
```

OFF is a special level that can be used to turn off logging. This level is initialized to`Integer.MAX_VALUE`. 

### SEVERE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEVERE: Level
```

SEVERE is a message level indicating a serious failure.

In general SEVERE messages should describe events that are of considerable importance and which will prevent normal program execution. They should be reasonably intelligible to end users and to system administrators. This level is initialized to`1000`. 

### WARNING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WARNING: Level
```

WARNING is a message level indicating a potential problem.

In general WARNING messages should describe events that will be of interest to end users or system managers, or which indicate potential problems. This level is initialized to`900`.
