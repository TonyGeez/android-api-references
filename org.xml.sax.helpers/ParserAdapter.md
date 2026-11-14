# ParserAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParserAdapter

```
open class ParserAdapter : DocumentHandler, XMLReader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xml.sax.helpers.ParserAdapter](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#) |

Adapt a SAX1 Parser as a SAX2 XMLReader.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This class wraps a SAX1 [Parser](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#) and makes it act as a SAX2 [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#), with feature, property, and Namespace support. Note that it is not possible to report [skippedEntity](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#skippedEntity(kotlin.String))events, since SAX1 does not make that information available.

This adapter does not test for duplicate Namespace-qualified attribute names.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ParserAdapter](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#ParserAdapter())`()` Construct a new parser adapter. |
| [ParserAdapter](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#ParserAdapter(org.xml.sax.Parser))`(`parser:` ` [Parser](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#)!`)` Construct a new parser adapter. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [characters](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#characters(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adapter implementation method; do not call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endDocument](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#endDocument())`()` Adapter implementation method; do not call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endElement](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#endElement(kotlin.String))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adapter implementation method; do not call. |
| --- | --- |
| open [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)! | [getContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#getContentHandler())`()` Return the current content handler. |
| open [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#)! | [getDTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#getDTDHandler())`()` Return the current DTD handler. |
| open [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)! | [getEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#getEntityResolver())`()` Return the current entity resolver. |
| --- | --- |
| open [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)! | [getErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#getErrorHandler())`()` Return the current error handler. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#getFeature(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Check a parser feature flag. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getProperty](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#getProperty(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get a parser property. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ignorableWhitespace](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#ignorableWhitespace(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adapter implementation method; do not call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#parse(kotlin.String))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse an XML document. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#parse(org.xml.sax.InputSource))`(`input:` ` [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!`)` Parse an XML document. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [processingInstruction](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#processingInstruction(kotlin.String,%20kotlin.String))`(`target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adapter implementation method; do not call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#setContentHandler(org.xml.sax.ContentHandler))`(`handler:` ` [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)!`)` Set the content handler. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#setDTDHandler(org.xml.sax.DTDHandler))`(`handler:` ` [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#)!`)` Set the DTD handler. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentLocator](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#setDocumentLocator(org.xml.sax.Locator))`(`locator:` ` [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#)!`)` Adapter implementation method; do not call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#setEntityResolver(org.xml.sax.EntityResolver))`(`resolver:` ` [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)!`)` Set the entity resolver. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#setErrorHandler(org.xml.sax.ErrorHandler))`(`handler:` ` [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)!`)` Set the error handler. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#setFeature(kotlin.String,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set a feature flag for the parser. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#setProperty(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Set a parser property. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDocument](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#startDocument())`()` Adapter implementation method; do not call. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startElement](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#startElement(kotlin.String,%20org.xml.sax.AttributeList))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qAtts:` ` [AttributeList](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList.html#)!`)` Adapter implementation method; do not call. |

## Public constructors

### ParserAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ParserAdapter()
```

Construct a new parser adapter.

Use the "org.xml.sax.parser" property to locate the embedded SAX1 driver.

| Exceptions ||
|----------------------------|-------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | If the embedded driver cannot be instantiated or if the org.xml.sax.parser property is not specified. |

### ParserAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ParserAdapter(parser: Parser!)
```

Construct a new parser adapter.

Note that the embedded parser cannot be changed once the adapter is created; to embed a different parser, allocate a new ParserAdapter.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `parser` | [Parser](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#)!:The SAX1 parser to embed. |

| Exceptions ||
|----------------------------------|----------------------------------|
| `java.lang.NullPointerException` | If the parser parameter is null. |

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

Adapter implementation method; do not call. Adapt a SAX1 characters event.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:An array of characters. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The starting position in the array. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to use. |
| --- | --- |

| Exceptions ||
|----------------------------|----------------------------------------------|
| `org.xml.sax.SAXException` | The client may raise a processing exception. |

**See Also**

- [org.xml.sax.DocumentHandler#characters](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#characters(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)) 

### endDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endDocument(): Unit
```

