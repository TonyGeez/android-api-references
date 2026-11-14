# DatatypeConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DatatypeConfigurationException

```
open class DatatypeConfigurationException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [javax.xml.datatype.DatatypeConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConfigurationException#) |

Indicates a serious configuration error.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DatatypeConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConfigurationException#DatatypeConfigurationException())`()` Create a new`DatatypeConfigurationException`with no specified detail message and cause. |
| [DatatypeConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConfigurationException#DatatypeConfigurationException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new`DatatypeConfigurationException`with the specified detail message. |
| [DatatypeConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConfigurationException#DatatypeConfigurationException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Create a new`DatatypeConfigurationException`with the specified detail message and cause. |
| [DatatypeConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConfigurationException#DatatypeConfigurationException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Create a new`DatatypeConfigurationException`with the specified cause. |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConfigurationException#printStackTrace())`()` Print the the trace of methods from where the error originated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConfigurationException#printStackTrace(java.io.PrintStream))`(`s:` ` [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#)`)` Print the the trace of methods from where the error originated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConfigurationException#printStackTrace(java.io.PrintWriter))`(`s:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)`)` Print the the trace of methods from where the error originated. |

## Public constructors

### DatatypeConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DatatypeConfigurationException()
```

Create a new`DatatypeConfigurationException`with no specified detail message and cause. 

### DatatypeConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DatatypeConfigurationException(message: String!)
```

Create a new`DatatypeConfigurationException`with the specified detail message.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The detail message. |

### DatatypeConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DatatypeConfigurationException(
    message: String!, 
    cause: Throwable!)
```

Create a new`DatatypeConfigurationException`with the specified detail message and cause.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The detail message. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:The cause. A`null`value is permitted, and indicates that the cause is nonexistent or unknown. |

### DatatypeConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DatatypeConfigurationException(cause: Throwable!)
```

Create a new`DatatypeConfigurationException`with the specified cause.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:The cause. A`null`value is permitted, and indicates that the cause is nonexistent or unknown. |

## Public methods

### printStackTrace

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun printStackTrace(): Unit
```

Print the the trace of methods from where the error originated. This will trace all nested exception objects, as well as this object. 

### printStackTrace

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun printStackTrace(s: PrintStream): Unit
```

Print the the trace of methods from where the error originated. This will trace all nested exception objects, as well as this object.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#):The stream where the dump will be sent to. |

### printStackTrace

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun printStackTrace(s: PrintWriter): Unit
```

Print the the trace of methods from where the error originated. This will trace all nested exception objects, as well as this object.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#):The writer where the dump will be sent to. |
