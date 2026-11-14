# LexicalHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LexicalHandler

```
interface LexicalHandler
```

| [org.xml.sax.ext.LexicalHandler](../org/xml/sax/ext/LexicalHandler.md) |

| Known Direct Subclasses [DefaultHandler2](../org/xml/sax/ext/DefaultHandler2.md), [TransformerHandler](../javax/xml/transform/sax/TransformerHandler.md) |-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DefaultHandler2](../org/xml/sax/ext/DefaultHandler2.md) | This class extends the SAX2 base handler class to support the SAX2 [LexicalHandler](../org/xml/sax/ext/LexicalHandler.md), [DeclHandler](../org/xml/sax/ext/DeclHandler.md), and [EntityResolver2](../org/xml/sax/ext/EntityResolver2.md) extensions. | | [TransformerHandler](../javax/xml/transform/sax/TransformerHandler.md) | A TransformerHandler listens for SAX ContentHandler parse events and transforms them to a Result. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

SAX2 extension handler for lexical events.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This is an optional extension handler for SAX2 to provide lexical information about an XML document, such as comments and CDATA section boundaries. XML readers are not required to recognize this handler, and it is not part of core-only SAX2 distributions.

The events in the lexical handler apply to the entire document, not just to the document element, and all lexical handler events must appear between the content handler's startDocument and endDocument events.

To set the LexicalHandler for an XML reader, use the [setProperty](../org/xml/sax/XMLReader.md))method with the property name`http://xml.org/sax/properties/lexical-handler`and an object implementing this interface (or null) as the value. If the reader does not report lexical events, it will throw a [SAXNotRecognizedException](../org/xml/sax/SAXNotRecognizedException.md) when you attempt to register the handler.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [comment](../org/xml/sax/ext/LexicalHandler.md))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Report an XML comment anywhere in the document. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endCDATA](../org/xml/sax/ext/LexicalHandler.md))`()` Report the end of a CDATA section. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endDTD](../org/xml/sax/ext/LexicalHandler.md))`()` Report the end of DTD declarations. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endEntity](../org/xml/sax/ext/LexicalHandler.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Report the end of an entity. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startCDATA](../org/xml/sax/ext/LexicalHandler.md))`()` Report the start of a CDATA section. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDTD](../org/xml/sax/ext/LexicalHandler.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Report the start of DTD declarations, if any. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startEntity](../org/xml/sax/ext/LexicalHandler.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Report the beginning of some internal and external XML entities. |

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

- [#startCDATA](../org/xml/sax/ext/LexicalHandler.md)) 

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

- [#startDTD](../org/xml/sax/ext/LexicalHandler.md)) 

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

- [#startEntity](../org/xml/sax/ext/LexicalHandler.md)) 

### startCDATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startCDATA(): Unit
```

Report the start of a CDATA section.

The contents of the CDATA section will be reported through the regular [characters](../org/xml/sax/ContentHandler.md))event; this event is intended only to report the boundary.

| Exceptions ||
|----------------------------|-----------------------------------------|
| `org.xml.sax.SAXException` | The application may raise an exception. |

**See Also**

- [#endCDATA](../org/xml/sax/ext/LexicalHandler.md)) 

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

All declarations reported through [DTDHandler](../org/xml/sax/DTDHandler.md) or [DeclHandler](../org/xml/sax/ext/DeclHandler.md) events must appear between the startDTD and [endDTD](../org/xml/sax/ext/LexicalHandler.md))events. Declarations are assumed to belong to the internal DTD subset unless they appear between [startEntity](../org/xml/sax/ext/LexicalHandler.md))and [endEntity](../org/xml/sax/ext/LexicalHandler.md))events. Comments and processing instructions from the DTD should also be reported between the startDTD and endDTD events, in their original order of (logical) occurrence; they are not required to appear in their correct locations relative to DTDHandler or DeclHandler events, however.

Note that the start/endDTD events will appear within the start/endDocument events from ContentHandler and before the first [startElement](../org/xml/sax/ContentHandler.md))event.

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

- [#endDTD](../org/xml/sax/ext/LexicalHandler.md))
- [#startEntity](../org/xml/sax/ext/LexicalHandler.md)) 

### startEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startEntity(name: String!): Unit
```

Report the beginning of some internal and external XML entities.

The reporting of parameter entities (including the external DTD subset) is optional, and SAX2 drivers that report LexicalHandler events may not implement it; you can use the`http://xml.org/sax/features/lexical-handler/parameter-entities`feature to query or control the reporting of parameter entities.

General entities are reported with their regular names, parameter entities have '%' prepended to their names, and the external DTD subset has the pseudo-entity name "\[dtd\]".

When a SAX2 driver is providing these events, all other events must be properly nested within start/end entity events. There is no additional requirement that events from [DeclHandler](../org/xml/sax/ext/DeclHandler.md) or [DTDHandler](../org/xml/sax/DTDHandler.md) be properly ordered.

Note that skipped entities will be reported through the [skippedEntity](../org/xml/sax/ContentHandler.md))event, which is part of the ContentHandler interface.

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

- [#endEntity](../org/xml/sax/ext/LexicalHandler.md))
- [org.xml.sax.ext.DeclHandler#internalEntityDecl](../org/xml/sax/ext/DeclHandler.md))
- [org.xml.sax.ext.DeclHandler#externalEntityDecl](../org/xml/sax/ext/DeclHandler.md))
