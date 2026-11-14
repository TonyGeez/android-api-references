# XMLFilterImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XMLFilterImpl

```
open class XMLFilterImpl : ContentHandler, DTDHandler, EntityResolver, ErrorHandler, XMLFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [org.xml.sax.helpers.XMLFilterImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#) |

Base class for deriving an XML filter.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This class is designed to sit between an [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#) and the client application's event handlers. By default, it does nothing but pass requests up to the reader and events on to the handlers unmodified, but subclasses can override specific methods to modify the event stream or the configuration requests as they pass through.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [XMLFilterImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#XMLFilterImpl())`()` Construct an empty XML filter, with no parent. |
| [XMLFilterImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#XMLFilterImpl(org.xml.sax.XMLReader))`(`parent:` ` [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#)!`)` Construct an XML filter with the specified parent. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [characters](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#characters(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Filter a character data event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endDocument](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#endDocument())`()` Filter an end document event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endElement](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#endElement(kotlin.String,%20kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Filter an end element event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endPrefixMapping](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#endPrefixMapping(kotlin.String))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Filter an end Namespace prefix mapping event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [error](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#error(org.xml.sax.SAXParseException))`(`e:` ` [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException.html#)!`)` Filter an error event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fatalError](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#fatalError(org.xml.sax.SAXParseException))`(`e:` ` [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException.html#)!`)` Filter a fatal error event. |
| open [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)! | [getContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#getContentHandler())`()` Get the content event handler. |
| open [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#)! | [getDTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#getDTDHandler())`()` Get the current DTD event handler. |
| open [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)! | [getEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#getEntityResolver())`()` Get the current entity resolver. |
| open [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)! | [getErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#getErrorHandler())`()` Get the current error event handler. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#getFeature(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a feature. |
| open [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#)! | [getParent](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#getParent())`()` Get the parent reader. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getProperty](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#getProperty(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a property. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ignorableWhitespace](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#ignorableWhitespace(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Filter an ignorable whitespace event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notationDecl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#notationDecl(kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Filter a notation declaration event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#parse(kotlin.String))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse a document. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#parse(org.xml.sax.InputSource))`(`input:` ` [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!`)` Parse a document. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [processingInstruction](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#processingInstruction(kotlin.String,%20kotlin.String))`(`target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Filter a processing instruction event. |
| open [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)! | [resolveEntity](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#resolveEntity(kotlin.String,%20kotlin.String))`(`publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Filter an external entity resolution. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#setContentHandler(org.xml.sax.ContentHandler))`(`handler:` ` [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)!`)` Set the content event handler. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#setDTDHandler(org.xml.sax.DTDHandler))`(`handler:` ` [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#)!`)` Set the DTD event handler. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentLocator](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#setDocumentLocator(org.xml.sax.Locator))`(`locator:` ` [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#)!`)` Filter a new document locator event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#setEntityResolver(org.xml.sax.EntityResolver))`(`resolver:` ` [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)!`)` Set the entity resolver. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#setErrorHandler(org.xml.sax.ErrorHandler))`(`handler:` ` [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)!`)` Set the error event handler. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#setFeature(kotlin.String,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the value of a feature. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParent](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#setParent(org.xml.sax.XMLReader))`(`parent:` ` [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#)!`)` Set the parent reader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#setProperty(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Set the value of a property. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skippedEntity](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#skippedEntity(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Filter a skipped entity event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDocument](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#startDocument())`()` Filter a start document event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startElement](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#startElement(kotlin.String,%20kotlin.String,%20kotlin.String,%20org.xml.sax.Attributes))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `atts:` ` [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#)!`)` Filter a start element event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startPrefixMapping](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#startPrefixMapping(kotlin.String,%20kotlin.String))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Filter a start Namespace prefix mapping event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unparsedEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#unparsedEntityDecl(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `notationName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Filter an unparsed entity declaration event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [warning](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#warning(org.xml.sax.SAXParseException))`(`e:` ` [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException.html#)!`)` Filter a warning event. |

## Public constructors

### XMLFilterImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
XMLFilterImpl()
```

Construct an empty XML filter, with no parent.

This filter will have no parent: you must assign a parent before you start a parse or do any configuration with setFeature or setProperty, unless you use this as a pure event consumer rather than as an [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#). 
**See Also**

- [org.xml.sax.XMLReader#setFeature](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#setFeature(kotlin.String,%20kotlin.Boolean))
- [org.xml.sax.XMLReader#setProperty](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#setProperty(kotlin.String,%20kotlin.Any))
- [#setParent](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#setParent(org.xml.sax.XMLReader)) 

### XMLFilterImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
XMLFilterImpl(parent: XMLReader!)
```

Construct an XML filter with the specified parent.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#)!:the XML reader from which this filter receives its events. |

**See Also**

- [#setParent](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#setParent(org.xml.sax.XMLReader))
- [#getParent](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#getParent())

## Public methods

### characters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun characters(
    ch: CharArray!, 
    start: Int, 
    length: Int
): Unit
```

Filter a character data event.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:An array of characters. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The starting position in the array. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to use from the array. |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |

### endDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endDocument(): Unit
```

Filter an end document event.

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |

### endElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endElement(
    uri: String!, 
    localName: String!, 
    qName: String!
): Unit
```

Filter an end element event.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The element's Namespace URI, or the empty string. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The element's local name, or the empty string. |
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The element's qualified (prefixed) name, or the empty string. |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |

### endPrefixMapping

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endPrefixMapping(prefix: String!): Unit
```

Filter an end Namespace prefix mapping event.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace prefix. |

| Exceptions ||
|----------------------------|------------------------------------------------------|
| `org.xml.sax.SAXException` | the client may throw an exception during processing |
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |

### error

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun error(e: SAXParseException!): Unit
```

Filter an error event.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | The error information encapsulated in a SAX parse exception. |
| `e` | [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException.html#)!:The error as an exception. |

| Exceptions ||
|----------------------------|------------------------------------------------------|
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |

### fatalError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fatalError(e: SAXParseException!): Unit
```

Filter a fatal error event.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | The error information encapsulated in a SAX parse exception. |
| `e` | [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException.html#)!:The error as an exception. |

| Exceptions ||
|----------------------------|------------------------------------------------------|
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |

### getContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContentHandler(): ContentHandler!
```

Get the content event handler.

| Return ||
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)! | The current content handler, or null if none was set. |

### getDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDTDHandler(): DTDHandler!
```

Get the current DTD event handler.

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------|
| [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#)! | The current DTD handler, or null if none was set. |

### getEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEntityResolver(): EntityResolver!
```

Get the current entity resolver.

| Return ||
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)! | The current entity resolver, or null if none was set. |

### getErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorHandler(): ErrorHandler!
```

Get the current error event handler.

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)! | The current error handler, or null if none was set. |

### getFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFeature(name: String!): Boolean
```

Look up the value of a feature.

This will always fail if the parent is null.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The feature name. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The current value of the feature. |

| Exceptions ||
|-----------------------------------------|------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the feature value can't be assigned or retrieved from the parent. |
| `org.xml.sax.SAXNotSupportedException` | When the parent recognizes the feature name but cannot determine its value at this time. |

### getParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParent(): XMLReader!
```

Get the parent reader.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------|
| [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#)! | The parent XML reader, or null if none is set. |

**See Also**

- [#setParent](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#setParent(org.xml.sax.XMLReader)) 

### getProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProperty(name: String!): Any!
```

Look up the value of a property.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property name. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The current value of the property. |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the property value can't be assigned or retrieved from the parent. |
| `org.xml.sax.SAXNotSupportedException` | When the parent recognizes the property name but cannot determine its value at this time. |

### ignorableWhitespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ignorableWhitespace(
    ch: CharArray!, 
    start: Int, 
    length: Int
): Unit
```

Filter an ignorable whitespace event.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:An array of characters. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The starting position in the array. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to use from the array. |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |

### notationDecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notationDecl(
    name: String!, 
    publicId: String!, 
    systemId: String!
): Unit
```

Filter a notation declaration event.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The notation name. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The notation's public identifier, or null. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The notation's system identifier, or null. |

| Exceptions ||
|----------------------------|------------------------------------------------------|
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(systemId: String!): Unit
```

Parse a document.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier as a fully-qualified URI. |

| Exceptions ||
|----------------------------|---------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |
| `java.io.IOException` | An IO exception from the parser, possibly from a byte stream or character stream supplied by the application. |

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(input: InputSource!): Unit
```

Parse a document.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!:The input source for the document entity. |

| Exceptions ||
|----------------------------|---------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |
| `java.io.IOException` | An IO exception from the parser, possibly from a byte stream or character stream supplied by the application. |

### processingInstruction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun processingInstruction(
    target: String!, 
    data: String!
): Unit
```

Filter a processing instruction event.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The processing instruction target. |
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The text following the target. |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |

### resolveEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resolveEntity(
    publicId: String!, 
    systemId: String!
): InputSource!
```

Filter an external entity resolution.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity's public identifier, or null. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity's system identifier. |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)! | A new InputSource or null for the default. |

| Exceptions ||
|----------------------------|------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |
| `java.io.IOException` | The client may throw an I/O-related exception while obtaining the new InputSource. |

### setContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentHandler(handler: ContentHandler!): Unit
```

Set the content event handler.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| `handler` | [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)!:the new content handler |

### setDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDTDHandler(handler: DTDHandler!): Unit
```

Set the DTD event handler.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| `handler` | [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#)!:the new DTD handler |

### setDocumentLocator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDocumentLocator(locator: Locator!): Unit
```

Filter a new document locator event.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------|
| `locator` | [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#)!:The document locator. |

### setEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEntityResolver(resolver: EntityResolver!): Unit
```

Set the entity resolver.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------|
| `resolver` | [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)!:The new entity resolver. |

### setErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setErrorHandler(handler: ErrorHandler!): Unit
```

Set the error event handler.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------|
| `handler` | [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)!:the new error handler |

### setFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFeature(
    name: String!, 
    value: Boolean
): Unit
```

Set the value of a feature.

This will always fail if the parent is null.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The feature name. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The requested feature value. |

| Exceptions ||
|-----------------------------------------|---------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the feature value can't be assigned or retrieved from the parent. |
| `org.xml.sax.SAXNotSupportedException` | When the parent recognizes the feature name but cannot set the requested value. |

### setParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParent(parent: XMLReader!): Unit
```

Set the parent reader.

This is the [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#) from which this filter will obtain its events and to which it will pass its configuration requests. The parent may itself be another filter.

If there is no parent reader set, any attempt to parse or to set or get a feature or property will fail.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------|
| `parent` | [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#)!:The parent XML reader. |

**See Also**

- [#getParent](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl#getParent()) 

### setProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProperty(
    name: String!, 
    value: Any!
): Unit
```

Set the value of a property.

This will always fail if the parent is null.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property name. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The requested property value. |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the property value can't be assigned or retrieved from the parent. |
| `org.xml.sax.SAXNotSupportedException` | When the parent recognizes the property name but cannot set the requested value. |

### skippedEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skippedEntity(name: String!): Unit
```

Filter a skipped entity event.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the skipped entity. |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |

### startDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startDocument(): Unit
```

Filter a start document event.

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |

### startElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startElement(
    uri: String!, 
    localName: String!, 
    qName: String!, 
    atts: Attributes!
): Unit
```

Filter a start element event.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The element's Namespace URI, or the empty string. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The element's local name, or the empty string. |
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The element's qualified (prefixed) name, or the empty string. |
| `atts` | [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#)!:The element's attributes. |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |

### startPrefixMapping

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startPrefixMapping(
    prefix: String!, 
    uri: String!
): Unit
```

Filter a start Namespace prefix mapping event.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace prefix. |
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI. |

| Exceptions ||
|----------------------------|------------------------------------------------------|
| `org.xml.sax.SAXException` | the client may throw an exception during processing |
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |

### unparsedEntityDecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unparsedEntityDecl(
    name: String!, 
    publicId: String!, 
    systemId: String!, 
    notationName: String!
): Unit
```

Filter an unparsed entity declaration event.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity name. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity's public identifier, or null. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity's system identifier, or null. |
| `notationName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the associated notation. |

| Exceptions ||
|----------------------------|------------------------------------------------------|
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |

### warning

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun warning(e: SAXParseException!): Unit
```

Filter a warning event.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | The warning information encapsulated in a SAX parse exception. |
| `e` | [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException.html#)!:The warning as an exception. |

| Exceptions ||
|----------------------------|------------------------------------------------------|
| `org.xml.sax.SAXException` | The client may throw an exception during processing. |
