# XMLReaderAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XMLReaderAdapter

```
open class XMLReaderAdapter : ContentHandler, Parser
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xml.sax.helpers.XMLReaderAdapter](../org/xml/sax/helpers/XMLReaderAdapter.md) |

Adapt a SAX2 XMLReader as a SAX1 Parser.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This class wraps a SAX2 [XMLReader](../org/xml/sax/XMLReader.md) and makes it act as a SAX1 [Parser](../org/xml/sax/Parser.md). The XMLReader must support a true value for the http://xml.org/sax/features/namespace-prefixes property or parsing will fail with a [SAXException](../org/xml/sax/SAXException.md); if the XMLReader supports a false value for the http://xml.org/sax/features/namespaces property, that will also be used to improve efficiency.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [XMLReaderAdapter](../org/xml/sax/helpers/XMLReaderAdapter.md))`()` Create a new adapter. |
| [XMLReaderAdapter](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`xmlReader:` ` [XMLReader](../org/xml/sax/XMLReader.md)!`)` Create a new adapter. |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [characters](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adapt a SAX2 characters event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endDocument](../org/xml/sax/helpers/XMLReaderAdapter.md))`()` End document event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endElement](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adapt a SAX2 end element event. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endPrefixMapping](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adapt a SAX2 end prefix mapping event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ignorableWhitespace](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adapt a SAX2 ignorable whitespace event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse the document. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`input:` ` [InputSource](../org/xml/sax/InputSource.md)!`)` Parse the document. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [processingInstruction](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adapt a SAX2 processing instruction event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDTDHandler](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`handler:` ` [DTDHandler](../org/xml/sax/DTDHandler.md)!`)` Register the DTD event handler. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentHandler](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`handler:` ` [DocumentHandler](../org/xml/sax/DocumentHandler.md)!`)` Register the SAX1 document event handler. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentLocator](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`locator:` ` [Locator](../org/xml/sax/Locator.md)!`)` Set a document locator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntityResolver](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`resolver:` ` [EntityResolver](../org/xml/sax/EntityResolver.md)!`)` Register the entity resolver. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`handler:` ` [ErrorHandler](../org/xml/sax/ErrorHandler.md)!`)` Register the error event handler. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocale](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Set the locale for error reporting. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skippedEntity](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adapt a SAX2 skipped entity event. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDocument](../org/xml/sax/helpers/XMLReaderAdapter.md))`()` Start document event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startElement](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `atts:` ` [Attributes](../org/xml/sax/Attributes.md)!`)` Adapt a SAX2 start element event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startPrefixMapping](../org/xml/sax/helpers/XMLReaderAdapter.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adapt a SAX2 start prefix mapping event. |
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
| `xmlReader` | [XMLReader](../org/xml/sax/XMLReader.md)!:The SAX2 XMLReader to wrap. |

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

- [org.xml.sax.ContentHandler#characters](../org/xml/sax/ContentHandler.md)) 

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

- [org.xml.sax.ContentHandler#endDocument](../org/xml/sax/ContentHandler.md)) 

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

- [org.xml.sax.ContentHandler#endElement](../org/xml/sax/ContentHandler.md)) 

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

- [org.xml.sax.ContentHandler#endPrefixMapping](../org/xml/sax/ContentHandler.md)) 

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

- [org.xml.sax.ContentHandler#ignorableWhitespace](../org/xml/sax/ContentHandler.md)) 

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
- [org.xml.sax.Parser#parse(java.lang.String)](../org/xml/sax/Parser.md)) 

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
| `input` | [InputSource](../org/xml/sax/InputSource.md)!:An input source for the document. |

| Exceptions ||
|----------------------------|----------------------------------------------------------------|
| `java.io.IOException` | If there is a problem reading the raw content of the document. |
| `org.xml.sax.SAXException` | If there is a problem processing the document. |

**See Also**

- [#parse(java.lang.String)](../org/xml/sax/helpers/XMLReaderAdapter.md))
- [org.xml.sax.Parser#parse(org.xml.sax.InputSource)](../org/xml/sax/Parser.md)) 

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

- [org.xml.sax.ContentHandler#processingInstruction](../org/xml/sax/ContentHandler.md)) 

### setDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDTDHandler(handler: DTDHandler!): Unit
```

Register the DTD event handler.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `handler` | [DTDHandler](../org/xml/sax/DTDHandler.md)!:The new DTD event handler. |

**See Also**

- [org.xml.sax.Parser#setDTDHandler](../org/xml/sax/Parser.md)) 

### setDocumentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDocumentHandler(handler: DocumentHandler!): Unit
```

Register the SAX1 document event handler.

Note that the SAX1 document handler has no Namespace support.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `handler` | [DocumentHandler](../org/xml/sax/DocumentHandler.md)!:The new SAX1 document event handler. |

**See Also**

- [org.xml.sax.Parser#setDocumentHandler](../org/xml/sax/Parser.md)) 

### setDocumentLocator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDocumentLocator(locator: Locator!): Unit
```

Set a document locator.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------|
| `locator` | [Locator](../org/xml/sax/Locator.md)!:The document locator. |

**See Also**

- [org.xml.sax.ContentHandler#setDocumentLocator](../org/xml/sax/ContentHandler.md)) 

### setEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEntityResolver(resolver: EntityResolver!): Unit
```

Register the entity resolver.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `resolver` | [EntityResolver](../org/xml/sax/EntityResolver.md)!:The new resolver. |

**See Also**

- [org.xml.sax.Parser#setEntityResolver](../org/xml/sax/Parser.md)) 

### setErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setErrorHandler(handler: ErrorHandler!): Unit
```

Register the error event handler.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| `handler` | [ErrorHandler](../org/xml/sax/ErrorHandler.md)!:The new error event handler. |

**See Also**

- [org.xml.sax.Parser#setErrorHandler](../org/xml/sax/Parser.md)) 

### setLocale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLocale(locale: Locale!): Unit
```

Set the locale for error reporting.

This is not supported in SAX2, and will always throw an exception.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the locale for error reporting. |

**See Also**

- [org.xml.sax.Parser#setLocale](../org/xml/sax/Parser.md))

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

- [org.xml.sax.ContentHandler#skippedEntity](../org/xml/sax/ContentHandler.md)) 

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

- [org.xml.sax.ContentHandler#startDocument](../org/xml/sax/ContentHandler.md)) 

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
| `atts` | [Attributes](../org/xml/sax/Attributes.md)!:The SAX2 attributes. |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | The client may raise a processing exception. |

**See Also**

- [org.xml.sax.ContentHandler#endDocument](../org/xml/sax/ContentHandler.md)) 

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

- [org.xml.sax.ContentHandler#startPrefixMapping](../org/xml/sax/ContentHandler.md))
