# ContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentHandler

```
interface ContentHandler
```

| [org.xml.sax.ContentHandler](../org/xml/sax/ContentHandler.md) |

| Known Direct Subclasses [DefaultHandler](../org/xml/sax/helpers/DefaultHandler.md), [TemplatesHandler](../javax/xml/transform/sax/TemplatesHandler.md), [TransformerHandler](../javax/xml/transform/sax/TransformerHandler.md), [ValidatorHandler](../javax/xml/validation/ValidatorHandler.md), [XMLFilterImpl](../org/xml/sax/helpers/XMLFilterImpl.md), [XMLReaderAdapter](../org/xml/sax/helpers/XMLReaderAdapter.md) |-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------| | [DefaultHandler](../org/xml/sax/helpers/DefaultHandler.md) | Default base class for SAX2 event handlers. | | [TemplatesHandler](../javax/xml/transform/sax/TemplatesHandler.md) | A SAX ContentHandler that may be used to process SAX parse events (parsing transformation instructions) into a Templates object. | | [TransformerHandler](../javax/xml/transform/sax/TransformerHandler.md) | A TransformerHandler listens for SAX ContentHandler parse events and transforms them to a Result. | | [ValidatorHandler](../javax/xml/validation/ValidatorHandler.md) | Streaming validator that works on SAX stream. | | [XMLFilterImpl](../org/xml/sax/helpers/XMLFilterImpl.md) | Base class for deriving an XML filter. | | [XMLReaderAdapter](../org/xml/sax/helpers/XMLReaderAdapter.md) | Adapt a SAX2 XMLReader as a SAX1 Parser. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DefaultHandler2](../org/xml/sax/ext/DefaultHandler2.md) |---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DefaultHandler2](../org/xml/sax/ext/DefaultHandler2.md) | This class extends the SAX2 base handler class to support the SAX2 [LexicalHandler](../org/xml/sax/ext/LexicalHandler.md), [DeclHandler](../org/xml/sax/ext/DeclHandler.md), and [EntityResolver2](../org/xml/sax/ext/EntityResolver2.md) extensions. | |
| --- | --- | --- | --- | --- | --- | --- |

Receive notification of the logical content of a document.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This is the main interface that most SAX applications implement: if the application needs to be informed of basic parsing events, it implements this interface and registers an instance with the SAX parser using the [setContentHandler](../org/xml/sax/XMLReader.md))method. The parser uses the instance to report basic document-related events like the start and end of elements and character data.

The order of events in this interface is very important, and mirrors the order of information in the document itself. For example, all of an element's content (character data, processing instructions, and/or subelements) will appear, in order, between the startElement event and the corresponding endElement event.

This interface is similar to the now-deprecated SAX 1.0 DocumentHandler interface, but it adds support for Namespaces and for reporting skipped entities (in non-validating XML processors).

Implementors should note that there is also a`ContentHandler`class in the`java.net`package; that means that it's probably a bad idea to do 

```kotlin
import java.net.*;
  import org.xml.sax.*;
  
```

