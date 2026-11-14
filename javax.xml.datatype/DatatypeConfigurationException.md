# DatatypeConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DatatypeConfigurationException

```
open class DatatypeConfigurationException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [javax.xml.datatype.DatatypeConfigurationException](../javax/xml/datatype/DatatypeConfigurationException.md) |
| --- | --- | --- | --- |

Indicates a serious configuration error.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DatatypeConfigurationException](../javax/xml/datatype/DatatypeConfigurationException.md))`()` Create a new`DatatypeConfigurationException`with no specified detail message and cause. |
| [DatatypeConfigurationException](../javax/xml/datatype/DatatypeConfigurationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new`DatatypeConfigurationException`with the specified detail message. |
| [DatatypeConfigurationException](../javax/xml/datatype/DatatypeConfigurationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Create a new`DatatypeConfigurationException`with the specified detail message and cause. |
| [DatatypeConfigurationException](../javax/xml/datatype/DatatypeConfigurationException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Create a new`DatatypeConfigurationException`with the specified cause. |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](../javax/xml/datatype/DatatypeConfigurationException.md))`()` Print the the trace of methods from where the error originated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](../javax/xml/datatype/DatatypeConfigurationException.md))`(`s:` ` [PrintStream](../java/io/PrintStream.md)`)` Print the the trace of methods from where the error originated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](../javax/xml/datatype/DatatypeConfigurationException.md))`(`s:` ` [PrintWriter](../java/io/PrintWriter.md)`)` Print the the trace of methods from where the error originated. |
| --- | --- |

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
| `s` | [PrintStream](../java/io/PrintStream.md):The stream where the dump will be sent to. |

### printStackTrace

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun printStackTrace(s: PrintWriter): Unit
```

Print the the trace of methods from where the error originated. This will trace all nested exception objects, as well as this object.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [PrintWriter](../java/io/PrintWriter.md):The writer where the dump will be sent to. |
