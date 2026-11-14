# TransformerException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransformerException

```
open class TransformerException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [javax.xml.transform.TransformerException](TransformerException.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [TransformerConfigurationException](TransformerConfigurationException.md) |-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------| | [TransformerConfigurationException](TransformerConfigurationException.md) | Indicates a serious configuration error. | |
| --- | --- | --- | --- | --- | --- | --- |

This class specifies an exceptional condition that occurred during the transformation process.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TransformerException](TransformerException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new TransformerException. |
| [TransformerException](TransformerException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `e:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Wrap an existing exception in a TransformerException. |
| [TransformerException](TransformerException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locator:` ` [SourceLocator](SourceLocator.md)!`)` Create a new TransformerException from a message and a Locator. |
| [TransformerException](TransformerException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locator:` ` [SourceLocator](SourceLocator.md)!`, `e:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Wrap an existing exception in a TransformerException. |
| [TransformerException](TransformerException.md))`(`e:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Create a new TransformerException wrapping an existing exception. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [getException](TransformerException.md))`()` This method retrieves an exception that this exception wraps. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocationAsString](TransformerException.md))`()` Get the location information as a string. |
| open [SourceLocator](SourceLocator.md)! | [getLocator](TransformerException.md))`()` Method getLocator retrieves an instance of a SourceLocator object that specifies where an error occurred. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMessageAndLocation](TransformerException.md))`()` Get the error message with location information appended. |
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [initCause](TransformerException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Initializes the*cause*of this throwable to the specified value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](TransformerException.md))`()` Print the the trace of methods from where the error originated. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](TransformerException.md))`(`s:` ` [PrintStream](../java.io/PrintStream.md)`)` Print the the trace of methods from where the error originated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](TransformerException.md))`(`s:` ` [PrintWriter](../java.io/PrintWriter.md)`)` Print the the trace of methods from where the error originated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocator](TransformerException.md))`(`location:` ` [SourceLocator](SourceLocator.md)!`)` Method setLocator sets an instance of a SourceLocator object that specifies where an error occurred. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](TransformerException.md) Returns the cause of this throwable or`null`if the cause is nonexistent or unknown. |

## Public constructors

### TransformerException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerException(message: String!)
```

Create a new TransformerException.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error or warning message. |

### TransformerException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerException(
    message: String!, 
    e: Throwable!)
```

Wrap an existing exception in a TransformerException.

This is used for throwing processor exceptions before the processing has started.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error or warning message, or null to use the message from the embedded exception. |
| `e` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:Any exception |

### TransformerException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerException(
    message: String!, 
    locator: SourceLocator!)
```

Create a new TransformerException from a message and a Locator.

This constructor is especially useful when an application is creating its own exception from within a DocumentHandler callback.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error or warning message. |
| `locator` | [SourceLocator](SourceLocator.md)!:The locator object for the error or warning. |

### TransformerException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerException(
    message: String!, 
    locator: SourceLocator!, 
    e: Throwable!)
```

Wrap an existing exception in a TransformerException.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error or warning message, or null to use the message from the embedded exception. |
| `locator` | [SourceLocator](SourceLocator.md)!:The locator object for the error or warning. |
| `e` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:Any exception |
| --- | --- |

### TransformerException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransformerException(e: Throwable!)
```

Create a new TransformerException wrapping an existing exception.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------|
| `e` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:The exception to be wrapped. |

## Public methods

### getException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getException(): Throwable!
```

This method retrieves an exception that this exception wraps.

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | An Throwable object, or null. |

**See Also**

- [#getCause](TransformerException.md) 

### getLocationAsString

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocationAsString(): String!
```

Get the location information as a string.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string with location info, or null if there is no location information. |

### getLocator

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocator(): SourceLocator!
```

Method getLocator retrieves an instance of a SourceLocator object that specifies where an error occurred.

| Return ||
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [SourceLocator](SourceLocator.md)! | A SourceLocator object, or null if none was specified. |

### getMessageAndLocation

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMessageAndLocation(): String!
```

Get the error message with location information appended.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A`String`representing the error message with location information appended. |

### initCause

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun initCause(cause: Throwable?): Throwable
```

Initializes the*cause*of this throwable to the specified value. (The cause is the throwable that caused this throwable to get thrown.)

This method can be called at most once. It is generally called from within the constructor, or immediately after creating the throwable. If this throwable was created with [TransformerException(java.lang.Throwable)](TransformerException.md))or [TransformerException(java.lang.String,java.lang.Throwable)](TransformerException.md)), this method cannot be called even once.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:the cause (which is saved for later retrieval by the [getCause()](TransformerException.md) method). (A null value is permitted, and indicates that the cause is nonexistent or unknown.) |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | a reference to this`Throwable`instance. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`cause`is this throwable. (A throwable cannot be its own cause.) |
| `java.lang.IllegalStateException` | if this throwable was created with [TransformerException(java.lang.Throwable)](TransformerException.md))or [TransformerException(java.lang.String,java.lang.Throwable)](TransformerException.md)), or this method has already been called on this throwable. |

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
| `s` | [PrintStream](../java.io/PrintStream.md):The stream where the dump will be sent to. |

### printStackTrace

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun printStackTrace(s: PrintWriter): Unit
```

Print the the trace of methods from where the error originated. This will trace all nested exception objects, as well as this object.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [PrintWriter](../java.io/PrintWriter.md):The writer where the dump will be sent to. |

### setLocator

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLocator(location: SourceLocator!): Unit
```

Method setLocator sets an instance of a SourceLocator object that specifies where an error occurred.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `location` | [SourceLocator](SourceLocator.md)!:A SourceLocator object, or null to clear the location. |

## Properties

### cause

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val cause: Throwable?
```

Returns the cause of this throwable or`null`if the cause is nonexistent or unknown. (The cause is the throwable that caused this throwable to get thrown.)

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | the cause of this throwable or`null`if the cause is nonexistent or unknown. |
