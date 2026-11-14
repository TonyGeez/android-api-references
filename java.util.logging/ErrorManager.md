# ErrorManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ErrorManager

```
open class ErrorManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.logging.ErrorManager](https://developer.android.com/reference/kotlin/java/util/logging/ErrorManager#) |

ErrorManager objects can be attached to Handlers to process any error that occurs on a Handler during Logging.

When processing logging output, if a Handler encounters problems then rather than throwing an Exception back to the issuer of the logging call (who is unlikely to be interested) the Handler should call its associated ErrorManager.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLOSE_FAILURE](https://developer.android.com/reference/kotlin/java/util/logging/ErrorManager#CLOSE_FAILURE:kotlin.Int) CLOSE_FAILURE is used when a close of an output stream fails. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLUSH_FAILURE](https://developer.android.com/reference/kotlin/java/util/logging/ErrorManager#FLUSH_FAILURE:kotlin.Int) FLUSH_FAILURE is used when a flush to an output stream fails. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_FAILURE](https://developer.android.com/reference/kotlin/java/util/logging/ErrorManager#FORMAT_FAILURE:kotlin.Int) FORMAT_FAILURE is used when formatting fails for any reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GENERIC_FAILURE](https://developer.android.com/reference/kotlin/java/util/logging/ErrorManager#GENERIC_FAILURE:kotlin.Int) GENERIC_FAILURE is used for failure that don't fit into one of the other categories. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPEN_FAILURE](https://developer.android.com/reference/kotlin/java/util/logging/ErrorManager#OPEN_FAILURE:kotlin.Int) OPEN_FAILURE is used when an open of an output stream fails. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WRITE_FAILURE](https://developer.android.com/reference/kotlin/java/util/logging/ErrorManager#WRITE_FAILURE:kotlin.Int) WRITE_FAILURE is used when a write to an output stream fails. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------|---|
| [ErrorManager](https://developer.android.com/reference/kotlin/java/util/logging/ErrorManager#ErrorManager())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [error](https://developer.android.com/reference/kotlin/java/util/logging/ErrorManager#error(kotlin.String,%20java.lang.Exception,%20kotlin.Int))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ex:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The error method is called when a Handler failure occurs. |

## Constants

### CLOSE_FAILURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLOSE_FAILURE: Int
```

CLOSE_FAILURE is used when a close of an output stream fails. 

 Value: 3

### FLUSH_FAILURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLUSH_FAILURE: Int
```

FLUSH_FAILURE is used when a flush to an output stream fails. 

 Value: 2

### FORMAT_FAILURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_FAILURE: Int
```

FORMAT_FAILURE is used when formatting fails for any reason. 

 Value: 5

### GENERIC_FAILURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GENERIC_FAILURE: Int
```

GENERIC_FAILURE is used for failure that don't fit into one of the other categories. 

 Value: 0

### OPEN_FAILURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPEN_FAILURE: Int
```

OPEN_FAILURE is used when an open of an output stream fails. 

 Value: 4

### WRITE_FAILURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WRITE_FAILURE: Int
```

WRITE_FAILURE is used when a write to an output stream fails. 

 Value: 1

## Public constructors

### ErrorManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ErrorManager()
```

## Public methods

### error

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun error(
    msg: String!, 
    ex: Exception!, 
    code: Int
): Unit
```

The error method is called when a Handler failure occurs.

This method may be overridden in subclasses. The default behavior in this base class is that the first call is reported to System.err, and subsequent calls are ignored.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a descriptive string (may be null) |
| `ex` | [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!:an exception (may be null) |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an error code defined in ErrorManager |
