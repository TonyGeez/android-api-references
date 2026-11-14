# ParserAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParserAdapter

```
open class ParserAdapter : DocumentHandler, XMLReader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xml.sax.helpers.ParserAdapter](../org/xml/sax/helpers/ParserAdapter.md) |

Adapt a SAX1 Parser as a SAX2 XMLReader.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This class wraps a SAX1 [Parser](../org/xml/sax/Parser.md) and makes it act as a SAX2 [XMLReader](../org/xml/sax/XMLReader.md), with feature, property, and Namespace support. Note that it is not possible to report [skippedEntity](../org/xml/sax/ContentHandler.md))events, since SAX1 does not make that information available.

This adapter does not test for duplicate Namespace-qualified attribute names.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ParserAdapter](../org/xml/sax/helpers/ParserAdapter.md))`()` Construct a new parser adapter. |
| [ParserAdapter](../org/xml/sax/helpers/ParserAdapter.md))`(`parser:` ` [Parser](../org/xml/sax/Parser.md)!`)` Construct a new parser adapter. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [characters](../org/xml/sax/helpers/ParserAdapter.md))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adapter implementation method; do not call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endDocument](../org/xml/sax/helpers/ParserAdapter.md))`()` Adapter implementation method; do not call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endElement](../org/xml/sax/helpers/ParserAdapter.md))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adapter implementation method; do not call. |
| --- | --- |
| open [ContentHandler](../org/xml/sax/ContentHandler.md)! | [getContentHandler](../org/xml/sax/helpers/ParserAdapter.md))`()` Return the current content handler. |
| open [DTDHandler](../org/xml/sax/DTDHandler.md)! | [getDTDHandler](../org/xml/sax/helpers/ParserAdapter.md))`()` Return the current DTD handler. |
| open [EntityResolver](../org/xml/sax/EntityResolver.md)! | [getEntityResolver](../org/xml/sax/helpers/ParserAdapter.md))`()` Return the current entity resolver. |
| --- | --- |
| open [ErrorHandler](../org/xml/sax/ErrorHandler.md)! | [getErrorHandler](../org/xml/sax/helpers/ParserAdapter.md))`()` Return the current error handler. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](../org/xml/sax/helpers/ParserAdapter.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Check a parser feature flag. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getProperty](../org/xml/sax/helpers/ParserAdapter.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get a parser property. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ignorableWhitespace](../org/xml/sax/helpers/ParserAdapter.md))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adapter implementation method; do not call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](../org/xml/sax/helpers/ParserAdapter.md))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse an XML document. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](../org/xml/sax/helpers/ParserAdapter.md))`(`input:` ` [InputSource](../org/xml/sax/InputSource.md)!`)` Parse an XML document. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [processingInstruction](../org/xml/sax/helpers/ParserAdapter.md))`(`target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adapter implementation method; do not call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentHandler](../org/xml/sax/helpers/ParserAdapter.md))`(`handler:` ` [ContentHandler](../org/xml/sax/ContentHandler.md)!`)` Set the content handler. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDTDHandler](../org/xml/sax/helpers/ParserAdapter.md))`(`handler:` ` [DTDHandler](../org/xml/sax/DTDHandler.md)!`)` Set the DTD handler. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentLocator](../org/xml/sax/helpers/ParserAdapter.md))`(`locator:` ` [Locator](../org/xml/sax/Locator.md)!`)` Adapter implementation method; do not call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntityResolver](../org/xml/sax/helpers/ParserAdapter.md))`(`resolver:` ` [EntityResolver](../org/xml/sax/EntityResolver.md)!`)` Set the entity resolver. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](../org/xml/sax/helpers/ParserAdapter.md))`(`handler:` ` [ErrorHandler](../org/xml/sax/ErrorHandler.md)!`)` Set the error handler. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](../org/xml/sax/helpers/ParserAdapter.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set a feature flag for the parser. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](../org/xml/sax/helpers/ParserAdapter.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Set a parser property. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDocument](../org/xml/sax/helpers/ParserAdapter.md))`()` Adapter implementation method; do not call. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startElement](../org/xml/sax/helpers/ParserAdapter.md))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qAtts:` ` [AttributeList](../org/xml/sax/AttributeList.md)!`)` Adapter implementation method; do not call. |

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
| `parser` | [Parser](../org/xml/sax/Parser.md)!:The SAX1 parser to embed. |

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

- [org.xml.sax.DocumentHandler#characters](../org/xml/sax/DocumentHandler.md)) 

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

- [org.xml.sax.DocumentHandler#endDocument](../org/xml/sax/DocumentHandler.md)) 

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

- [org.xml.sax.DocumentHandler#endElement](../org/xml/sax/DocumentHandler.md)) 

### getContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContentHandler(): ContentHandler!
```

