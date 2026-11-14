# FactoryConfigurationError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FactoryConfigurationError

```
open class FactoryConfigurationError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error.html#) ||
| | | ↳ | [javax.xml.parsers.FactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/parsers/FactoryConfigurationError#) |

Thrown when a problem with configuration with the Parser Factories exists. This error will typically be thrown when the class of a parser factory specified in the system properties cannot be found or instantiated.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/parsers/FactoryConfigurationError#FactoryConfigurationError())`()` Create a new`FactoryConfigurationError`with no detail message. |
| [FactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/parsers/FactoryConfigurationError#FactoryConfigurationError(java.lang.Exception))`(`e:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!`)` Create a new`FactoryConfigurationError`with a given`Exception`base cause of the error. |
| [FactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/parsers/FactoryConfigurationError#FactoryConfigurationError(java.lang.Exception,%20kotlin.String))`(`e:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new`FactoryConfigurationError`with the given`Exception`base cause and detail message. |
| [FactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/parsers/FactoryConfigurationError#FactoryConfigurationError(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new`FactoryConfigurationError`with the`String `specified as an error message. |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)! | [getException](https://developer.android.com/reference/kotlin/javax/xml/parsers/FactoryConfigurationError#getException())`()` Return the actual exception (if any) that caused this exception to be raised. |

| Properties ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/javax/xml/parsers/FactoryConfigurationError#message:kotlin.String) Return the message (if any) for this error . |

## Public constructors

### FactoryConfigurationError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FactoryConfigurationError()
```

Create a new`FactoryConfigurationError`with no detail message. 

### FactoryConfigurationError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FactoryConfigurationError(e: Exception!)
```

Create a new`FactoryConfigurationError`with a given`Exception`base cause of the error.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!:The exception to be encapsulated in a FactoryConfigurationError. |

### FactoryConfigurationError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FactoryConfigurationError(
    e: Exception!, 
    msg: String!)
```

Create a new`FactoryConfigurationError`with the given`Exception`base cause and detail message.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!:The exception to be encapsulated in a FactoryConfigurationError |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The detail message. |

### FactoryConfigurationError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FactoryConfigurationError(msg: String!)
```

Create a new`FactoryConfigurationError`with the`String `specified as an error message.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error message for the exception. |

## Public methods

### getException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getException(): Exception!
```

Return the actual exception (if any) that caused this exception to be raised.

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)! | The encapsulated exception, or null if there is none. |

## Properties

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

Return the message (if any) for this error . If there is no message for the exception and there is an encapsulated exception then the message of that exception, if it exists will be returned. Else the name of the encapsulated exception will be returned.

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The error message. |
