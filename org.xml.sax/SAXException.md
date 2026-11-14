# SAXException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SAXException

```
open class SAXException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [org.xml.sax.SAXException](SAXException.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [SAXNotRecognizedException](SAXNotRecognizedException.md), [SAXNotSupportedException](SAXNotSupportedException.md), [SAXParseException](SAXParseException.md) |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------| | [SAXNotRecognizedException](SAXNotRecognizedException.md) | Exception class for an unrecognized identifier. | | [SAXNotSupportedException](SAXNotSupportedException.md) | Exception class for an unsupported operation. | | [SAXParseException](SAXParseException.md) | Encapsulate an XML parse error or warning. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Encapsulate a general SAX error or warning.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This class can contain basic error or warning information from either the XML parser or the application: a parser writer or application writer can subclass it to provide additional functionality. SAX handlers may throw this exception or any exception subclassed from it.

If the application needs to pass through other types of exceptions, it must wrap those exceptions in a SAXException or an exception derived from a SAXException.

If the parser or application needs to include information about a specific location in an XML document, it should use the [SAXParseException](SAXParseException.md) subclass.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SAXException](SAXException.md))`()` Create a new SAXException. |
| [SAXException](SAXException.md))`(`e:` ` [Exception](../java.lang/Exception.md)!`)` Create a new SAXException wrapping an existing exception. |
| [SAXException](SAXException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new SAXException. |
| [SAXException](SAXException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `e:` ` [Exception](../java.lang/Exception.md)!`)` Create a new SAXException from an existing exception. |

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Exception](../java.lang/Exception.md)! | [getException](SAXException.md))`()` Return the embedded exception, if any. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](SAXException.md))`()` Override toString to pick up any embedded exception. |

| Properties ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](SAXException.md) Return a detail message for this exception. |

## Public constructors

### SAXException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SAXException()
```

Create a new SAXException. 

### SAXException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SAXException(e: Exception!)
```

Create a new SAXException wrapping an existing exception.

The existing exception will be embedded in the new one, and its message will become the default message for the SAXException.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [Exception](../java.lang/Exception.md)!:The exception to be wrapped in a SAXException. |

### SAXException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SAXException(message: String!)
```

Create a new SAXException.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error or warning message. |

### SAXException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SAXException(
    message: String!, 
    e: Exception!)
```

Create a new SAXException from an existing exception.

The existing exception will be embedded in the new one, but the new exception will have its own message.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The detail message. |
| `e` | [Exception](../java.lang/Exception.md)!:The exception to be wrapped in a SAXException. |

## Public methods

### getException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getException(): Exception!
```

Return the embedded exception, if any.

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------|
| [Exception](../java.lang/Exception.md)! | The embedded exception, or null if there is none. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Override toString to pick up any embedded exception.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A string representation of this exception. |

## Properties

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

Return a detail message for this exception.

If there is an embedded exception, and if the SAXException has no detail message of its own, this method will return the detail message from the embedded exception.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The error or warning message. |