Adapter implementation method; do not call. Adapt a SAX1 end document event.

| Exceptions ||
|----------------------------|----------------------------------------------|
| `org.xml.sax.SAXException` | The client may raise a processing exception. |

**See Also**

- [org.xml.sax.DocumentHandler#endDocument](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#endDocument()) 

### endElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endElement(qName: String!): Unit
```

Adapter implementation method; do not call. Adapt a SAX1 end element event.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `name` | The element type name |
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified (prefixed) name. |

| Exceptions ||
|----------------------------|----------------------------------------------|
| `org.xml.sax.SAXException` | The client may raise a processing exception. |

**See Also**

- [org.xml.sax.DocumentHandler#endElement](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#endElement(kotlin.String)) 

### getContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContentHandler(): ContentHandler!
```

Return the current content handler.

| Return ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)! | The current content handler, or null if none was supplied. |

**See Also**

- [org.xml.sax.XMLReader#getEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#getEntityResolver()) 

### getDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDTDHandler(): DTDHandler!
```

Return the current DTD handler.

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#)! | the current DTD handler, or null if none was supplied |

**See Also**

- [org.xml.sax.XMLReader#getEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#getEntityResolver()) 

### getEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEntityResolver(): EntityResolver!
```

Return the current entity resolver.

| Return ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)! | The current entity resolver, or null if none was supplied. |

**See Also**

