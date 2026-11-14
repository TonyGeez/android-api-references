# DefaultHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DefaultHandler

```
open class DefaultHandler : ContentHandler, DTDHandler, EntityResolver, ErrorHandler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xml.sax.helpers.DefaultHandler](../org/xml/sax/helpers/DefaultHandler.md) |

| Known Direct Subclasses [DefaultHandler2](../org/xml/sax/ext/DefaultHandler2.md) |---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DefaultHandler2](../org/xml/sax/ext/DefaultHandler2.md) | This class extends the SAX2 base handler class to support the SAX2 [LexicalHandler](../org/xml/sax/ext/LexicalHandler.md), [DeclHandler](../org/xml/sax/ext/DeclHandler.md), and [EntityResolver2](../org/xml/sax/ext/EntityResolver2.md) extensions. | |
| --- | --- | --- | --- | --- | --- | --- |

Default base class for SAX2 event handlers.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This class is available as a convenience base class for SAX2 applications: it provides default implementations for all of the callbacks in the four core SAX2 handler classes:

- [EntityResolver](../org/xml/sax/EntityResolver.md)
- [DTDHandler](../org/xml/sax/DTDHandler.md)
- [ContentHandler](../org/xml/sax/ContentHandler.md)
- [ErrorHandler](../org/xml/sax/ErrorHandler.md)

Application writers can extend this class when they need to implement only part of an interface; parser writers can instantiate this class to provide default handlers when the application has not supplied its own.

This class replaces the deprecated SAX1 [HandlerBase](../org/xml/sax/HandlerBase.md) class.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------|---|
| [DefaultHandler](../org/xml/sax/helpers/DefaultHandler.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [characters](../org/xml/sax/helpers/DefaultHandler.md))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Receive notification of character data inside an element. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endDocument](../org/xml/sax/helpers/DefaultHandler.md))`()` Receive notification of the end of the document. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endElement](../org/xml/sax/helpers/DefaultHandler.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of the end of an element. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endPrefixMapping](../org/xml/sax/helpers/DefaultHandler.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of the end of a Namespace mapping. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [error](../org/xml/sax/helpers/DefaultHandler.md))`(`e:` ` [SAXParseException](../org/xml/sax/SAXParseException.md)!`)` Receive notification of a recoverable parser error. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fatalError](../org/xml/sax/helpers/DefaultHandler.md))`(`e:` ` [SAXParseException](../org/xml/sax/SAXParseException.md)!`)` Report a fatal XML parsing error. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ignorableWhitespace](../org/xml/sax/helpers/DefaultHandler.md))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Receive notification of ignorable whitespace in element content. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notationDecl](../org/xml/sax/helpers/DefaultHandler.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of a notation declaration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [processingInstruction](../org/xml/sax/helpers/DefaultHandler.md))`(`target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of a processing instruction. |
| --- | --- |
| open [InputSource](../org/xml/sax/InputSource.md)! | [resolveEntity](../org/xml/sax/helpers/DefaultHandler.md))`(`publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Resolve an external entity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentLocator](../org/xml/sax/helpers/DefaultHandler.md))`(`locator:` ` [Locator](../org/xml/sax/Locator.md)!`)` Receive a Locator object for document events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skippedEntity](../org/xml/sax/helpers/DefaultHandler.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of a skipped entity. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDocument](../org/xml/sax/helpers/DefaultHandler.md))`()` Receive notification of the beginning of the document. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startElement](../org/xml/sax/helpers/DefaultHandler.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attributes:` ` [Attributes](../org/xml/sax/Attributes.md)!`)` Receive notification of the start of an element. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startPrefixMapping](../org/xml/sax/helpers/DefaultHandler.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of the start of a Namespace mapping. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unparsedEntityDecl](../org/xml/sax/helpers/DefaultHandler.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `notationName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of an unparsed entity declaration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [warning](../org/xml/sax/helpers/DefaultHandler.md))`(`e:` ` [SAXParseException](../org/xml/sax/SAXParseException.md)!`)` Receive notification of a parser warning. |

## Public constructors

### DefaultHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DefaultHandler()
```

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

Receive notification of character data inside an element.

By default, do nothing. Application writers may override this method to take specific actions for each chunk of character data (such as adding the data to a node or buffer, or printing it to a file).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The characters. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The start position in the character array. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to use from the character array. |
| --- | --- |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ContentHandler#characters](../org/xml/sax/ContentHandler.md)) 

### endDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endDocument(): Unit
```

Receive notification of the end of the document.

By default, do nothing. Application writers may override this method in a subclass to take specific actions at the end of a document (such as finalising a tree or closing an output file).

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

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

Receive notification of the end of an element.

By default, do nothing. Application writers may override this method in a subclass to take specific actions at the end of each element (such as finalising a tree node or writing output to a file).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty string if the element has no Namespace URI or if Namespace processing is not being performed. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The local name (without prefix), or the empty string if Namespace processing is not being performed. |
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified name (with prefix), or the empty string if qualified names are not available. |
| --- | --- |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ContentHandler#endElement](../org/xml/sax/ContentHandler.md)) 

### endPrefixMapping

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endPrefixMapping(prefix: String!): Unit
```

Receive notification of the end of a Namespace mapping.

By default, do nothing. Application writers may override this method in a subclass to take specific actions at the end of each prefix mapping.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace prefix being declared. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | the client may throw an exception during processing |
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ContentHandler#endPrefixMapping](../org/xml/sax/ContentHandler.md)) 

### error

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun error(e: SAXParseException!): Unit
```

Receive notification of a recoverable parser error.

The default implementation does nothing. Application writers may override this method in a subclass to take specific actions for each error, such as inserting the message in a log file or printing it to the console.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | The error information encapsulated in a SAX parse exception. |
| `e` | [SAXParseException](../org/xml/sax/SAXParseException.md)!:The warning information encoded as an exception. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ErrorHandler#warning](../org/xml/sax/ErrorHandler.md))
- [org.xml.sax.SAXParseException](../org/xml/sax/SAXParseException.md) 

### fatalError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fatalError(e: SAXParseException!): Unit
```

Report a fatal XML parsing error.

The default implementation throws a SAXParseException. Application writers may override this method in a subclass if they need to take specific actions for each fatal error (such as collecting all of the errors into a single report): in any case, the application must stop all regular processing when this method is invoked, since the document is no longer reliable, and the parser may no longer report parsing events.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | The error information encapsulated in a SAX parse exception. |
| `e` | [SAXParseException](../org/xml/sax/SAXParseException.md)!:The error information encoded as an exception. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ErrorHandler#fatalError](../org/xml/sax/ErrorHandler.md))
- [org.xml.sax.SAXParseException](../org/xml/sax/SAXParseException.md) 

### ignorableWhitespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ignorableWhitespace(
    ch: CharArray!, 
    start: Int, 
    length: Int
): Unit
```

Receive notification of ignorable whitespace in element content.

By default, do nothing. Application writers may override this method to take specific actions for each chunk of ignorable whitespace (such as adding data to a node or buffer, or printing it to a file).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The whitespace characters. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The start position in the character array. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to use from the character array. |
| --- | --- |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ContentHandler#ignorableWhitespace](../org/xml/sax/ContentHandler.md)) 

### notationDecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notationDecl(
    name: String!, 
    publicId: String!, 
    systemId: String!
): Unit
```

Receive notification of a notation declaration.

By default, do nothing. Application writers may override this method in a subclass if they wish to keep track of the notations declared in a document.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The notation name. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The notation public identifier, or null if not available. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The notation system identifier. |
| --- | --- |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.DTDHandler#notationDecl](../org/xml/sax/DTDHandler.md)) 

### processingInstruction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun processingInstruction(
    target: String!, 
    data: String!
): Unit
```

Receive notification of a processing instruction.

By default, do nothing. Application writers may override this method in a subclass to take specific actions for each processing instruction, such as setting status variables or invoking other methods.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The processing instruction target. |
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The processing instruction data, or null if none is supplied. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ContentHandler#processingInstruction](../org/xml/sax/ContentHandler.md)) 

### resolveEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resolveEntity(
    publicId: String!, 
    systemId: String!
): InputSource!
```

Resolve an external entity.

Always return null, so that the parser will use the system identifier provided in the XML document. This method implements the SAX default behaviour: application writers can override it in a subclass to do special translations such as catalog lookups or URI redirection.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The public identifier, or null if none is available. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier provided in the XML document. |

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [InputSource](../org/xml/sax/InputSource.md)! | The new input source, or null to require the default behaviour. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `java.io.IOException` | If there is an error setting up the new input source. |
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.EntityResolver#resolveEntity](../org/xml/sax/EntityResolver.md)) 

### setDocumentLocator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDocumentLocator(locator: Locator!): Unit
```

Receive a Locator object for document events.

By default, do nothing. Application writers may override this method in a subclass if they wish to store the locator for use with other document events.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| `locator` | [Locator](../org/xml/sax/Locator.md)!:A locator for all SAX document events. |

**See Also**

- [org.xml.sax.ContentHandler#setDocumentLocator](../org/xml/sax/ContentHandler.md))
- [org.xml.sax.Locator](../org/xml/sax/Locator.md) 

### skippedEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skippedEntity(name: String!): Unit
```

Receive notification of a skipped entity.

By default, do nothing. Application writers may override this method in a subclass to take specific actions for each processing instruction, such as setting status variables or invoking other methods.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the skipped entity. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ContentHandler#processingInstruction](../org/xml/sax/ContentHandler.md)) 

### startDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startDocument(): Unit
```

Receive notification of the beginning of the document.

By default, do nothing. Application writers may override this method in a subclass to take specific actions at the beginning of a document (such as allocating the root node of a tree or creating an output file).

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ContentHandler#startDocument](../org/xml/sax/ContentHandler.md)) 

### startElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startElement(
    uri: String!, 
    localName: String!, 
    qName: String!, 
    attributes: Attributes!
): Unit
```

Receive notification of the start of an element.

By default, do nothing. Application writers may override this method in a subclass to take specific actions at the start of each element (such as allocating a new tree node or writing output to a file).

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty string if the element has no Namespace URI or if Namespace processing is not being performed. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The local name (without prefix), or the empty string if Namespace processing is not being performed. |
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified name (with prefix), or the empty string if qualified names are not available. |
| --- | --- |
| `atts` | the attributes attached to the element. If there are no attributes, it shall be an empty Attributes object. The value of this object after startElement returns is undefined |
| `attributes` | [Attributes](../org/xml/sax/Attributes.md)!:The attributes attached to the element. If there are no attributes, it shall be an empty Attributes object. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | any SAX exception, possibly wrapping another exception |
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ContentHandler#startElement](../org/xml/sax/ContentHandler.md)) 

### startPrefixMapping

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startPrefixMapping(
    prefix: String!, 
    uri: String!
): Unit
```

Receive notification of the start of a Namespace mapping.

By default, do nothing. Application writers may override this method in a subclass to take specific actions at the start of each Namespace prefix scope (such as storing the prefix mapping).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace prefix being declared. |
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI mapped to the prefix. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | the client may throw an exception during processing |
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ContentHandler#startPrefixMapping](../org/xml/sax/ContentHandler.md)) 

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

Receive notification of an unparsed entity declaration.

By default, do nothing. Application writers may override this method in a subclass to keep track of the unparsed entities declared in a document.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity name. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity public identifier, or null if not available. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity system identifier. |
| --- | --- |
| `notationName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the associated notation. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.DTDHandler#unparsedEntityDecl](../org/xml/sax/DTDHandler.md)) 

### warning

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun warning(e: SAXParseException!): Unit
```

Receive notification of a parser warning.

The default implementation does nothing. Application writers may override this method in a subclass to take specific actions for each warning, such as inserting the message in a log file or printing it to the console.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | The warning information encapsulated in a SAX parse exception. |
| `e` | [SAXParseException](../org/xml/sax/SAXParseException.md)!:The warning information encoded as an exception. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ErrorHandler#warning](../org/xml/sax/ErrorHandler.md))
- [org.xml.sax.SAXParseException](../org/xml/sax/SAXParseException.md)