In fact, "import ...\*" is usually a sign of sloppy programming anyway, so the user should consider this a feature rather than a bug.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [characters](../org/xml/sax/ContentHandler.md))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Receive notification of character data. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endDocument](../org/xml/sax/ContentHandler.md))`()` Receive notification of the end of a document. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endElement](../org/xml/sax/ContentHandler.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of the end of an element. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endPrefixMapping](../org/xml/sax/ContentHandler.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` End the scope of a prefix-URI mapping. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ignorableWhitespace](../org/xml/sax/ContentHandler.md))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Receive notification of ignorable whitespace in element content. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [processingInstruction](../org/xml/sax/ContentHandler.md))`(`target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of a processing instruction. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentLocator](../org/xml/sax/ContentHandler.md))`(`locator:` ` [Locator](../org/xml/sax/Locator.md)!`)` Receive an object for locating the origin of SAX document events. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skippedEntity](../org/xml/sax/ContentHandler.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of a skipped entity. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDocument](../org/xml/sax/ContentHandler.md))`()` Receive notification of the beginning of a document. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startElement](../org/xml/sax/ContentHandler.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `atts:` ` [Attributes](../org/xml/sax/Attributes.md)!`)` Receive notification of the beginning of an element. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startPrefixMapping](../org/xml/sax/ContentHandler.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Begin the scope of a prefix-URI Namespace mapping. |

## Public methods

### characters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun characters(
    ch: CharArray!, 
    start: Int, 
    length: Int
): Unit
```

Receive notification of character data.

The Parser will call this method to report each chunk of character data. SAX parsers may return all contiguous character data in a single chunk, or they may split it into several chunks; however, all of the characters in any single event must come from the same external entity so that the Locator provides useful information.

The application must not attempt to read from the array outside of the specified range.

Individual characters may consist of more than one Java`char`value. There are two important cases where this happens, because characters can't be represented in just sixteen bits. In one case, characters are represented in a*Surrogate Pair*, using two special Unicode values. Such characters are in the so-called "Astral Planes", with a code point above U+FFFF. A second case involves composite characters, such as a base character combining with one or more accent characters.

Your code should not assume that algorithms using`char`-at-a-time idioms will be working in character units; in some cases they will split characters. This is relevant wherever XML permits arbitrary characters, such as attribute values, processing instruction data, and comments as well as in data reported from this method. It's also generally relevant whenever Java code manipulates internationalized text; the issue isn't unique to XML.

Note that some parsers will report whitespace in element content using the [ignorableWhitespace](../org/xml/sax/ContentHandler.md))method rather than this one (validating parsers*must*do so).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the characters from the XML document |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start position in the array |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of characters to read from the array |
| --- | --- |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |

**See Also**

- [#ignorableWhitespace](../org/xml/sax/ContentHandler.md))
- [org.xml.sax.Locator](../org/xml/sax/Locator.md) 

### endDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun endDocument(): Unit
```

Receive notification of the end of a document.

**There is an apparent contradiction between the documentation for this method and the documentation for [org.xml.sax.ErrorHandler#fatalError](../org/xml/sax/ErrorHandler.md)). Until this ambiguity is resolved in a future major release, clients should make no assumptions about whether endDocument() will or will not be invoked when the parser has reported a fatalError() or thrown an exception.**

The SAX parser will invoke this method only once, and it will be the last method invoked during the parse. The parser shall not invoke this method until it has either abandoned parsing (because of an unrecoverable error) or reached the end of input.

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |

**See Also**

- [#startDocument](../org/xml/sax/ContentHandler.md)) 

### endElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun endElement(
    uri: String!, 
    localName: String!, 
    qName: String!
): Unit
```

Receive notification of the end of an element.

The SAX parser will invoke this method at the end of every element in the XML document; there will be a corresponding [startElement](../org/xml/sax/ContentHandler.md))event for every endElement event (even when the element is empty).

For information on the names, see startElement.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the Namespace URI, or the empty string if the element has no Namespace URI or if Namespace processing is not being performed |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the local name (without prefix), or the empty string if Namespace processing is not being performed |
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the qualified XML name (with prefix), or the empty string if qualified names are not available |
| --- | --- |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |

### endPrefixMapping

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun endPrefixMapping(prefix: String!): Unit
```

End the scope of a prefix-URI mapping.

See [startPrefixMapping](../org/xml/sax/ContentHandler.md))for details. These events will always occur immediately after the corresponding [endElement](../org/xml/sax/ContentHandler.md))event, but the order of [endPrefixMapping](../org/xml/sax/ContentHandler.md))events is not otherwise guaranteed.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the prefix that was being mapped. This is the empty string when a default mapping scope ends. |

| Exceptions ||
|----------------------------|-----------------------------------------------------|
| `org.xml.sax.SAXException` | the client may throw an exception during processing |

**See Also**

- [#startPrefixMapping](../org/xml/sax/ContentHandler.md))
- [#endElement](../org/xml/sax/ContentHandler.md)) 

### ignorableWhitespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun ignorableWhitespace(
    ch: CharArray!, 
    start: Int, 
    length: Int
): Unit
```

Receive notification of ignorable whitespace in element content.

Validating Parsers must use this method to report each chunk of whitespace in element content (see the W3C XML 1.0 recommendation, section 2.10): non-validating parsers may also use this method if they are capable of parsing and using content models.

SAX parsers may return all contiguous whitespace in a single chunk, or they may split it into several chunks; however, all of the characters in any single event must come from the same external entity, so that the Locator provides useful information.

The application must not attempt to read from the array outside of the specified range.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the characters from the XML document |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start position in the array |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of characters to read from the array |
| --- | --- |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |

**See Also**

- [#characters](../org/xml/sax/ContentHandler.md)) 

### processingInstruction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun processingInstruction(
    target: String!, 
    data: String!
): Unit
```

Receive notification of a processing instruction.

The Parser will invoke this method once for each processing instruction found: note that processing instructions may occur before or after the main document element.

A SAX parser must never report an XML declaration (XML 1.0, section 2.8) or a text declaration (XML 1.0, section 4.3.1) using this method.

Like [characters()](../org/xml/sax/ContentHandler.md)), processing instruction data may have characters that need more than one`char`value.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the processing instruction target |
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the processing instruction data, or null if none was supplied. The data does not include any whitespace separating it from the target |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |

### setDocumentLocator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDocumentLocator(locator: Locator!): Unit
```

Receive an object for locating the origin of SAX document events.

SAX parsers are strongly encouraged (though not absolutely required) to supply a locator: if it does so, it must supply the locator to the application by invoking this method before invoking any of the other methods in the ContentHandler interface.

The locator allows the application to determine the end position of any document-related event, even if the parser is not reporting an error. Typically, the application will use this information for reporting its own errors (such as character content that does not match an application's business rules). The information returned by the locator is probably not sufficient for use with a search engine.

Note that the locator will return correct information only during the invocation SAX event callbacks after [startDocument](../org/xml/sax/ContentHandler.md))returns and before [endDocument](../org/xml/sax/ContentHandler.md))is called. The application should not attempt to use it at any other time.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `locator` | [Locator](../org/xml/sax/Locator.md)!:an object that can return the location of any SAX document event |

**See Also**

- [org.xml.sax.Locator](../org/xml/sax/Locator.md) 

### skippedEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun skippedEntity(name: String!): Unit
```

