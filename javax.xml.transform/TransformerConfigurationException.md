# TransformerConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransformerConfigurationException

```
open class TransformerConfigurationException : TransformerException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [javax.xml.transform.TransformerException](../javax/xml/transform/TransformerException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [javax.xml.transform.TransformerConfigurationException](../javax/xml/transform/TransformerConfigurationException.md) |

Indicates a serious configuration error.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TransformerConfigurationException](../javax/xml/transform/TransformerConfigurationException.md))`()` Create a new`TransformerConfigurationException`with no detail message. |
| [TransformerConfigurationException](../javax/xml/transform/TransformerConfigurationException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new`TransformerConfigurationException`with the`String `specified as an error message. |
| [TransformerConfigurationException](../javax/xml/transform/TransformerConfigurationException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `e:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Create a new`TransformerConfigurationException`with the given`Exception`base cause and detail message. |
| [TransformerConfigurationException](../javax/xml/transform/TransformerConfigurationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locator:` ` [SourceLocator](../javax/xml/transform/SourceLocator.md)!`)` Create a new TransformerConfigurationException from a message and a Locator. |
| [TransformerConfigurationException](../javax/xml/transform/TransformerConfigurationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locator:` ` [SourceLocator](../javax/xml/transform/SourceLocator.md)!`, `e:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Wrap an existing exception in a TransformerConfigurationException. |
| [TransformerConfigurationException](../javax/xml/transform/TransformerConfigurationException.md))`(`e:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Create a new`TransformerConfigurationException`with a given`Exception`base cause of the error. |

| Inherited functions ||
|---|---|
| From class [TransformerException](../javax/xml/transform/TransformerException.md) |----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [getException](../javax/xml/transform/TransformerException.md))`()` <br /> This method retrieves an exception that this exception wraps. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocationAsString](../javax/xml/transform/TransformerException.md))`()` <br /> Get the location information as a string. <br /> | | [SourceLocator](../javax/xml/transform/SourceLocator.md)! | [getLocator](../javax/xml/transform/TransformerException.md))`()` <br /> Method getLocator retrieves an instance of a SourceLocator object that specifies where an error occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMessageAndLocation](../javax/xml/transform/TransformerException.md))`()` <br /> Get the error message with location information appended. <br /> | | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [initCause](../javax/xml/transform/TransformerException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> Initializes the*cause*of this throwable to the specified value. (The cause is the throwable that caused this throwable to get thrown.) This method can be called at most once. It is generally called from within the constructor, or immediately after creating the throwable. If this throwable was created with [TransformerException(java.lang.Throwable)](../javax/xml/transform/TransformerException.md))or [TransformerException(java.lang.String,java.lang.Throwable)](../javax/xml/transform/TransformerException.md)), this method cannot be called even once. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](../javax/xml/transform/TransformerException.md))`()` <br /> Print the the trace of methods from where the error originated. This will trace all nested exception objects, as well as this object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](../javax/xml/transform/TransformerException.md))`(`s:` ` [PrintStream](../java/io/PrintStream.md)`)` <br /> Print the the trace of methods from where the error originated. This will trace all nested exception objects, as well as this object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](../javax/xml/transform/TransformerException.md))`(`s:` ` [PrintWriter](../java/io/PrintWriter.md)`)` <br /> Print the the trace of methods from where the error originated. This will trace all nested exception objects, as well as this object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocator](../javax/xml/transform/TransformerException.md))`(`location:` ` [SourceLocator](../javax/xml/transform/SourceLocator.md)!`)` <br /> Method setLocator sets an instance of a SourceLocator object that specifies where an error occurred. <br /> | ||

| Inherited properties ||
|---|---|
| From class [TransformerException](../javax/xml/transform/TransformerException.md) |-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](../javax/xml/transform/TransformerException.md) <br /> Returns the cause of this throwable or`null`if the cause is nonexistent or unknown. (The cause is the throwable that caused this throwable to get thrown.) <br /> | ||

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
| `locator` | [SourceLocator](../javax/xml/transform/SourceLocator.md)!:The locator object for the error or warning. |

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
| `locator` | [SourceLocator](../javax/xml/transform/SourceLocator.md)!:The locator object for the error or warning. |
| `e` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:Any exception. |
| --- | --- |

### TransformerConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerConfigurationException(e: Throwable!)
```

Create a new`TransformerConfigurationException`with a given`Exception`base cause of the error.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:The exception to be encapsulated in a TransformerConfigurationException. |
