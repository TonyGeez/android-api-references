# TransformerFactoryConfigurationError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransformerFactoryConfigurationError

```
open class TransformerFactoryConfigurationError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error.html#) ||
| | | ↳ | [javax.xml.transform.TransformerFactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactoryConfigurationError#) |
| --- | --- | --- | --- |

Thrown when a problem with configuration with the Transformer Factories exists. This error will typically be thrown when the class of a transformation factory specified in the system properties cannot be found or instantiated.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TransformerFactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactoryConfigurationError#TransformerFactoryConfigurationError())`()` Create a new`TransformerFactoryConfigurationError`with no detail message. |
| [TransformerFactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactoryConfigurationError#TransformerFactoryConfigurationError(java.lang.Exception))`(`e:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!`)` Create a new`TransformerFactoryConfigurationError`with a given`Exception`base cause of the error. |
| [TransformerFactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactoryConfigurationError#TransformerFactoryConfigurationError(java.lang.Exception,%20kotlin.String))`(`e:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new`TransformerFactoryConfigurationError`with the given`Exception`base cause and detail message. |
| [TransformerFactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactoryConfigurationError#TransformerFactoryConfigurationError(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new`TransformerFactoryConfigurationError`with the`String`specified as an error message. |

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)! | [getException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactoryConfigurationError#getException())`()` Return the actual exception (if any) that caused this exception to be raised. |

| Properties ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactoryConfigurationError#message:kotlin.String) Return the message (if any) for this error . |

## Public constructors

### TransformerFactoryConfigurationError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerFactoryConfigurationError()
```

Create a new`TransformerFactoryConfigurationError`with no detail message. 

### TransformerFactoryConfigurationError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerFactoryConfigurationError(e: Exception!)
```

Create a new`TransformerFactoryConfigurationError`with a given`Exception`base cause of the error.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!:The exception to be encapsulated in a TransformerFactoryConfigurationError. |

### TransformerFactoryConfigurationError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerFactoryConfigurationError(
    e: Exception!, 
    msg: String!)
```

Create a new`TransformerFactoryConfigurationError`with the given`Exception`base cause and detail message.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!:The exception to be encapsulated in a TransformerFactoryConfigurationError |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The detail message. |

### TransformerFactoryConfigurationError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerFactoryConfigurationError(msg: String!)
```

Create a new`TransformerFactoryConfigurationError`with the`String`specified as an error message.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error message for the exception. |

## Public methods

### getException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getException(): Exception!
```

Return the actual exception (if any) that caused this exception to be raised.

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)! | The encapsulated exception, or null if there is none. |

## Properties

### message

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

Return the message (if any) for this error . If there is no message for the exception and there is an encapsulated exception then the message of that exception will be returned.

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The error message. |