Receive notification of a skipped entity. This is not called for entity references within markup constructs such as element start tags or markup declarations. (The XML recommendation requires reporting skipped external entities. SAX also reports internal entity expansion/non-expansion, except within markup constructs.)

The Parser will invoke this method each time the entity is skipped. Non-validating processors may skip entities if they have not seen the declarations (because, for example, the entity was declared in an external DTD subset). All processors may skip external entities, depending on the values of the`http://xml.org/sax/features/external-general-entities`and the`http://xml.org/sax/features/external-parameter-entities`properties.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the skipped entity. If it is a parameter entity, the name will begin with '%', and if it is the external DTD subset, it will be the string "\[dtd\]" |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |

### startDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startDocument(): Unit
```

Receive notification of the beginning of a document.

The SAX parser will invoke this method only once, before any other event callbacks (except for [setDocumentLocator](../org/xml/sax/ContentHandler.md))).

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |

**See Also**

- [#endDocument](../org/xml/sax/ContentHandler.md)) 

### startElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startElement(
    uri: String!, 
    localName: String!, 
    qName: String!, 
    atts: Attributes!
): Unit
```

Receive notification of the beginning of an element.

The Parser will invoke this method at the beginning of every element in the XML document; there will be a corresponding [endElement](../org/xml/sax/ContentHandler.md))event for every startElement event (even when the element is empty). All of the element's content will be reported, in order, before the corresponding endElement event.

This event allows up to three name components for each element:

1. the Namespace URI;
2. the local name; and
3. the qualified (prefixed) name.

Any or all of these may be provided, depending on the values of the http://xml.org/sax/features/namespaces and the http://xml.org/sax/features/namespace-prefixes properties:

- the Namespace URI and local name are required when the namespaces property is true (the default), and are optional when the namespaces property is false (if one is specified, both must be);
- the qualified name is required when the namespace-prefixes property is true, and is optional when the namespace-prefixes property is false (the default).

Note that the attribute list provided will contain only attributes with explicit values (specified or defaulted): #IMPLIED attributes will be omitted. The attribute list will contain attributes used for Namespace declarations (xmlns\* attributes) only if the`http://xml.org/sax/features/namespace-prefixes`property is true (it is false by default, and support for a true value is optional).

Like [characters()](../org/xml/sax/ContentHandler.md)), attribute values may have characters that need more than one`char`value.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the Namespace URI, or the empty string if the element has no Namespace URI or if Namespace processing is not being performed |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the local name (without prefix), or the empty string if Namespace processing is not being performed |
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the qualified name (with prefix), or the empty string if qualified names are not available |
| --- | --- |
| `atts` | [Attributes](../org/xml/sax/Attributes.md)!:the attributes attached to the element. If there are no attributes, it shall be an empty Attributes object. The value of this object after startElement returns is undefined |

| Exceptions ||
|----------------------------|--------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |

**See Also**

- [#endElement](../org/xml/sax/ContentHandler.md))
- [org.xml.sax.Attributes](../org/xml/sax/Attributes.md)
- [org.xml.sax.helpers.AttributesImpl](../org/xml/sax/helpers/AttributesImpl.md) 

### startPrefixMapping

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startPrefixMapping(
    prefix: String!, 
    uri: String!
): Unit
```

Begin the scope of a prefix-URI Namespace mapping.

The information from this event is not necessary for normal Namespace processing: the SAX XML reader will automatically replace prefixes for element and attribute names when the`http://xml.org/sax/features/namespaces`feature is true (the default).

There are cases, however, when applications need to use prefixes in character data or in attribute values, where they cannot safely be expanded automatically; the start/endPrefixMapping event supplies the information to the application to expand prefixes in those contexts itself, if necessary.

Note that start/endPrefixMapping events are not guaranteed to be properly nested relative to each other: all startPrefixMapping events will occur immediately before the corresponding [startElement](../org/xml/sax/ContentHandler.md))event, and all [endPrefixMapping](../org/xml/sax/ContentHandler.md))events will occur immediately after the corresponding [endElement](../org/xml/sax/ContentHandler.md))event, but their order is not otherwise guaranteed.

There should never be start/endPrefixMapping events for the "xml" prefix, since it is predeclared and immutable.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the Namespace prefix being declared. An empty string is used for the default element namespace, which has no prefix. |
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the Namespace URI the prefix is mapped to |

| Exceptions ||
|----------------------------|-----------------------------------------------------|
| `org.xml.sax.SAXException` | the client may throw an exception during processing |

**See Also**

- [#endPrefixMapping](../org/xml/sax/ContentHandler.md))
- [#startElement](../org/xml/sax/ContentHandler.md))
