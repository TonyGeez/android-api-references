# DocumentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DocumentHandler

```
interface DocumentHandler
```

| [org.xml.sax.DocumentHandler](DocumentHandler.md) |

| Known Direct Subclasses [HandlerBase](HandlerBase.md), [ParserAdapter](../org.xml.sax.helpers/ParserAdapter.md) |---------------------------------------------------------------------------------------------------|------------------------------------------| | [HandlerBase](HandlerBase.md) | Default base class for handlers. | | [ParserAdapter](../org.xml.sax.helpers/ParserAdapter.md) | Adapt a SAX1 Parser as a SAX2 XMLReader. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 9.**
|
| This interface has been replaced by the SAX2 [ContentHandler](ContentHandler.md) interface, which includes Namespace support.

Receive notification of general document events.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This was the main event-handling interface for SAX1; in SAX2, it has been replaced by [ContentHandler](ContentHandler.md), which provides Namespace support and reporting of skipped entities. This interface is included in SAX2 only to support legacy SAX1 applications.

The order of events in this interface is very important, and mirrors the order of information in the document itself. For example, all of an element's content (character data, processing instructions, and/or subelements) will appear, in order, between the startElement event and the corresponding endElement event.

Application writers who do not want to implement the entire interface can derive a class from HandlerBase, which implements the default functionality; parser writers can instantiate HandlerBase to obtain a default handler. The application can find the location of any document event using the Locator interface supplied by the Parser through the setDocumentLocator method.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [characters](DocumentHandler.md))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Receive notification of character data. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endDocument](DocumentHandler.md))`()` Receive notification of the end of a document. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endElement](DocumentHandler.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of the end of an element. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ignorableWhitespace](DocumentHandler.md))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Receive notification of ignorable whitespace in element content. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [processingInstruction](DocumentHandler.md))`(`target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of a processing instruction. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentLocator](DocumentHandler.md))`(`locator:` ` [Locator](Locator.md)!`)` Receive an object for locating the origin of SAX document events. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDocument](DocumentHandler.md))`()` Receive notification of the beginning of a document. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startElement](DocumentHandler.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `atts:` ` [AttributeList](AttributeList.md)!`)` Receive notification of the beginning of an element. |

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

**Deprecated:** *Deprecated in Java.*

Receive notification of character data.

The Parser will call this method to report each chunk of character data. SAX parsers may return all contiguous character data in a single chunk, or they may split it into several chunks; however, all of the characters in any single event must come from the same external entity, so that the Locator provides useful information.

The application must not attempt to read from the array outside of the specified range.

Note that some parsers will report whitespace using the ignorableWhitespace() method rather than this one (validating parsers must do so).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The characters from the XML document. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The start position in the array. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to read from the array. |
| --- | --- |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [#ignorableWhitespace](DocumentHandler.md))
- [org.xml.sax.Locator](Locator.md) 

### endDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun endDocument(): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of the end of a document.

The SAX parser will invoke this method only once, and it will be the last method invoked during the parse. The parser shall not invoke this method until it has either abandoned parsing (because of an unrecoverable error) or reached the end of input.

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

### endElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun endElement(name: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of the end of an element.

The SAX parser will invoke this method at the end of every element in the XML document; there will be a corresponding startElement() event for every endElement() event (even when the element is empty).

If the element name has a namespace prefix, the prefix will still be attached to the name.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The element type name |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

### ignorableWhitespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun ignorableWhitespace(
    ch: CharArray!, 
    start: Int, 
    length: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of ignorable whitespace in element content.

Validating Parsers must use this method to report each chunk of ignorable whitespace (see the W3C XML 1.0 recommendation, section 2.10): non-validating parsers may also use this method if they are capable of parsing and using content models.

SAX parsers may return all contiguous whitespace in a single chunk, or they may split it into several chunks; however, all of the characters in any single event must come from the same external entity, so that the Locator provides useful information.

The application must not attempt to read from the array outside of the specified range.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The characters from the XML document. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The start position in the array. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to read from the array. |
| --- | --- |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [#characters](DocumentHandler.md)) 

### processingInstruction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun processingInstruction(
    target: String!, 
    data: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of a processing instruction.

The Parser will invoke this method once for each processing instruction found: note that processing instructions may occur before or after the main document element.

A SAX parser should never report an XML declaration (XML 1.0, section 2.8) or a text declaration (XML 1.0, section 4.3.1) using this method.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The processing instruction target. |
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The processing instruction data, or null if none was supplied. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

### setDocumentLocator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDocumentLocator(locator: Locator!): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive an object for locating the origin of SAX document events.

SAX parsers are strongly encouraged (though not absolutely required) to supply a locator: if it does so, it must supply the locator to the application by invoking this method before invoking any of the other methods in the DocumentHandler interface.

The locator allows the application to determine the end position of any document-related event, even if the parser is not reporting an error. Typically, the application will use this information for reporting its own errors (such as character content that does not match an application's business rules). The information returned by the locator is probably not sufficient for use with a search engine.

Note that the locator will return correct information only during the invocation of the events in this interface. The application should not attempt to use it at any other time.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `locator` | [Locator](Locator.md)!:An object that can return the location of any SAX document event. |

**See Also**

- [org.xml.sax.Locator](Locator.md) 

### startDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startDocument(): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of the beginning of a document.

The SAX parser will invoke this method only once, before any other methods in this interface or in DTDHandler (except for setDocumentLocator).

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

### startElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startElement(
    name: String!, 
    atts: AttributeList!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of the beginning of an element.

The Parser will invoke this method at the beginning of every element in the XML document; there will be a corresponding endElement() event for every startElement() event (even when the element is empty). All of the element's content will be reported, in order, before the corresponding endElement() event.

If the element name has a namespace prefix, the prefix will still be attached. Note that the attribute list provided will contain only attributes with explicit values (specified or defaulted): #IMPLIED attributes will be omitted.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The element type name. |
| `atts` | [AttributeList](AttributeList.md)!:The attributes attached to the element, if any. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [#endElement](DocumentHandler.md))
- [org.xml.sax.AttributeList](AttributeList.md)
