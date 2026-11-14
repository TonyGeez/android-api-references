Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XMLFilter

```
interface XMLFilter : XMLReader
```

| [org.xml.sax.XMLFilter](../org/xml/sax/XMLFilter.md) |

| Known Direct Subclasses [XMLFilterImpl](../org/xml/sax/helpers/XMLFilterImpl.md) |---|---| | [XMLFilterImpl](../org/xml/sax/helpers/XMLFilterImpl.md) | Base class for deriving an XML filter. | |
| --- | --- | --- | --- | --- | --- | --- |

Interface for an XML filter. *This module, both source code and documentation, is in the Public Domain, and comes with **NO WARRANTY**.* See <http://www.saxproject.org> for further information.

An XML filter is like an XML reader, except that it obtains its events from another XML reader rather than a primary source like an XML document or database. Filters can modify a stream of events as they pass on to the final application.

The XMLFilterImpl helper class provides a convenient base for creating SAX2 filters, by passing on all `https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver`, `https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler`, `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler` and `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler` events automatically.

## Summary

| Public methods ||
|---|---|
| abstract [XMLReader](../org/xml/sax/XMLReader.md)! | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLFilter#getParent()()` Get the parent reader. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLFilter#setParent(org.xml.sax.XMLReader)(parent: https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader!)` Set the parent reader. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader` |---|---| | `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler!` | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getContentHandler()()` Return the current content handler. <br /> | | `https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler!` | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getDTDHandler()()` Return the current DTD handler. <br /> | | `https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver!` | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getEntityResolver()()` Return the current entity resolver. <br /> | | `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler!` | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getErrorHandler()()` Return the current error handler. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getFeature(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Look up the value of a feature flag. The feature name is any fully-qualified URI. It is possible for an XMLReader to recognize a feature name but temporarily be unable to return its value. Some feature values may be available only in specific contexts, such as before, during, or after a parse. Also, some feature values may not be programmatically accessible. (In the case of an adapter for SAX1 `https://developer.android.com/reference/kotlin/org/xml/sax/Parser`, there is no implementation-independent way to expose whether the underlying parser is performing validation, expanding external entities, and so forth.) All XMLReaders are required to recognize the http://xml.org/sax/features/namespaces and the http://xml.org/sax/features/namespace-prefixes feature names. Typical usage is something like this: ```kotlin XMLReader r = new MySAXDriver(); // try to activate validation try { r.setFeature("http://xml.org/sax/features/validation", true); } catch (SAXException e) { System.err.println("Cannot activate validation."); } // register event handlers r.setContentHandler(new MyContentHandler()); r.setErrorHandler(new MyErrorHandler()); // parse the first document try { r.parse("http://www.foo.com/mydoc.xml"); } catch (IOException e) { System.err.println("I/O exception reading XML document"); } catch (SAXException e) { System.err.println("XML exception reading document."); } ``` Implementors are free (and encouraged) to invent their own features, using names built on their own URIs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#getProperty(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Look up the value of a property. The property name is any fully-qualified URI. It is possible for an XMLReader to recognize a property name but temporarily be unable to return its value. Some property values may be available only in specific contexts, such as before, during, or after a parse. XMLReaders are not required to recognize any specific property names, though an initial core set is documented for SAX2. Implementors are free (and encouraged) to invent their own properties, using names built on their own URIs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#parse(kotlin.String)(systemId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Parse an XML document from a system identifier (URI). This method is a shortcut for the common case of reading a document from a system identifier. It is the exact equivalent of the following: ```kotlin parse(new InputSource(systemId)); ``` If the system identifier is a URL, it must be fully resolved by the application before it is passed to the parser. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#parse(org.xml.sax.InputSource)(input: https://developer.android.com/reference/kotlin/org/xml/sax/InputSource!)` Parse an XML document. The application can use this method to instruct the XML reader to begin parsing an XML document from any valid input source (a character stream, a byte stream, or a URI). Applications may not invoke this method while a parse is in progress (they should create a new XMLReader instead for each nested XML document). Once a parse is complete, an application may reuse the same XMLReader object, possibly with a different input source. Configuration of the XMLReader object (such as handler bindings and values established for feature flags and properties) is unchanged by completion of a parse, unless the definition of that aspect of the configuration explicitly specifies other behavior. (For example, feature flags or properties exposing characteristics of the document being parsed.) During the parse, the XMLReader will provide information about the XML document through the registered event handlers. This method is synchronous: it will not return until parsing has ended. If a client application wants to terminate parsing early, it should throw an exception. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setContentHandler(org.xml.sax.ContentHandler)(handler: https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler!)` Allow an application to register a content event handler. If the application does not register a content handler, all content events reported by the SAX parser will be silently ignored. Applications may register a new or different handler in the middle of a parse, and the SAX parser must begin using the new handler immediately. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setDTDHandler(org.xml.sax.DTDHandler)(handler: https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler!)` Allow an application to register a DTD event handler. If the application does not register a DTD handler, all DTD events reported by the SAX parser will be silently ignored. Applications may register a new or different handler in the middle of a parse, and the SAX parser must begin using the new handler immediately. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setEntityResolver(org.xml.sax.EntityResolver)(resolver: https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver!)` Allow an application to register an entity resolver. If the application does not register an entity resolver, the XMLReader will perform its own default resolution. Applications may register a new or different resolver in the middle of a parse, and the SAX parser must begin using the new resolver immediately. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setErrorHandler(org.xml.sax.ErrorHandler)(handler: https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler!)` Allow an application to register an error event handler. If the application does not register an error handler, all error events reported by the SAX parser will be silently ignored; however, normal processing may not continue. It is highly recommended that all SAX applications implement an error handler to avoid unexpected bugs. Applications may register a new or different handler in the middle of a parse, and the SAX parser must begin using the new handler immediately. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setFeature(kotlin.String,%20kotlin.Boolean)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set the value of a feature flag. The feature name is any fully-qualified URI. It is possible for an XMLReader to expose a feature value but to be unable to change the current value. Some feature values may be immutable or mutable only in specific contexts, such as before, during, or after a parse. All XMLReaders are required to support setting http://xml.org/sax/features/namespaces to true and http://xml.org/sax/features/namespace-prefixes to false. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setProperty(kotlin.String,%20kotlin.Any)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Set the value of a property. The property name is any fully-qualified URI. It is possible for an XMLReader to recognize a property name but to be unable to change the current value. Some property values may be immutable or mutable only in specific contexts, such as before, during, or after a parse. XMLReaders are not required to recognize setting any specific property names, though a core set is defined by SAX2. This method is also the standard mechanism for setting extended handlers. <br /> | ||

## Public methods

### getParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getParent(): XMLReader!
```

Get the parent reader.

This method allows the application to query the parent reader (which may be another filter). It is generally a bad idea to perform any operations on the parent reader directly: they should all pass through this filter.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader!` | The parent filter, or null if none has been set. |

### setParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setParent(parent: XMLReader!): Unit
```

Set the parent reader.

This method allows the application to link the filter to a parent reader (which may be another filter). The argument may not be null.

| Parameters ||
|---|---|
| `parent` | [XMLReader](../org/xml/sax/XMLReader.md)!: The parent reader. |
