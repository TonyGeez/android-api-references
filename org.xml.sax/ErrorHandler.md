# ErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ErrorHandler

```
interface ErrorHandler
```

| [org.xml.sax.ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler#) |

| Known Direct Subclasses [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler), [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase), [XMLFilterImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl) |-----------------------------------------------------------------------------------------------------|---------------------------------------------| | [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler) | Default base class for SAX2 event handlers. | | [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase) | Default base class for handlers. | | [XMLFilterImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl) | Base class for deriving an XML filter. | |

| Known Indirect Subclasses [DefaultHandler2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2) |---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DefaultHandler2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2) | This class extends the SAX2 base handler class to support the SAX2 [LexicalHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler), [DeclHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler), and [EntityResolver2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/EntityResolver2) extensions. | |

Basic interface for SAX error handlers.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

If a SAX application needs to implement customized error handling, it must implement this interface and then register an instance with the XML reader using the [setErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setErrorHandler(org.xml.sax.ErrorHandler))method. The parser will then report all errors and warnings through this interface.

**WARNING:** If an application does*not* register an ErrorHandler, XML parsing errors will go unreported, except that*SAXParseException* s will be thrown for fatal errors. In order to detect validity errors, an ErrorHandler that does something with [error()](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler#error(org.xml.sax.SAXParseException))calls must be registered.

For XML processing errors, a SAX driver must use this interface in preference to throwing an exception: it is up to the application to decide whether to throw an exception for different types of errors and warnings. Note, however, that there is no requirement that the parser continue to report additional errors after a call to [fatalError](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler#fatalError(org.xml.sax.SAXParseException)). In other words, a SAX driver class may throw an exception after reporting any fatalError. Also parsers may throw appropriate exceptions for non-XML errors. For example, org.xml.sax.XMLReader#parse would throw an IOException for errors accessing entities or the document.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [error](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler#error(org.xml.sax.SAXParseException))`(`exception:` ` [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)!`)` Receive notification of a recoverable error. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fatalError](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler#fatalError(org.xml.sax.SAXParseException))`(`exception:` ` [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)!`)` Receive notification of a non-recoverable error. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [warning](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler#warning(org.xml.sax.SAXParseException))`(`exception:` ` [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)!`)` Receive notification of a warning. |

## Public methods

### error

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun error(exception: SAXParseException!): Unit
```

Receive notification of a recoverable error.

This corresponds to the definition of "error" in section 1.2 of the W3C XML 1.0 Recommendation. For example, a validating parser would use this callback to report the violation of a validity constraint. The default behaviour is to take no action.

The SAX parser must continue to provide normal parsing events after invoking this method: it should still be possible for the application to process the document through to the end. If the application cannot do so, then the parser should report a fatal error even if the XML recommendation does not require it to do so.

Filters may use this method to report other, non-XML errors as well.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)!:The error information encapsulated in a SAX parse exception. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException) 

### fatalError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun fatalError(exception: SAXParseException!): Unit
```

Receive notification of a non-recoverable error.

**There is an apparent contradiction between the documentation for this method and the documentation for [org.xml.sax.ContentHandler#endDocument](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler#endDocument()). Until this ambiguity is resolved in a future major release, clients should make no assumptions about whether endDocument() will or will not be invoked when the parser has reported a fatalError() or thrown an exception.**

This corresponds to the definition of "fatal error" in section 1.2 of the W3C XML 1.0 Recommendation. For example, a parser would use this callback to report the violation of a well-formedness constraint.

The application must assume that the document is unusable after the parser has invoked this method, and should continue (if at all) only for the sake of collecting additional error messages: in fact, SAX parsers are free to stop reporting any other events once this method has been invoked.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)!:The error information encapsulated in a SAX parse exception. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException) 

### warning

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun warning(exception: SAXParseException!): Unit
```

Receive notification of a warning.

SAX parsers will use this method to report conditions that are not errors or fatal errors as defined by the XML recommendation. The default behaviour is to take no action.

The SAX parser must continue to provide normal parsing events after invoking this method: it should still be possible for the application to process the document through to the end.

Filters may use this method to report other, non-XML warnings as well.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)!:The warning information encapsulated in a SAX parse exception. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)
