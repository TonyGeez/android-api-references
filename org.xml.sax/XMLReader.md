# XMLReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XMLReader

```
interface XMLReader
```

| [org.xml.sax.XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#) |

| Known Direct Subclasses [Driver](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver.html#), [ParserAdapter](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter), [XMLFilter](https://developer.android.com/reference/kotlin/org/xml/sax/XMLFilter) |---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------| | [Driver](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver.html#) | SAX2 Driver that pulls events from XmlPullParser and converts them into SAX2 callbacks. | | [ParserAdapter](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter) | Adapt a SAX1 Parser as a SAX2 XMLReader. | | [XMLFilter](https://developer.android.com/reference/kotlin/org/xml/sax/XMLFilter) | Interface for an XML filter. | |

| Known Indirect Subclasses [XMLFilterImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl) |---------------------------------------------------------------------------------------------------|----------------------------------------| | [XMLFilterImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl) | Base class for deriving an XML filter. | |

Interface for reading an XML document using callbacks.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

**Note:** despite its name, this interface does*not* extend the standard Java [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#) interface, because reading XML is a fundamentally different activity than reading character data.

XMLReader is the interface that an XML parser's SAX2 driver must implement. This interface allows an application to set and query features and properties in the parser, to register event handlers for document processing, and to initiate a document parse.

All SAX interfaces are assumed to be synchronous: the #parse methods must not return until parsing is complete, and readers must wait for an event-handler callback to return before reporting the next event.

This interface replaces the (now deprecated) SAX 1.0 interface. The XMLReader interface contains two important enhancements over the old Parser interface (as well as some minor ones):

1. it adds a standard way to query and set features and properties; and
2. it adds Namespace support, which is required for many higher-level XML standards.

There are adapters available to convert a SAX1 Parser to a SAX2 XMLReader and vice-versa.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler)! | [getContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getContentHandler())`()` Return the current content handler. |
| abstract [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler)! | [getDTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getDTDHandler())`()` Return the current DTD handler. |
| abstract [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver)! | [getEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getEntityResolver())`()` Return the current entity resolver. |
| abstract [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler)! | [getErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getErrorHandler())`()` Return the current error handler. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getFeature(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a feature flag. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getProperty](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getProperty(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#parse(kotlin.String))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse an XML document from a system identifier (URI). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#parse(org.xml.sax.InputSource))`(`input:` ` [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource)!`)` Parse an XML document. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setContentHandler(org.xml.sax.ContentHandler))`(`handler:` ` [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler)!`)` Allow an application to register a content event handler. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setDTDHandler(org.xml.sax.DTDHandler))`(`handler:` ` [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler)!`)` Allow an application to register a DTD event handler. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setEntityResolver(org.xml.sax.EntityResolver))`(`resolver:` ` [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver)!`)` Allow an application to register an entity resolver. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setErrorHandler(org.xml.sax.ErrorHandler))`(`handler:` ` [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler)!`)` Allow an application to register an error event handler. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setFeature(kotlin.String,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the value of a feature flag. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setProperty(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Set the value of a property. |

## Public methods

### getContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getContentHandler(): ContentHandler!
```

Return the current content handler.

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler)! | The current content handler, or null if none has been registered. |

**See Also**

- [#setContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setContentHandler(org.xml.sax.ContentHandler)) 

### getDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDTDHandler(): DTDHandler!
```

Return the current DTD handler.

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler)! | The current DTD handler, or null if none has been registered. |

**See Also**

- [#setDTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setDTDHandler(org.xml.sax.DTDHandler)) 

### getEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEntityResolver(): EntityResolver!
```

Return the current entity resolver.

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver)! | The current entity resolver, or null if none has been registered. |

**See Also**

- [#setEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setEntityResolver(org.xml.sax.EntityResolver)) 

### getErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getErrorHandler(): ErrorHandler!
```

Return the current error handler.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler)! | The current error handler, or null if none has been registered. |

**See Also**

- [#setErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setErrorHandler(org.xml.sax.ErrorHandler)) 

### getFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFeature(name: String!): Boolean
```

Look up the value of a feature flag.

The feature name is any fully-qualified URI. It is possible for an XMLReader to recognize a feature name but temporarily be unable to return its value. Some feature values may be available only in specific contexts, such as before, during, or after a parse. Also, some feature values may not be programmatically accessible. (In the case of an adapter for SAX1 [Parser](https://developer.android.com/reference/kotlin/org/xml/sax/Parser), there is no implementation-independent way to expose whether the underlying parser is performing validation, expanding external entities, and so forth.)

All XMLReaders are required to recognize the http://xml.org/sax/features/namespaces and the http://xml.org/sax/features/namespace-prefixes feature names.

Typical usage is something like this: 

```kotlin
XMLReader r = new MySAXDriver();
 
                          // try to activate validation
  try {
    r.setFeature("http://xml.org/sax/features/validation", true);
  } catch (SAXException e) {
    System.err.println("Cannot activate validation.");
  }
 
                          // register event handlers
  r.setContentHandler(new MyContentHandler());
  r.setErrorHandler(new MyErrorHandler());
 
                          // parse the first document
  try {
    r.parse("http://www.foo.com/mydoc.xml");
  } catch (IOException e) {
    System.err.println("I/O exception reading XML document");
  } catch (SAXException e) {
    System.err.println("XML exception reading document.");
  }
  
```

Implementors are free (and encouraged) to invent their own features, using names built on their own URIs.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The feature name, which is a fully-qualified URI. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The current value of the feature (true or false). |

| Exceptions ||
|-----------------------------------------|---------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the feature value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the XMLReader recognizes the feature name but cannot determine its value at this time. |

**See Also**

- [#setFeature](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setFeature(kotlin.String,%20kotlin.Boolean)) 

### getProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getProperty(name: String!): Any!
```

Look up the value of a property.

The property name is any fully-qualified URI. It is possible for an XMLReader to recognize a property name but temporarily be unable to return its value. Some property values may be available only in specific contexts, such as before, during, or after a parse.

XMLReaders are not required to recognize any specific property names, though an initial core set is documented for SAX2.

Implementors are free (and encouraged) to invent their own properties, using names built on their own URIs.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property name, which is a fully-qualified URI. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The current value of the property. |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the property value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the XMLReader recognizes the property name but cannot determine its value at this time. |

**See Also**

- [#setProperty](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setProperty(kotlin.String,%20kotlin.Any)) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parse(systemId: String!): Unit
```

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

- <https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#parse(org.xml.sax.InputSource)> 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parse(input: InputSource!): Unit
```

Parse an XML document.

The application can use this method to instruct the XML reader to begin parsing an XML document from any valid input source (a character stream, a byte stream, or a URI).

Applications may not invoke this method while a parse is in progress (they should create a new XMLReader instead for each nested XML document). Once a parse is complete, an application may reuse the same XMLReader object, possibly with a different input source. Configuration of the XMLReader object (such as handler bindings and values established for feature flags and properties) is unchanged by completion of a parse, unless the definition of that aspect of the configuration explicitly specifies other behavior. (For example, feature flags or properties exposing characteristics of the document being parsed.)

During the parse, the XMLReader will provide information about the XML document through the registered event handlers.

This method is synchronous: it will not return until parsing has ended. If a client application wants to terminate parsing early, it should throw an exception.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource)!:The input source for the top-level of the XML document. |

| Exceptions ||
|----------------------------|---------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |
| `java.io.IOException` | An IO exception from the parser, possibly from a byte stream or character stream supplied by the application. |

**See Also**

- [org.xml.sax.InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource)
- [#parse(java.lang.String)](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#parse(kotlin.String))
- [#setEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setEntityResolver(org.xml.sax.EntityResolver))
- [#setDTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setDTDHandler(org.xml.sax.DTDHandler))
- [#setContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setContentHandler(org.xml.sax.ContentHandler))
- [#setErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setErrorHandler(org.xml.sax.ErrorHandler)) 

### setContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setContentHandler(handler: ContentHandler!): Unit
```

Allow an application to register a content event handler.

If the application does not register a content handler, all content events reported by the SAX parser will be silently ignored.

Applications may register a new or different handler in the middle of a parse, and the SAX parser must begin using the new handler immediately.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------|
| `handler` | [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler)!:The content handler. |

**See Also**

- [#getContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getContentHandler()) 

### setDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDTDHandler(handler: DTDHandler!): Unit
```

Allow an application to register a DTD event handler.

If the application does not register a DTD handler, all DTD events reported by the SAX parser will be silently ignored.

Applications may register a new or different handler in the middle of a parse, and the SAX parser must begin using the new handler immediately.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `handler` | [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler)!:The DTD handler. |

**See Also**

- [#getDTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getDTDHandler()) 

### setEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEntityResolver(resolver: EntityResolver!): Unit
```

Allow an application to register an entity resolver.

If the application does not register an entity resolver, the XMLReader will perform its own default resolution.

Applications may register a new or different resolver in the middle of a parse, and the SAX parser must begin using the new resolver immediately.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------|
| `resolver` | [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver)!:The entity resolver. |

**See Also**

- [#getEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getEntityResolver()) 

### setErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setErrorHandler(handler: ErrorHandler!): Unit
```

Allow an application to register an error event handler.

If the application does not register an error handler, all error events reported by the SAX parser will be silently ignored; however, normal processing may not continue. It is highly recommended that all SAX applications implement an error handler to avoid unexpected bugs.

Applications may register a new or different handler in the middle of a parse, and the SAX parser must begin using the new handler immediately.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------|
| `handler` | [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler)!:The error handler. |

**See Also**

- [#getErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getErrorHandler()) 

### setFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFeature(
    name: String!, 
    value: Boolean
): Unit
```

Set the value of a feature flag.

The feature name is any fully-qualified URI. It is possible for an XMLReader to expose a feature value but to be unable to change the current value. Some feature values may be immutable or mutable only in specific contexts, such as before, during, or after a parse.

All XMLReaders are required to support setting http://xml.org/sax/features/namespaces to true and http://xml.org/sax/features/namespace-prefixes to false.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The feature name, which is a fully-qualified URI. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The requested value of the feature (true or false). |

| Exceptions ||
|-----------------------------------------|------------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the feature value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the XMLReader recognizes the feature name but cannot set the requested value. |

**See Also**

- [#getFeature](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getFeature(kotlin.String)) 

### setProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setProperty(
    name: String!, 
    value: Any!
): Unit
```

Set the value of a property.

The property name is any fully-qualified URI. It is possible for an XMLReader to recognize a property name but to be unable to change the current value. Some property values may be immutable or mutable only in specific contexts, such as before, during, or after a parse.

XMLReaders are not required to recognize setting any specific property names, though a core set is defined by SAX2.

This method is also the standard mechanism for setting extended handlers.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property name, which is a fully-qualified URI. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The requested value for the property. |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the property value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the XMLReader recognizes the property name but cannot set the requested value. |
