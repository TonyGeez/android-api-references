# SAXParseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SAXParseException

```
open class SAXParseException : SAXException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [org.xml.sax.SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [org.xml.sax.SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException#) |

Encapsulate an XML parse error or warning.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This exception may include information for locating the error in the original XML document, as if it came from a [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator) object. Note that although the application will receive a SAXParseException as the argument to the handlers in the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler) interface, the application is not actually required to throw the exception; instead, it can simply read the information in it and take a different action.

Since this exception is a subclass of [SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException), it inherits the ability to wrap another exception.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException#SAXParseException(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `lineNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `columnNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new SAXParseException. |
| [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException#SAXParseException(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20java.lang.Exception))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `lineNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `columnNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `e:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!`)` Create a new SAXParseException with an embedded exception. |
| [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException#SAXParseException(kotlin.String,%20org.xml.sax.Locator))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locator:` ` [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator)!`)` Create a new SAXParseException from a message and a Locator. |
| [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException#SAXParseException(kotlin.String,%20org.xml.sax.Locator,%20java.lang.Exception))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locator:` ` [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator)!`, `e:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!`)` Wrap an existing exception in a SAXParseException. |

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnNumber](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException#getColumnNumber())`()` The column number of the end of the text where the exception occurred. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineNumber](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException#getLineNumber())`()` The line number of the end of the text where the exception occurred. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPublicId](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException#getPublicId())`()` Get the public identifier of the entity where the exception occurred. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException#getSystemId())`()` Get the system identifier of the entity where the exception occurred. |

| Inherited functions ||
|---|---|
| From class [SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException) |----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)! | [getException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException#getException())`()` <br /> Return the embedded exception, if any. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException#toString())`()` <br /> Override toString to pick up any embedded exception. <br /> | ||

| Inherited properties ||
|---|---|
| From class [SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException) |-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException#message:kotlin.String) <br /> Return a detail message for this exception. If there is an embedded exception, and if the SAXException has no detail message of its own, this method will return the detail message from the embedded exception. <br /> | ||

## Public constructors

### SAXParseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SAXParseException(
    message: String!, 
    publicId: String!, 
    systemId: String!, 
    lineNumber: Int, 
    columnNumber: Int)
```

Create a new SAXParseException.

This constructor is most useful for parser writers.

All parameters except the message are as if they were provided by a [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator). For example, if the system identifier is a URL (including relative filename), the caller must resolve it fully before creating the exception.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error or warning message. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The public identifier of the entity that generated the error or warning. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier of the entity that generated the error or warning. |
| --- | --- |
| `lineNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The line number of the end of the text that caused the error or warning. |
| `columnNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The column number of the end of the text that cause the error or warning. |

### SAXParseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SAXParseException(
    message: String!, 
    publicId: String!, 
    systemId: String!, 
    lineNumber: Int, 
    columnNumber: Int, 
    e: Exception!)
```

Create a new SAXParseException with an embedded exception.

This constructor is most useful for parser writers who need to wrap an exception that is not a subclass of [SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException).

All parameters except the message and exception are as if they were provided by a [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator). For example, if the system identifier is a URL (including relative filename), the caller must resolve it fully before creating the exception.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error or warning message, or null to use the message from the embedded exception. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The public identifier of the entity that generated the error or warning. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier of the entity that generated the error or warning. |
| --- | --- |
| `lineNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The line number of the end of the text that caused the error or warning. |
| `columnNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The column number of the end of the text that cause the error or warning. |
| `e` | [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!:Another exception to embed in this one. |
| --- | --- |

### SAXParseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SAXParseException(
    message: String!, 
    locator: Locator!)
```

Create a new SAXParseException from a message and a Locator.

This constructor is especially useful when an application is creating its own exception from within a [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler) callback.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error or warning message. |
| `locator` | [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator)!:The locator object for the error or warning (may be null). |

**See Also**

- [org.xml.sax.Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator) 

### SAXParseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SAXParseException(
    message: String!, 
    locator: Locator!, 
    e: Exception!)
```

Wrap an existing exception in a SAXParseException.

This constructor is especially useful when an application is creating its own exception from within a [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler) callback, and needs to wrap an existing exception that is not a subclass of [SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error or warning message, or null to use the message from the embedded exception. |
| `locator` | [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator)!:The locator object for the error or warning (may be null). |
| `e` | [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!:Any exception. |
| --- | --- |

**See Also**

- [org.xml.sax.Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator)

## Public methods

### getColumnNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColumnNumber(): Int
```

The column number of the end of the text where the exception occurred.

The first column in a line is position 1.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer representing the column number, or -1 if none is available. |

**See Also**

- [org.xml.sax.Locator#getColumnNumber](https://developer.android.com/reference/kotlin/org/xml/sax/Locator#getColumnNumber()) 

### getLineNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineNumber(): Int
```

The line number of the end of the text where the exception occurred.

The first line is line 1.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer representing the line number, or -1 if none is available. |

**See Also**

- [org.xml.sax.Locator#getLineNumber](https://developer.android.com/reference/kotlin/org/xml/sax/Locator#getLineNumber()) 

### getPublicId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPublicId(): String!
```

Get the public identifier of the entity where the exception occurred.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string containing the public identifier, or null if none is available. |

**See Also**

- [org.xml.sax.Locator#getPublicId](https://developer.android.com/reference/kotlin/org/xml/sax/Locator#getPublicId()) 

### getSystemId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSystemId(): String!
```

Get the system identifier of the entity where the exception occurred.

If the system identifier is a URL, it will have been resolved fully.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string containing the system identifier, or null if none is available. |

**See Also**

- [org.xml.sax.Locator#getSystemId](https://developer.android.com/reference/kotlin/org/xml/sax/Locator#getSystemId())