Return the current content handler.

| Return ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [ContentHandler](../org/xml/sax/ContentHandler.md)! | The current content handler, or null if none was supplied. |

**See Also**

- [org.xml.sax.XMLReader#getEntityResolver](../org/xml/sax/XMLReader.md)) 

### getDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDTDHandler(): DTDHandler!
```

Return the current DTD handler.

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [DTDHandler](../org/xml/sax/DTDHandler.md)! | the current DTD handler, or null if none was supplied |

**See Also**

- [org.xml.sax.XMLReader#getEntityResolver](../org/xml/sax/XMLReader.md)) 

### getEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEntityResolver(): EntityResolver!
```

Return the current entity resolver.

| Return ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [EntityResolver](../org/xml/sax/EntityResolver.md)! | The current entity resolver, or null if none was supplied. |

**See Also**

- [org.xml.sax.XMLReader#getEntityResolver](../org/xml/sax/XMLReader.md)) 

### getErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorHandler(): ErrorHandler!
```

Return the current error handler.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [ErrorHandler](../org/xml/sax/ErrorHandler.md)! | The current error handler, or null if none was supplied. |

**See Also**

- [org.xml.sax.XMLReader#getEntityResolver](../org/xml/sax/XMLReader.md)) 

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

- [org.xml.sax.XMLReader#setFeature](../org/xml/sax/XMLReader.md)) 

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

- [org.xml.sax.XMLReader#getProperty](../org/xml/sax/XMLReader.md)) 

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

- [org.xml.sax.DocumentHandler#ignorableWhitespace](../org/xml/sax/DocumentHandler.md)) 

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
- [org.xml.sax.Parser#parse(java.lang.String)](../org/xml/sax/Parser.md)) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(input: InputSource!): Unit
```

Parse an XML document.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `input` | [InputSource](../org/xml/sax/InputSource.md)!:An input source for the document. |

| Exceptions ||
|----------------------------|----------------------------------------------------------------|
| `java.io.IOException` | If there is a problem reading the raw content of the document. |
| `org.xml.sax.SAXException` | If there is a problem processing the document. |

**See Also**

- [#parse(java.lang.String)](../org/xml/sax/helpers/ParserAdapter.md))
- [org.xml.sax.Parser#parse(org.xml.sax.InputSource)](../org/xml/sax/Parser.md)) 

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

- [org.xml.sax.DocumentHandler#processingInstruction](../org/xml/sax/DocumentHandler.md)) 

### setContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentHandler(handler: ContentHandler!): Unit
```

Set the content handler.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| `handler` | [ContentHandler](../org/xml/sax/ContentHandler.md)!:the new content handler |

**See Also**

- [org.xml.sax.XMLReader#setEntityResolver](../org/xml/sax/XMLReader.md)) 

### setDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDTDHandler(handler: DTDHandler!): Unit
```

Set the DTD handler.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| `handler` | [DTDHandler](../org/xml/sax/DTDHandler.md)!:the new DTD handler |

**See Also**

- [org.xml.sax.XMLReader#setEntityResolver](../org/xml/sax/XMLReader.md)) 

### setDocumentLocator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDocumentLocator(locator: Locator!): Unit
```

Adapter implementation method; do not call. Adapt a SAX1 document locator event.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------|
| `locator` | [Locator](../org/xml/sax/Locator.md)!:A document locator. |

**See Also**

- [org.xml.sax.ContentHandler#setDocumentLocator](../org/xml/sax/ContentHandler.md)) 

### setEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEntityResolver(resolver: EntityResolver!): Unit
```

Set the entity resolver.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------|
| `resolver` | [EntityResolver](../org/xml/sax/EntityResolver.md)!:The new entity resolver. |

**See Also**

- [org.xml.sax.XMLReader#setEntityResolver](../org/xml/sax/XMLReader.md)) 

### setErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setErrorHandler(handler: ErrorHandler!): Unit
```

Set the error handler.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `handler` | [ErrorHandler](../org/xml/sax/ErrorHandler.md)!:The new error handler. |

**See Also**

- [org.xml.sax.XMLReader#setEntityResolver](../org/xml/sax/XMLReader.md)) 

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

- [org.xml.sax.XMLReader#setFeature](../org/xml/sax/XMLReader.md)) 

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

- [org.xml.sax.XMLReader#setProperty](../org/xml/sax/XMLReader.md)) 

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

- [org.xml.sax.DocumentHandler#startDocument](../org/xml/sax/DocumentHandler.md)) 

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
| `qAtts` | [AttributeList](../org/xml/sax/AttributeList.md)!:The XML attribute list (with qnames). |

| Exceptions ||
|----------------------------|----------------------------------------------|
| `org.xml.sax.SAXException` | The client may raise a processing exception. |
