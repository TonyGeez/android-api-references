# HandlerBase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HandlerBase

```
open class HandlerBase : DTDHandler, DocumentHandler, EntityResolver, ErrorHandler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#) |

| **This class was deprecated in API level 9.**
|
| This class works with the deprecated [DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler) interface. It has been replaced by the SAX2 [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler) class.

Default base class for handlers.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This class implements the default behaviour for four SAX1 interfaces: EntityResolver, DTDHandler, DocumentHandler, and ErrorHandler. It is now obsolete, but is included in SAX2 to support legacy SAX1 applications. SAX2 applications should use the [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler) class instead.

Application writers can extend this class when they need to implement only part of an interface; parser writers can instantiate this class to provide default handlers when the application has not supplied its own.

Note that the use of this class is optional.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------|---|
| [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#HandlerBase())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [characters](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#characters(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Receive notification of character data inside an element. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endDocument](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#endDocument())`()` Receive notification of the end of the document. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endElement](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#endElement(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of the end of an element. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [error](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#error(org.xml.sax.SAXParseException))`(`e:` ` [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)!`)` Receive notification of a recoverable parser error. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fatalError](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#fatalError(org.xml.sax.SAXParseException))`(`e:` ` [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)!`)` Report a fatal XML parsing error. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ignorableWhitespace](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#ignorableWhitespace(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Receive notification of ignorable whitespace in element content. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notationDecl](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#notationDecl(kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of a notation declaration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [processingInstruction](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#processingInstruction(kotlin.String,%20kotlin.String))`(`target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of a processing instruction. |
| open [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource)! | [resolveEntity](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#resolveEntity(kotlin.String,%20kotlin.String))`(`publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Resolve an external entity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentLocator](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#setDocumentLocator(org.xml.sax.Locator))`(`locator:` ` [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator)!`)` Receive a Locator object for document events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDocument](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#startDocument())`()` Receive notification of the beginning of the document. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startElement](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#startElement(kotlin.String,%20org.xml.sax.AttributeList))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attributes:` ` [AttributeList](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList)!`)` Receive notification of the start of an element. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unparsedEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#unparsedEntityDecl(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `notationName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Receive notification of an unparsed entity declaration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [warning](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase#warning(org.xml.sax.SAXParseException))`(`e:` ` [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)!`)` Receive notification of a parser warning. |

## Public constructors

### HandlerBase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HandlerBase()
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

**Deprecated:** *Deprecated in Java.*

Receive notification of character data inside an element.

By default, do nothing. Application writers may override this method to take specific actions for each chunk of character data (such as adding the data to a node or buffer, or printing it to a file).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The characters. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The start position in the character array. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to use from the character array. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.DocumentHandler#characters](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler#characters(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)) 

### endDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endDocument(): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of the end of the document.

By default, do nothing. Application writers may override this method in a subclass to take specific actions at the beginning of a document (such as finalising a tree or closing an output file).

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.DocumentHandler#endDocument](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler#endDocument()) 

### endElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endElement(name: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of the end of an element.

By default, do nothing. Application writers may override this method in a subclass to take specific actions at the end of each element (such as finalising a tree node or writing output to a file).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the element name |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.DocumentHandler#endElement](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler#endElement(kotlin.String)) 

### error

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun error(e: SAXParseException!): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of a recoverable parser error.

The default implementation does nothing. Application writers may override this method in a subclass to take specific actions for each error, such as inserting the message in a log file or printing it to the console.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | The error information encapsulated in a SAX parse exception. |
| `e` | [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)!:The warning information encoded as an exception. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ErrorHandler#warning](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler#warning(org.xml.sax.SAXParseException))
- [org.xml.sax.SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException) 

### fatalError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fatalError(e: SAXParseException!): Unit
```

**Deprecated:** *Deprecated in Java.*

Report a fatal XML parsing error.

The default implementation throws a SAXParseException. Application writers may override this method in a subclass if they need to take specific actions for each fatal error (such as collecting all of the errors into a single report): in any case, the application must stop all regular processing when this method is invoked, since the document is no longer reliable, and the parser may no longer report parsing events.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | The error information encapsulated in a SAX parse exception. |
| `e` | [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)!:The error information encoded as an exception. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ErrorHandler#fatalError](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler#fatalError(org.xml.sax.SAXParseException))
- [org.xml.sax.SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException) 

### ignorableWhitespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ignorableWhitespace(
    ch: CharArray!, 
    start: Int, 
    length: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of ignorable whitespace in element content.

By default, do nothing. Application writers may override this method to take specific actions for each chunk of ignorable whitespace (such as adding data to a node or buffer, or printing it to a file).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The whitespace characters. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The start position in the character array. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to use from the character array. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.DocumentHandler#ignorableWhitespace](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler#ignorableWhitespace(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)) 

### notationDecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notationDecl(
    name: String!, 
    publicId: String!, 
    systemId: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of a notation declaration.

By default, do nothing. Application writers may override this method in a subclass if they wish to keep track of the notations declared in a document.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The notation name. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The notation public identifier, or null if not available. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The notation system identifier. |

**See Also**

- [org.xml.sax.DTDHandler#notationDecl](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler#notationDecl(kotlin.String,%20kotlin.String,%20kotlin.String)) 

### processingInstruction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun processingInstruction(
    target: String!, 
    data: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of a processing instruction.

By default, do nothing. Application writers may override this method in a subclass to take specific actions for each processing instruction, such as setting status variables or invoking other methods.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The processing instruction target. |
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The processing instruction data, or null if none is supplied. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.DocumentHandler#processingInstruction](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler#processingInstruction(kotlin.String,%20kotlin.String)) 

### resolveEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resolveEntity(
    publicId: String!, 
    systemId: String!
): InputSource!
```

**Deprecated:** *Deprecated in Java.*

Resolve an external entity.

Always return null, so that the parser will use the system identifier provided in the XML document. This method implements the SAX default behaviour: application writers can override it in a subclass to do special translations such as catalog lookups or URI redirection.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The public identifier, or null if none is available. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier provided in the XML document. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource)! | The new input source, or null to require the default behaviour. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.EntityResolver#resolveEntity](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver#resolveEntity(kotlin.String,%20kotlin.String)) 

### setDocumentLocator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDocumentLocator(locator: Locator!): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive a Locator object for document events.

By default, do nothing. Application writers may override this method in a subclass if they wish to store the locator for use with other document events.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `locator` | [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator)!:A locator for all SAX document events. |

**See Also**

- [org.xml.sax.DocumentHandler#setDocumentLocator](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler#setDocumentLocator(org.xml.sax.Locator))
- [org.xml.sax.Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator) 

### startDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startDocument(): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of the beginning of the document.

By default, do nothing. Application writers may override this method in a subclass to take specific actions at the beginning of a document (such as allocating the root node of a tree or creating an output file).

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.DocumentHandler#startDocument](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler#startDocument()) 

### startElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startElement(
    name: String!, 
    attributes: AttributeList!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of the start of an element.

By default, do nothing. Application writers may override this method in a subclass to take specific actions at the start of each element (such as allocating a new tree node or writing output to a file).

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The element type name. |
| `atts` | The attributes attached to the element, if any. |
| `attributes` | [AttributeList](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList)!:The specified or defaulted attributes. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.DocumentHandler#startElement](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler#startElement(kotlin.String,%20org.xml.sax.AttributeList)) 

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

**Deprecated:** *Deprecated in Java.*

Receive notification of an unparsed entity declaration.

By default, do nothing. Application writers may override this method in a subclass to keep track of the unparsed entities declared in a document.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity name. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity public identifier, or null if not available. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity system identifier. |
| `notationName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the associated notation. |

**See Also**

- [org.xml.sax.DTDHandler#unparsedEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler#unparsedEntityDecl(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String)) 

### warning

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun warning(e: SAXParseException!): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive notification of a parser warning.

The default implementation does nothing. Application writers may override this method in a subclass to take specific actions for each warning, such as inserting the message in a log file or printing it to the console.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | The warning information encapsulated in a SAX parse exception. |
| `e` | [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)!:The warning information encoded as an exception. |

| Exceptions ||
|----------------------------|---------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

**See Also**

- [org.xml.sax.ErrorHandler#warning](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler#warning(org.xml.sax.SAXParseException))
- [org.xml.sax.SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException)
