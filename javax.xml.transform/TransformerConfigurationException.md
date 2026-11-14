# TransformerConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransformerConfigurationException

```
open class TransformerConfigurationException : TransformerException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [javax.xml.transform.TransformerException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException) ||
| | | | ↳ | [javax.xml.transform.TransformerConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerConfigurationException#) |

Indicates a serious configuration error.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TransformerConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerConfigurationException#TransformerConfigurationException())`()` Create a new`TransformerConfigurationException`with no detail message. |
| [TransformerConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerConfigurationException#TransformerConfigurationException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new`TransformerConfigurationException`with the`String `specified as an error message. |
| [TransformerConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerConfigurationException#TransformerConfigurationException(kotlin.String,%20kotlin.Throwable))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `e:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Create a new`TransformerConfigurationException`with the given`Exception`base cause and detail message. |
| [TransformerConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerConfigurationException#TransformerConfigurationException(kotlin.String,%20javax.xml.transform.SourceLocator))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locator:` ` [SourceLocator](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator)!`)` Create a new TransformerConfigurationException from a message and a Locator. |
| [TransformerConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerConfigurationException#TransformerConfigurationException(kotlin.String,%20javax.xml.transform.SourceLocator,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locator:` ` [SourceLocator](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator)!`, `e:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Wrap an existing exception in a TransformerConfigurationException. |
| [TransformerConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerConfigurationException#TransformerConfigurationException(kotlin.Throwable))`(`e:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Create a new`TransformerConfigurationException`with a given`Exception`base cause of the error. |

| Inherited functions ||
|---|---|
| From class [TransformerException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException) |----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [getException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException#getException())`()` <br /> This method retrieves an exception that this exception wraps. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocationAsString](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException#getLocationAsString())`()` <br /> Get the location information as a string. <br /> | | [SourceLocator](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator)! | [getLocator](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException#getLocator())`()` <br /> Method getLocator retrieves an instance of a SourceLocator object that specifies where an error occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMessageAndLocation](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException#getMessageAndLocation())`()` <br /> Get the error message with location information appended. <br /> | | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [initCause](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException#initCause(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> Initializes the*cause*of this throwable to the specified value. (The cause is the throwable that caused this throwable to get thrown.) This method can be called at most once. It is generally called from within the constructor, or immediately after creating the throwable. If this throwable was created with [TransformerException(java.lang.Throwable)](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException#TransformerException(kotlin.Throwable))or [TransformerException(java.lang.String,java.lang.Throwable)](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException#TransformerException(kotlin.String,%20kotlin.Throwable)), this method cannot be called even once. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException#printStackTrace())`()` <br /> Print the the trace of methods from where the error originated. This will trace all nested exception objects, as well as this object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException#printStackTrace(java.io.PrintStream))`(`s:` ` [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#)`)` <br /> Print the the trace of methods from where the error originated. This will trace all nested exception objects, as well as this object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException#printStackTrace(java.io.PrintWriter))`(`s:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)`)` <br /> Print the the trace of methods from where the error originated. This will trace all nested exception objects, as well as this object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocator](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException#setLocator(javax.xml.transform.SourceLocator))`(`location:` ` [SourceLocator](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator)!`)` <br /> Method setLocator sets an instance of a SourceLocator object that specifies where an error occurred. <br /> | ||

| Inherited properties ||
|---|---|
| From class [TransformerException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException) |-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException#cause:kotlin.Throwable) <br /> Returns the cause of this throwable or`null`if the cause is nonexistent or unknown. (The cause is the throwable that caused this throwable to get thrown.) <br /> | ||

## Public constructors

### TransformerConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerConfigurationException()
```

Create a new`TransformerConfigurationException`with no detail message. 

### TransformerConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerConfigurationException(msg: String!)
```

Create a new`TransformerConfigurationException`with the`String `specified as an error message.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error message for the exception. |

### TransformerConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerConfigurationException(
    msg: String!, 
    e: Throwable!)
```

Create a new`TransformerConfigurationException`with the given`Exception`base cause and detail message.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:The exception to be encapsulated in a TransformerConfigurationException |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The detail message. |

### TransformerConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerConfigurationException(
    message: String!, 
    locator: SourceLocator!)
```

Create a new TransformerConfigurationException from a message and a Locator.

This constructor is especially useful when an application is creating its own exception from within a DocumentHandler callback.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error or warning message. |
| `locator` | [SourceLocator](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator)!:The locator object for the error or warning. |

### TransformerConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerConfigurationException(
    message: String!, 
    locator: SourceLocator!, 
    e: Throwable!)
```

Wrap an existing exception in a TransformerConfigurationException.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error or warning message, or null to use the message from the embedded exception. |
| `locator` | [SourceLocator](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator)!:The locator object for the error or warning. |
| `e` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:Any exception. |

### TransformerConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerConfigurationException(e: Throwable!)
```

Create a new`TransformerConfigurationException`with a given`Exception`base cause of the error.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:The exception to be encapsulated in a TransformerConfigurationException. |
