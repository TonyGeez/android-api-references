# XMLReaderAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XMLReaderAdapter

```
open class XMLReaderAdapter : ContentHandler, Parser
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xml.sax.helpers.XMLReaderAdapter](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#) |

Adapt a SAX2 XMLReader as a SAX1 Parser.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This class wraps a SAX2 [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#) and makes it act as a SAX1 [Parser](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#). The XMLReader must support a true value for the http://xml.org/sax/features/namespace-prefixes property or parsing will fail with a [SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException.html#); if the XMLReader supports a false value for the http://xml.org/sax/features/namespaces property, that will also be used to improve efficiency.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [XMLReaderAdapter](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#XMLReaderAdapter())`()` Create a new adapter. |
| [XMLReaderAdapter](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#XMLReaderAdapter(org.xml.sax.XMLReader))`(`xmlReader:` ` [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#)!`)` Create a new adapter. |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [characters](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#characters(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adapt a SAX2 characters event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endDocument](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#endDocument())`()` End document event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endElement](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#endElement(kotlin.String,%20kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adapt a SAX2 end element event. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endPrefixMapping](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#endPrefixMapping(kotlin.String))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adapt a SAX2 end prefix mapping event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ignorableWhitespace](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#ignorableWhitespace(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adapt a SAX2 ignorable whitespace event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#parse(kotlin.String))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse the document. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#parse(org.xml.sax.InputSource))`(`input:` ` [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!`)` Parse the document. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [processingInstruction](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#processingInstruction(kotlin.String,%20kotlin.String))`(`target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adapt a SAX2 processing instruction event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#setDTDHandler(org.xml.sax.DTDHandler))`(`handler:` ` [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#)!`)` Register the DTD event handler. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#setDocumentHandler(org.xml.sax.DocumentHandler))`(`handler:` ` [DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#)!`)` Register the SAX1 document event handler. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentLocator](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#setDocumentLocator(org.xml.sax.Locator))`(`locator:` ` [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#)!`)` Set a document locator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#setEntityResolver(org.xml.sax.EntityResolver))`(`resolver:` ` [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)!`)` Register the entity resolver. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#setErrorHandler(org.xml.sax.ErrorHandler))`(`handler:` ` [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)!`)` Register the error event handler. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocale](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#setLocale(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Set the locale for error reporting. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skippedEntity](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#skippedEntity(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adapt a SAX2 skipped entity event. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDocument](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#startDocument())`()` Start document event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startElement](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#startElement(kotlin.String,%20kotlin.String,%20kotlin.String,%20org.xml.sax.Attributes))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `atts:` ` [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#)!`)` Adapt a SAX2 start element event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startPrefixMapping](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#startPrefixMapping(kotlin.String,%20kotlin.String))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adapt a SAX2 start prefix mapping event. |
| --- | --- |

## Public constructors

### XMLReaderAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
XMLReaderAdapter()
```

Create a new adapter.

Use the "org.xml.sax.driver" property to locate the SAX2 driver to embed.

| Exceptions ||
|----------------------------|-------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | If the embedded driver cannot be instantiated or if the org.xml.sax.driver property is not specified. |

### XMLReaderAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
XMLReaderAdapter(xmlReader: XMLReader!)
```

Create a new adapter.

Create a new adapter, wrapped around a SAX2 XMLReader. The adapter will make the XMLReader act like a SAX1 Parser.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `xmlReader` | [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#)!:The SAX2 XMLReader to wrap. |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | If the argument is null. |

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

Adapt a SAX2 characters event.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:An array of characters. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The starting position in the array. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to use. |
| --- | --- |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may raise a processing exception. |

**See Also**

- [org.xml.sax.ContentHandler#characters](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#characters(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)) 

### endDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endDocument(): Unit
```

End document event.

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may raise a processing exception. |

**See Also**

- [org.xml.sax.ContentHandler#endDocument](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endDocument()) 

### endElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endElement(
    uri: String!, 
    localName: String!, 
    qName: String!
): Unit
```

Adapt a SAX2 end element event.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace local name. |
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified (prefixed) name. |
| --- | --- |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may raise a processing exception. |

**See Also**

- [org.xml.sax.ContentHandler#endElement](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endElement(kotlin.String,%20kotlin.String,%20kotlin.String)) 

### endPrefixMapping

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endPrefixMapping(prefix: String!): Unit
```

Adapt a SAX2 end prefix mapping event.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The prefix being mapped. |

| Exceptions ||
|----------------------------|-----------------------------------------------------|
| `org.xml.sax.SAXException` | the client may throw an exception during processing |

**See Also**

- [org.xml.sax.ContentHandler#endPrefixMapping](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endPrefixMapping(kotlin.String)) 

### ignorableWhitespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ignorableWhitespace(
    ch: CharArray!, 
    start: Int, 
    length: Int
): Unit
```

Adapt a SAX2 ignorable whitespace event.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:An array of characters. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The starting position in the array. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to use. |
| --- | --- |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may raise a processing exception. |

**See Also**

- [org.xml.sax.ContentHandler#ignorableWhitespace](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#ignorableWhitespace(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(systemId: String!): Unit
```

Parse the document.

This method will throw an exception if the embedded XMLReader does not support the http://xml.org/sax/features/namespace-prefixes property.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The absolute URL of the document. |

| Exceptions ||
|----------------------------|----------------------------------------------------------------|
| `java.io.IOException` | If there is a problem reading the raw content of the document. |
| `org.xml.sax.SAXException` | If there is a problem processing the document. |

**See Also**

- <https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#parse(org.xml.sax.InputSource)>
- [org.xml.sax.Parser#parse(java.lang.String)](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#parse(kotlin.String)) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(input: InputSource!): Unit
```

Parse the document.

This method will throw an exception if the embedded XMLReader does not support the http://xml.org/sax/features/namespace-prefixes property.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------|
| `source` | The input source for the top-level of the XML document. |
| `input` | [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!:An input source for the document. |

| Exceptions ||
|----------------------------|----------------------------------------------------------------|
| `java.io.IOException` | If there is a problem reading the raw content of the document. |
| `org.xml.sax.SAXException` | If there is a problem processing the document. |

**See Also**

- [#parse(java.lang.String)](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderAdapter#parse(kotlin.String))
- [org.xml.sax.Parser#parse(org.xml.sax.InputSource)](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#parse(org.xml.sax.InputSource)) 

### processingInstruction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun processingInstruction(
    target: String!, 
    data: String!
): Unit
```

Adapt a SAX2 processing instruction event.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The processing instruction target. |
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The remainder of the processing instruction |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may raise a processing exception. |

**See Also**

- [org.xml.sax.ContentHandler#processingInstruction](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#processingInstruction(kotlin.String,%20kotlin.String)) 

### setDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDTDHandler(handler: DTDHandler!): Unit
```

Register the DTD event handler.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `handler` | [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#)!:The new DTD event handler. |

**See Also**

- [org.xml.sax.Parser#setDTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#setDTDHandler(org.xml.sax.DTDHandler)) 

### setDocumentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDocumentHandler(handler: DocumentHandler!): Unit
```

Register the SAX1 document event handler.

Note that the SAX1 document handler has no Namespace support.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `handler` | [DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#)!:The new SAX1 document event handler. |

**See Also**

- [org.xml.sax.Parser#setDocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#setDocumentHandler(org.xml.sax.DocumentHandler)) 

### setDocumentLocator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDocumentLocator(locator: Locator!): Unit
```

Set a document locator.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------|
| `locator` | [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#)!:The document locator. |

**See Also**

- [org.xml.sax.ContentHandler#setDocumentLocator](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#setDocumentLocator(org.xml.sax.Locator)) 

### setEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEntityResolver(resolver: EntityResolver!): Unit
```

Register the entity resolver.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `resolver` | [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)!:The new resolver. |

**See Also**

- [org.xml.sax.Parser#setEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#setEntityResolver(org.xml.sax.EntityResolver)) 

### setErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setErrorHandler(handler: ErrorHandler!): Unit
```

Register the error event handler.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| `handler` | [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)!:The new error event handler. |

**See Also**

- [org.xml.sax.Parser#setErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#setErrorHandler(org.xml.sax.ErrorHandler)) 

### setLocale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLocale(locale: Locale!): Unit
```

Set the locale for error reporting.

This is not supported in SAX2, and will always throw an exception.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the locale for error reporting. |

**See Also**

- [org.xml.sax.Parser#setLocale](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#setLocale(java.util.Locale))

| Exceptions ||
|----------------------------|---------------------------|
| `org.xml.sax.SAXException` | Thrown unless overridden. |

### skippedEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skippedEntity(name: String!): Unit
```

Adapt a SAX2 skipped entity event.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the skipped entity. |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | Throwable by subclasses. |

**See Also**

- [org.xml.sax.ContentHandler#skippedEntity](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#skippedEntity(kotlin.String)) 

### startDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startDocument(): Unit
```

Start document event.

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may raise a processing exception. |

**See Also**

- [org.xml.sax.ContentHandler#startDocument](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startDocument()) 

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

Adapt a SAX2 start element event.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace local name. |
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified (prefixed) name. |
| --- | --- |
| `atts` | [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#)!:The SAX2 attributes. |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may raise a processing exception. |

**See Also**

- [org.xml.sax.ContentHandler#endDocument](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endDocument()) 

### startPrefixMapping

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startPrefixMapping(
    prefix: String!, 
    uri: String!
): Unit
```

Adapt a SAX2 start prefix mapping event.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The prefix being mapped. |
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI being mapped to. |

| Exceptions ||
|----------------------------|-----------------------------------------------------|
| `org.xml.sax.SAXException` | the client may throw an exception during processing |

**See Also**

- [org.xml.sax.ContentHandler#startPrefixMapping](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startPrefixMapping(kotlin.String,%20kotlin.String))
