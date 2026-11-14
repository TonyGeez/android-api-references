# Parser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Parser

```
interface Parser
```

| [org.xml.sax.Parser](Parser.md) |

| Known Direct Subclasses [XMLReaderAdapter](../org.xml.sax.helpers/XMLReaderAdapter.md) |---------------------------------------------------------------------------------------------------------|------------------------------------------| | [XMLReaderAdapter](../org.xml.sax.helpers/XMLReaderAdapter.md) | Adapt a SAX2 XMLReader as a SAX1 Parser. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 9.**
|
| This interface has been replaced by the SAX2 [XMLReader](XMLReader.md) interface, which includes Namespace support.

Basic interface for SAX (Simple API for XML) parsers.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This was the main event supplier interface for SAX1; it has been replaced in SAX2 by [XMLReader](XMLReader.md), which includes Namespace support and sophisticated configurability and extensibility.

All SAX1 parsers must implement this basic interface: it allows applications to register handlers for different types of events and to initiate a parse from a URI, or a character stream.

All SAX1 parsers must also implement a zero-argument constructor (though other constructors are also allowed).

SAX1 parsers are reusable but not re-entrant: the application may reuse a parser object (possibly with a different input source) once the first parse has completed successfully, but it may not invoke the parse() methods recursively within a parse.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](Parser.md))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse an XML document from a system identifier (URI). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](Parser.md))`(`source:` ` [InputSource](InputSource.md)!`)` Parse an XML document. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDTDHandler](Parser.md))`(`handler:` ` [DTDHandler](DTDHandler.md)!`)` Allow an application to register a DTD event handler. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentHandler](Parser.md))`(`handler:` ` [DocumentHandler](DocumentHandler.md)!`)` Allow an application to register a document event handler. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntityResolver](Parser.md))`(`resolver:` ` [EntityResolver](EntityResolver.md)!`)` Allow an application to register a custom entity resolver. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](Parser.md))`(`handler:` ` [ErrorHandler](ErrorHandler.md)!`)` Allow an application to register an error event handler. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocale](Parser.md))`(`locale:` ` [Locale](../java.util/Locale.md)!`)` Allow an application to request a locale for errors and warnings. |

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
| `source` | [InputSource](InputSource.md)!:The input source for the top-level of the XML document. |

| Exceptions ||
|----------------------------|---------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |
| `java.io.IOException` | An IO exception from the parser, possibly from a byte stream or character stream supplied by the application. |

**See Also**

- [org.xml.sax.InputSource](InputSource.md)
- [#parse(java.lang.String)](Parser.md))
- [#setEntityResolver](Parser.md))
- [#setDTDHandler](Parser.md))
- [#setDocumentHandler](Parser.md))
- [#setErrorHandler](Parser.md)) 

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
| `handler` | [DTDHandler](DTDHandler.md)!:The DTD handler. |

**See Also**

- [org.xml.sax.DTDHandler](DTDHandler.md)
- [org.xml.sax.HandlerBase](HandlerBase.md) 

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
| `handler` | [DocumentHandler](DocumentHandler.md)!:The document handler. |

**See Also**

- [org.xml.sax.DocumentHandler](DocumentHandler.md)
- [org.xml.sax.HandlerBase](HandlerBase.md) 

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
| `resolver` | [EntityResolver](EntityResolver.md)!:The object for resolving entities. |

**See Also**

- [org.xml.sax.EntityResolver](EntityResolver.md)
- [org.xml.sax.HandlerBase](HandlerBase.md) 

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
| `handler` | [ErrorHandler](ErrorHandler.md)!:The error handler. |

**See Also**

- [org.xml.sax.ErrorHandler](ErrorHandler.md)
- [org.xml.sax.SAXException](SAXException.md)
- [org.xml.sax.HandlerBase](HandlerBase.md) 

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
| `locale` | [Locale](../java.util/Locale.md)!:A Java Locale object. |

| Exceptions ||
|----------------------------|------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | Throws an exception (using the previous or default locale) if the requested locale is not supported. |

**See Also**

- [org.xml.sax.SAXException](SAXException.md)
- [org.xml.sax.SAXParseException](SAXParseException.md)