- [org.xml.sax.XMLReader#getEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#getEntityResolver()) 

### getErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorHandler(): ErrorHandler!
```

Return the current error handler.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)! | The current error handler, or null if none was supplied. |

**See Also**

- [org.xml.sax.XMLReader#getEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#getEntityResolver()) 

### getFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFeature(name: String!): Boolean
```

Check a parser feature flag.

The only features recognized are namespaces and namespace-prefixes.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The feature name, as a complete URI. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The current feature value. |

| Exceptions ||
|-----------------------------------------|------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the feature value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | If the feature is not currently readable. |

**See Also**

- [org.xml.sax.XMLReader#setFeature](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#setFeature(kotlin.String,%20kotlin.Boolean)) 

### getProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProperty(name: String!): Any!
```

Get a parser property.

No properties are currently recognized.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property name. |

| Return ||
|-----------------------------------------------------------------------------|---------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The property value. |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the property value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | If the property value is not currently readable. |

**See Also**

- [org.xml.sax.XMLReader#getProperty](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#getProperty(kotlin.String)) 

### ignorableWhitespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ignorableWhitespace(
    ch: CharArray!, 
    start: Int, 
    length: Int
): Unit
```

Adapter implementation method; do not call. Adapt a SAX1 ignorable whitespace event.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:An array of characters. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The starting position in the array. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to use. |
| --- | --- |

| Exceptions ||
|----------------------------|----------------------------------------------|
| `org.xml.sax.SAXException` | The client may raise a processing exception. |

**See Also**

- [org.xml.sax.DocumentHandler#ignorableWhitespace](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#ignorableWhitespace(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(systemId: String!): Unit
```

Parse an XML document.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The absolute URL of the document. |

| Exceptions ||
|----------------------------|----------------------------------------------------------------|
| `java.io.IOException` | If there is a problem reading the raw content of the document. |
| `org.xml.sax.SAXException` | If there is a problem processing the document. |

**See Also**

- <https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#parse(org.xml.sax.InputSource)>
- [org.xml.sax.Parser#parse(java.lang.String)](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#parse(kotlin.String)) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(input: InputSource!): Unit
```

Parse an XML document.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `input` | [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!:An input source for the document. |

| Exceptions ||
|----------------------------|----------------------------------------------------------------|
| `java.io.IOException` | If there is a problem reading the raw content of the document. |
| `org.xml.sax.SAXException` | If there is a problem processing the document. |

**See Also**

- [#parse(java.lang.String)](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter#parse(kotlin.String))
- [org.xml.sax.Parser#parse(org.xml.sax.InputSource)](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#parse(org.xml.sax.InputSource)) 

### processingInstruction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun processingInstruction(
    target: String!, 
    data: String!
): Unit
```

Adapter implementation method; do not call. Adapt a SAX1 processing instruction event.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The processing instruction target. |
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The remainder of the processing instruction |

| Exceptions ||
|----------------------------|----------------------------------------------|
| `org.xml.sax.SAXException` | The client may raise a processing exception. |

**See Also**

- [org.xml.sax.DocumentHandler#processingInstruction](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#processingInstruction(kotlin.String,%20kotlin.String)) 

### setContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentHandler(handler: ContentHandler!): Unit
```

Set the content handler.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| `handler` | [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)!:the new content handler |

**See Also**

- [org.xml.sax.XMLReader#setEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#setEntityResolver(org.xml.sax.EntityResolver)) 

### setDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDTDHandler(handler: DTDHandler!): Unit
```

Set the DTD handler.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| `handler` | [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#)!:the new DTD handler |

**See Also**

- [org.xml.sax.XMLReader#setEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#setEntityResolver(org.xml.sax.EntityResolver)) 

### setDocumentLocator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDocumentLocator(locator: Locator!): Unit
```

Adapter implementation method; do not call. Adapt a SAX1 document locator event.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------|
| `locator` | [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#)!:A document locator. |

**See Also**

- [org.xml.sax.ContentHandler#setDocumentLocator](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#setDocumentLocator(org.xml.sax.Locator)) 

### setEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEntityResolver(resolver: EntityResolver!): Unit
```

Set the entity resolver.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------|
| `resolver` | [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)!:The new entity resolver. |

**See Also**

- [org.xml.sax.XMLReader#setEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#setEntityResolver(org.xml.sax.EntityResolver)) 

### setErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setErrorHandler(handler: ErrorHandler!): Unit
```

Set the error handler.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `handler` | [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)!:The new error handler. |

**See Also**

- [org.xml.sax.XMLReader#setEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#setEntityResolver(org.xml.sax.EntityResolver)) 

### setFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFeature(
    name: String!, 
    value: Boolean
): Unit
```

Set a feature flag for the parser.

The only features recognized are namespaces and namespace-prefixes.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The feature name, as a complete URI. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The requested feature value. |

| Exceptions ||
|-----------------------------------------|------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the feature can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | If the feature can't be assigned that value. |

**See Also**

- [org.xml.sax.XMLReader#setFeature](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#setFeature(kotlin.String,%20kotlin.Boolean)) 

### setProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProperty(
    name: String!, 
    value: Any!
): Unit
```

Set a parser property.

No properties are currently recognized.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property name. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The property value. |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the property value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | If the property can't be assigned that value. |

**See Also**

- [org.xml.sax.XMLReader#setProperty](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#setProperty(kotlin.String,%20kotlin.Any)) 

### startDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startDocument(): Unit
```

Adapter implementation method; do not call. Adapt a SAX1 start document event.

| Exceptions ||
|----------------------------|----------------------------------------------|
| `org.xml.sax.SAXException` | The client may raise a processing exception. |

**See Also**

- [org.xml.sax.DocumentHandler#startDocument](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#startDocument()) 

### startElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startElement(
    qName: String!, 
    qAtts: AttributeList!
): Unit
```

Adapter implementation method; do not call. Adapt a SAX1 startElement event.

If necessary, perform Namespace processing.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `name` | The element type name. |
| `atts` | The attributes attached to the element, if any. |
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified (prefixed) name. |
| --- | --- |
| `qAtts` | [AttributeList](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList.html#)!:The XML attribute list (with qnames). |

| Exceptions ||
|----------------------------|----------------------------------------------|
| `org.xml.sax.SAXException` | The client may raise a processing exception. |
