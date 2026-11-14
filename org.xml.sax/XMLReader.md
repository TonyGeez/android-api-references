# XMLReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XMLReader

```
interface XMLReader
```

| [org.xml.sax.XMLReader](../org/xml/sax/XMLReader.md) |

| Known Direct Subclasses [Driver](../org/xmlpull/v1/sax2/Driver.md), [ParserAdapter](../org/xml/sax/helpers/ParserAdapter.md), [XMLFilter](../org/xml/sax/XMLFilter.md) |---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------| | [Driver](../org/xmlpull/v1/sax2/Driver.md) | SAX2 Driver that pulls events from XmlPullParser and converts them into SAX2 callbacks. | | [ParserAdapter](../org/xml/sax/helpers/ParserAdapter.md) | Adapt a SAX1 Parser as a SAX2 XMLReader. | | [XMLFilter](../org/xml/sax/XMLFilter.md) | Interface for an XML filter. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [XMLFilterImpl](../org/xml/sax/helpers/XMLFilterImpl.md) |---------------------------------------------------------------------------------------------------|----------------------------------------| | [XMLFilterImpl](../org/xml/sax/helpers/XMLFilterImpl.md) | Base class for deriving an XML filter. | |
| --- | --- | --- | --- | --- | --- | --- |

Interface for reading an XML document using callbacks.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

**Note:** despite its name, this interface does*not* extend the standard Java [Reader](../java/io/Reader.md) interface, because reading XML is a fundamentally different activity than reading character data.

XMLReader is the interface that an XML parser's SAX2 driver must implement. This interface allows an application to set and query features and properties in the parser, to register event handlers for document processing, and to initiate a document parse.

All SAX interfaces are assumed to be synchronous: the #parse methods must not return until parsing is complete, and readers must wait for an event-handler callback to return before reporting the next event.

This interface replaces the (now deprecated) SAX 1.0 interface. The XMLReader interface contains two important enhancements over the old Parser interface (as well as some minor ones):

1. it adds a standard way to query and set features and properties; and
2. it adds Namespace support, which is required for many higher-level XML standards.

There are adapters available to convert a SAX1 Parser to a SAX2 XMLReader and vice-versa.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ContentHandler](../org/xml/sax/ContentHandler.md)! | [getContentHandler](../org/xml/sax/XMLReader.md))`()` Return the current content handler. |
| abstract [DTDHandler](../org/xml/sax/DTDHandler.md)! | [getDTDHandler](../org/xml/sax/XMLReader.md))`()` Return the current DTD handler. |
| abstract [EntityResolver](../org/xml/sax/EntityResolver.md)! | [getEntityResolver](../org/xml/sax/XMLReader.md))`()` Return the current entity resolver. |
| --- | --- |
| abstract [ErrorHandler](../org/xml/sax/ErrorHandler.md)! | [getErrorHandler](../org/xml/sax/XMLReader.md))`()` Return the current error handler. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](../org/xml/sax/XMLReader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a feature flag. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getProperty](../org/xml/sax/XMLReader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a property. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](../org/xml/sax/XMLReader.md))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse an XML document from a system identifier (URI). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](../org/xml/sax/XMLReader.md))`(`input:` ` [InputSource](../org/xml/sax/InputSource.md)!`)` Parse an XML document. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentHandler](../org/xml/sax/XMLReader.md))`(`handler:` ` [ContentHandler](../org/xml/sax/ContentHandler.md)!`)` Allow an application to register a content event handler. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDTDHandler](../org/xml/sax/XMLReader.md))`(`handler:` ` [DTDHandler](../org/xml/sax/DTDHandler.md)!`)` Allow an application to register a DTD event handler. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntityResolver](../org/xml/sax/XMLReader.md))`(`resolver:` ` [EntityResolver](../org/xml/sax/EntityResolver.md)!`)` Allow an application to register an entity resolver. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](../org/xml/sax/XMLReader.md))`(`handler:` ` [ErrorHandler](../org/xml/sax/ErrorHandler.md)!`)` Allow an application to register an error event handler. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](../org/xml/sax/XMLReader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the value of a feature flag. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](../org/xml/sax/XMLReader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Set the value of a property. |

## Public methods

### getContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getContentHandler(): ContentHandler!
```

Return the current content handler.

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [ContentHandler](../org/xml/sax/ContentHandler.md)! | The current content handler, or null if none has been registered. |

**See Also**

- [#setContentHandler](../org/xml/sax/XMLReader.md)) 

### getDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDTDHandler(): DTDHandler!
```

Return the current DTD handler.

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [DTDHandler](../org/xml/sax/DTDHandler.md)! | The current DTD handler, or null if none has been registered. |

**See Also**

- [#setDTDHandler](../org/xml/sax/XMLReader.md)) 

### getEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEntityResolver(): EntityResolver!
```

Return the current entity resolver.

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [EntityResolver](../org/xml/sax/EntityResolver.md)! | The current entity resolver, or null if none has been registered. |

**See Also**

- [#setEntityResolver](../org/xml/sax/XMLReader.md)) 

### getErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getErrorHandler(): ErrorHandler!
```

Return the current error handler.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [ErrorHandler](../org/xml/sax/ErrorHandler.md)! | The current error handler, or null if none has been registered. |

**See Also**

- [#setErrorHandler](../org/xml/sax/XMLReader.md)) 

### getFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFeature(name: String!): Boolean
```

Look up the value of a feature flag.

The feature name is any fully-qualified URI. It is possible for an XMLReader to recognize a feature name but temporarily be unable to return its value. Some feature values may be available only in specific contexts, such as before, during, or after a parse. Also, some feature values may not be programmatically accessible. (In the case of an adapter for SAX1 [Parser](../org/xml/sax/Parser.md), there is no implementation-independent way to expose whether the underlying parser is performing validation, expanding external entities, and so forth.)

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

- [#setFeature](../org/xml/sax/XMLReader.md)) 

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

- [#setProperty](../org/xml/sax/XMLReader.md)) 

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
| `input` | [InputSource](../org/xml/sax/InputSource.md)!:The input source for the top-level of the XML document. |

| Exceptions ||
|----------------------------|---------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |
| `java.io.IOException` | An IO exception from the parser, possibly from a byte stream or character stream supplied by the application. |

**See Also**

- [org.xml.sax.InputSource](../org/xml/sax/InputSource.md)
- [#parse(java.lang.String)](../org/xml/sax/XMLReader.md))
- [#setEntityResolver](../org/xml/sax/XMLReader.md))
- [#setDTDHandler](../org/xml/sax/XMLReader.md))
- [#setContentHandler](../org/xml/sax/XMLReader.md))
- [#setErrorHandler](../org/xml/sax/XMLReader.md)) 

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
| `handler` | [ContentHandler](../org/xml/sax/ContentHandler.md)!:The content handler. |

**See Also**

- [#getContentHandler](../org/xml/sax/XMLReader.md)) 

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
| `handler` | [DTDHandler](../org/xml/sax/DTDHandler.md)!:The DTD handler. |

**See Also**

- [#getDTDHandler](../org/xml/sax/XMLReader.md)) 

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
| `resolver` | [EntityResolver](../org/xml/sax/EntityResolver.md)!:The entity resolver. |

**See Also**

- [#getEntityResolver](../org/xml/sax/XMLReader.md)) 

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
| `handler` | [ErrorHandler](../org/xml/sax/ErrorHandler.md)!:The error handler. |

**See Also**

- [#getErrorHandler](../org/xml/sax/XMLReader.md)) 

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

- [#getFeature](../org/xml/sax/XMLReader.md)) 

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
