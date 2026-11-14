# LexicalHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LexicalHandler

```
interface LexicalHandler
```

| [org.xml.sax.ext.LexicalHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#) |

| Known Direct Subclasses [DefaultHandler2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2), [TransformerHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/TransformerHandler.html#) |-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DefaultHandler2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2) | This class extends the SAX2 base handler class to support the SAX2 [LexicalHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#), [DeclHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler), and [EntityResolver2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/EntityResolver2) extensions. | | [TransformerHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/TransformerHandler.html#) | A TransformerHandler listens for SAX ContentHandler parse events and transforms them to a Result. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

SAX2 extension handler for lexical events.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This is an optional extension handler for SAX2 to provide lexical information about an XML document, such as comments and CDATA section boundaries. XML readers are not required to recognize this handler, and it is not part of core-only SAX2 distributions.

The events in the lexical handler apply to the entire document, not just to the document element, and all lexical handler events must appear between the content handler's startDocument and endDocument events.

To set the LexicalHandler for an XML reader, use the [setProperty](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#setProperty(kotlin.String,%20kotlin.Any))method with the property name`http://xml.org/sax/properties/lexical-handler`and an object implementing this interface (or null) as the value. If the reader does not report lexical events, it will throw a [SAXNotRecognizedException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXNotRecognizedException.html#) when you attempt to register the handler.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [comment](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#comment(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Report an XML comment anywhere in the document. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endCDATA](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#endCDATA())`()` Report the end of a CDATA section. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endDTD](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#endDTD())`()` Report the end of DTD declarations. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endEntity](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#endEntity(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Report the end of an entity. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startCDATA](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#startCDATA())`()` Report the start of a CDATA section. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDTD](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#startDTD(kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Report the start of DTD declarations, if any. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startEntity](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#startEntity(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Report the beginning of some internal and external XML entities. |

## Public methods

### comment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun comment(
    ch: CharArray!, 
    start: Int, 
    length: Int
): Unit
```

Report an XML comment anywhere in the document.

This callback will be used for comments inside or outside the document element, including comments in the external DTD subset (if read). Comments in the DTD must be properly nested inside start/endDTD and start/endEntity events (if used).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:An array holding the characters in the comment. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The starting position in the array. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to use from the array. |
| --- | --- |

| Exceptions ||
|----------------------------|-----------------------------------------|
| `org.xml.sax.SAXException` | The application may raise an exception. |

### endCDATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun endCDATA(): Unit
```

Report the end of a CDATA section.

| Exceptions ||
|----------------------------|-----------------------------------------|
| `org.xml.sax.SAXException` | The application may raise an exception. |

**See Also**

- [#startCDATA](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#startCDATA()) 

### endDTD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun endDTD(): Unit
```

Report the end of DTD declarations.

This method is intended to report the end of the DOCTYPE declaration; if the document has no DOCTYPE declaration, this method will not be invoked.

| Exceptions ||
|----------------------------|-----------------------------------------|
| `org.xml.sax.SAXException` | The application may raise an exception. |

**See Also**

- [#startDTD](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#startDTD(kotlin.String,%20kotlin.String,%20kotlin.String)) 

### endEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun endEntity(name: String!): Unit
```

Report the end of an entity.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the entity that is ending. |

| Exceptions ||
|----------------------------|-----------------------------------------|
| `org.xml.sax.SAXException` | The application may raise an exception. |

**See Also**

- [#startEntity](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#startEntity(kotlin.String)) 

### startCDATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startCDATA(): Unit
```

Report the start of a CDATA section.

The contents of the CDATA section will be reported through the regular [characters](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#characters(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))event; this event is intended only to report the boundary.

| Exceptions ||
|----------------------------|-----------------------------------------|
| `org.xml.sax.SAXException` | The application may raise an exception. |

**See Also**

- [#endCDATA](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#endCDATA()) 

### startDTD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startDTD(
    name: String!, 
    publicId: String!, 
    systemId: String!
): Unit
```

Report the start of DTD declarations, if any.

This method is intended to report the beginning of the DOCTYPE declaration; if the document has no DOCTYPE declaration, this method will not be invoked.

All declarations reported through [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#) or [DeclHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler) events must appear between the startDTD and [endDTD](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#endDTD())events. Declarations are assumed to belong to the internal DTD subset unless they appear between [startEntity](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#startEntity(kotlin.String))and [endEntity](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#endEntity(kotlin.String))events. Comments and processing instructions from the DTD should also be reported between the startDTD and endDTD events, in their original order of (logical) occurrence; they are not required to appear in their correct locations relative to DTDHandler or DeclHandler events, however.

Note that the start/endDTD events will appear within the start/endDocument events from ContentHandler and before the first [startElement](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startElement(kotlin.String,%20kotlin.String,%20kotlin.String,%20org.xml.sax.Attributes))event.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The document type name. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The declared public identifier for the external DTD subset, or null if none was declared. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The declared system identifier for the external DTD subset, or null if none was declared. (Note that this is not resolved against the document base URI.) |
| --- | --- |

| Exceptions ||
|----------------------------|-----------------------------------------|
| `org.xml.sax.SAXException` | The application may raise an exception. |

**See Also**

- [#endDTD](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#endDTD())
- [#startEntity](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#startEntity(kotlin.String)) 

### startEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startEntity(name: String!): Unit
```

Report the beginning of some internal and external XML entities.

The reporting of parameter entities (including the external DTD subset) is optional, and SAX2 drivers that report LexicalHandler events may not implement it; you can use the`http://xml.org/sax/features/lexical-handler/parameter-entities`feature to query or control the reporting of parameter entities.

General entities are reported with their regular names, parameter entities have '%' prepended to their names, and the external DTD subset has the pseudo-entity name "\[dtd\]".

When a SAX2 driver is providing these events, all other events must be properly nested within start/end entity events. There is no additional requirement that events from [DeclHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler) or [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#) be properly ordered.

Note that skipped entities will be reported through the [skippedEntity](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#skippedEntity(kotlin.String))event, which is part of the ContentHandler interface.

Because of the streaming event model that SAX uses, some entity boundaries cannot be reported under any circumstances:

- general entities within attribute values
- parameter entities within declarations

These will be silently expanded, with no indication of where the original entity boundaries were.

Note also that the boundaries of character references (which are not really entities anyway) are not reported.

All start/endEntity events must be properly nested.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the entity. If it is a parameter entity, the name will begin with '%', and if it is the external DTD subset, it will be "\[dtd\]". |

| Exceptions ||
|----------------------------|-----------------------------------------|
| `org.xml.sax.SAXException` | The application may raise an exception. |

**See Also**

- [#endEntity](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#endEntity(kotlin.String))
- [org.xml.sax.ext.DeclHandler#internalEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler#internalEntityDecl(kotlin.String,%20kotlin.String))
- [org.xml.sax.ext.DeclHandler#externalEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler#externalEntityDecl(kotlin.String,%20kotlin.String,%20kotlin.String))
