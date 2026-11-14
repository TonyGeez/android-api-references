# Parser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Parser

```
interface Parser
```

| [org.xml.sax.Parser](https://developer.android.com/reference/kotlin/org/xml/sax/Parser#) |

| Known Direct Subclasses [XMLReaderAdapter](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter) |---------------------------------------------------------------------------------------------------------|------------------------------------------| | [XMLReaderAdapter](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter) | Adapt a SAX2 XMLReader as a SAX1 Parser. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 9.**
|
| This interface has been replaced by the SAX2 [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader) interface, which includes Namespace support.

Basic interface for SAX (Simple API for XML) parsers.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This was the main event supplier interface for SAX1; it has been replaced in SAX2 by [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader), which includes Namespace support and sophisticated configurability and extensibility.

All SAX1 parsers must implement this basic interface: it allows applications to register handlers for different types of events and to initiate a parse from a URI, or a character stream.

All SAX1 parsers must also implement a zero-argument constructor (though other constructors are also allowed).

SAX1 parsers are reusable but not re-entrant: the application may reuse a parser object (possibly with a different input source) once the first parse has completed successfully, but it may not invoke the parse() methods recursively within a parse.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/org/xml/sax/Parser#parse(kotlin.String))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse an XML document from a system identifier (URI). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/org/xml/sax/Parser#parse(org.xml.sax.InputSource))`(`source:` ` [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource)!`)` Parse an XML document. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/Parser#setDTDHandler(org.xml.sax.DTDHandler))`(`handler:` ` [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler)!`)` Allow an application to register a DTD event handler. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/Parser#setDocumentHandler(org.xml.sax.DocumentHandler))`(`handler:` ` [DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler)!`)` Allow an application to register a document event handler. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/Parser#setEntityResolver(org.xml.sax.EntityResolver))`(`resolver:` ` [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver)!`)` Allow an application to register a custom entity resolver. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/Parser#setErrorHandler(org.xml.sax.ErrorHandler))`(`handler:` ` [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler)!`)` Allow an application to register an error event handler. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocale](https://developer.android.com/reference/kotlin/org/xml/sax/Parser#setLocale(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Allow an application to request a locale for errors and warnings. |

## Public methods

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parse(systemId: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Parse an XML document from a system identifier (URI).

This method is a shortcut for the common case of reading a document from a system identifier. It is the exact equivalent of the following: 

```kotlin
parse(new InputSource(systemId));
  
```

If the system identifier is a URL, it must be fully resolved by the application before it is passed to the parser.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier (URI). |

| Exceptions ||
|----------------------------|---------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |
| `java.io.IOException` | An IO exception from the parser, possibly from a byte stream or character stream supplied by the application. |

**See Also**

- <https://developer.android.com/reference/kotlin/org/xml/sax/Parser#parse(org.xml.sax.InputSource)> 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parse(source: InputSource!): Unit
```

**Deprecated:** *Deprecated in Java.*

Parse an XML document.

The application can use this method to instruct the SAX parser to begin parsing an XML document from any valid input source (a character stream, a byte stream, or a URI).

Applications may not invoke this method while a parse is in progress (they should create a new Parser instead for each additional XML document). Once a parse is complete, an application may reuse the same Parser object, possibly with a different input source.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource)!:The input source for the top-level of the XML document. |

| Exceptions ||
|----------------------------|---------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |
| `java.io.IOException` | An IO exception from the parser, possibly from a byte stream or character stream supplied by the application. |

**See Also**

- [org.xml.sax.InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource)
- [#parse(java.lang.String)](https://developer.android.com/reference/kotlin/org/xml/sax/Parser#parse(kotlin.String))
- [#setEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/Parser#setEntityResolver(org.xml.sax.EntityResolver))
- [#setDTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/Parser#setDTDHandler(org.xml.sax.DTDHandler))
- [#setDocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/Parser#setDocumentHandler(org.xml.sax.DocumentHandler))
- [#setErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/Parser#setErrorHandler(org.xml.sax.ErrorHandler)) 

### setDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDTDHandler(handler: DTDHandler!): Unit
```

**Deprecated:** *Deprecated in Java.*

Allow an application to register a DTD event handler.

If the application does not register a DTD handler, all DTD events reported by the SAX parser will be silently ignored (this is the default behaviour implemented by HandlerBase).

Applications may register a new or different handler in the middle of a parse, and the SAX parser must begin using the new handler immediately.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `handler` | [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler)!:The DTD handler. |

**See Also**

- [org.xml.sax.DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler)
- [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase) 

### setDocumentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDocumentHandler(handler: DocumentHandler!): Unit
```

**Deprecated:** *Deprecated in Java.*

Allow an application to register a document event handler.

If the application does not register a document handler, all document events reported by the SAX parser will be silently ignored (this is the default behaviour implemented by HandlerBase).

Applications may register a new or different handler in the middle of a parse, and the SAX parser must begin using the new handler immediately.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------|
| `handler` | [DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler)!:The document handler. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler)
- [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase) 

### setEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEntityResolver(resolver: EntityResolver!): Unit
```

**Deprecated:** *Deprecated in Java.*

Allow an application to register a custom entity resolver.

If the application does not register an entity resolver, the SAX parser will resolve system identifiers and open connections to entities itself (this is the default behaviour implemented in HandlerBase).

Applications may register a new or different entity resolver in the middle of a parse, and the SAX parser must begin using the new resolver immediately.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------|
| `resolver` | [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver)!:The object for resolving entities. |

**See Also**

- [org.xml.sax.EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver)
- [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase) 

### setErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setErrorHandler(handler: ErrorHandler!): Unit
```

**Deprecated:** *Deprecated in Java.*

Allow an application to register an error event handler.

If the application does not register an error event handler, all error events reported by the SAX parser will be silently ignored, except for fatalError, which will throw a SAXException (this is the default behaviour implemented by HandlerBase).

Applications may register a new or different handler in the middle of a parse, and the SAX parser must begin using the new handler immediately.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------|
| `handler` | [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler)!:The error handler. |

**See Also**

- [org.xml.sax.ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler)
- [org.xml.sax.SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException)
- [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase) 

### setLocale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setLocale(locale: Locale!): Unit
```

**Deprecated:** *Deprecated in Java.*

Allow an application to request a locale for errors and warnings.

SAX parsers are not required to provide localisation for errors and warnings; if they cannot support the requested locale, however, they must throw a SAX exception. Applications may not request a locale change in the middle of a parse.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:A Java Locale object. |

| Exceptions ||
|----------------------------|------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | Throws an exception (using the previous or default locale) if the requested locale is not supported. |

**See Also**

- [org.xml.sax.SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException)
- [org.xml.sax.SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)
