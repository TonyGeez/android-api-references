# DTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DTDHandler

```
interface DTDHandler
```

| [org.xml.sax.DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler#) |

| Known Direct Subclasses [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler), [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase), [TransformerHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/TransformerHandler.html#), [XMLFilterImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl) |-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------| | [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler) | Default base class for SAX2 event handlers. | | [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase) | Default base class for handlers. | | [TransformerHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/TransformerHandler.html#) | A TransformerHandler listens for SAX ContentHandler parse events and transforms them to a Result. | | [XMLFilterImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl) | Base class for deriving an XML filter. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DefaultHandler2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2) |---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DefaultHandler2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2) | This class extends the SAX2 base handler class to support the SAX2 [LexicalHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler), [DeclHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler), and [EntityResolver2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/EntityResolver2) extensions. | |
| --- | --- | --- | --- | --- | --- | --- |

Receive notification of basic DTD-related events.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

If a SAX application needs information about notations and unparsed entities, then the application implements this interface and registers an instance with the SAX parser using the parser's setDTDHandler method. The parser uses the instance to report notation and unparsed entity declarations to the application.

Note that this interface includes only those DTD events that the XML recommendation*requires*processors to report: notation and unparsed entity declarations.

The SAX parser may report these events in any order, regardless of the order in which the notations and unparsed entities were declared; however, all DTD events must be reported after the document handler's startDocument event, and before the first startElement event. (If the [LexicalHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler) is used, these events must also be reported before the endDTD event.)

It is up to the application to store the information for future use (perhaps in a hash table or object tree). If the application encounters attributes of type "NOTATION", "ENTITY", or "ENTITIES", it can use the information that it obtained through this interface to find the entity and/or notation corresponding with the attribute value.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notationDecl](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler#notationDecl(kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of a notation declaration event. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unparsedEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler#unparsedEntityDecl(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `notationName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of an unparsed entity declaration event. |

## Public methods

### notationDecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun notationDecl(
    name: String!, 
    publicId: String!, 
    systemId: String!
): Unit
```

Receive notification of a notation declaration event.

It is up to the application to record the notation for later reference, if necessary; notations may appear as attribute values and in unparsed entity declarations, and are sometime used with processing instruction target names.

At least one of publicId and systemId must be non-null. If a system identifier is present, and it is a URL, the SAX parser must resolve it fully before passing it to the application through this event.

There is no guarantee that the notation declaration will be reported before any unparsed entities that use it.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The notation name. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The notation's public identifier, or null if none was given. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The notation's system identifier, or null if none was given. |
| --- | --- |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [#unparsedEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler#unparsedEntityDecl(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))
- [org.xml.sax.Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes) 

### unparsedEntityDecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unparsedEntityDecl(
    name: String!, 
    publicId: String!, 
    systemId: String!, 
    notationName: String!
): Unit
```

Receive notification of an unparsed entity declaration event.

Note that the notation name corresponds to a notation reported by the [notationDecl](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler#notationDecl(kotlin.String,%20kotlin.String,%20kotlin.String))event. It is up to the application to record the entity for later reference, if necessary; unparsed entities may appear as attribute values.

If the system identifier is a URL, the parser must resolve it fully before passing it to the application.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The unparsed entity's name. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity's public identifier, or null if none was given. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity's system identifier. |
| --- | --- |
| `notationName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the associated notation. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [#notationDecl](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler#notationDecl(kotlin.String,%20kotlin.String,%20kotlin.String))
- [org.xml.sax.Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes)
