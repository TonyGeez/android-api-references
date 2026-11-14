# DefaultHandler2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DefaultHandler2

```
open class DefaultHandler2 : DefaultHandler, DeclHandler, EntityResolver2, LexicalHandler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [org.xml.sax.helpers.DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#) ||
| | ↳ | [org.xml.sax.ext.DefaultHandler2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#) |

This class extends the SAX2 base handler class to support the SAX2 [LexicalHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler), [DeclHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler), and [EntityResolver2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/EntityResolver2) extensions. Except for overriding the original SAX1 [resolveEntity()](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#resolveEntity(kotlin.String,%20kotlin.String))method the added handler methods just return. Subclassers may override everything on a method-by-method basis.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.*

*Note:* this class might yet learn that the*ContentHandler.setDocumentLocator()* call might be passed a [Locator2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2) object, and that the*ContentHandler.startElement()* call might be passed a [Attributes2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2) object.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DefaultHandler2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#DefaultHandler2())`()` Constructs a handler which ignores all parsing events. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attributeDecl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#attributeDecl(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`eName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `aName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [comment](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#comment(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [elementDecl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#elementDecl(kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `model:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endCDATA](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#endCDATA())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endDTD](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#endDTD())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endEntity](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#endEntity(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [externalEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#externalEntityDecl(kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)! | [getExternalSubset](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#getExternalSubset(kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `baseURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Tells the parser that if no external subset has been declared in the document text, none should be used. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [internalEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#internalEntityDecl(kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)! | [resolveEntity](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#resolveEntity(kotlin.String,%20kotlin.String))`(`publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Invokes org. |
| open [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)! | [resolveEntity](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#resolveEntity(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `baseURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Tells the parser to resolve the systemId against the baseURI and read the entity text from that resulting absolute URI. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startCDATA](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#startCDATA())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDTD](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#startDTD(kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startEntity](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2#startEntity(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [characters](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#characters(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Receive notification of character data inside an element. By default, do nothing. Application writers may override this method to take specific actions for each chunk of character data (such as adding the data to a node or buffer, or printing it to a file). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endDocument](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#endDocument())`()` <br /> Receive notification of the end of the document. By default, do nothing. Application writers may override this method in a subclass to take specific actions at the end of a document (such as finalising a tree or closing an output file). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endElement](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#endElement(kotlin.String,%20kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Receive notification of the end of an element. By default, do nothing. Application writers may override this method in a subclass to take specific actions at the end of each element (such as finalising a tree node or writing output to a file). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endPrefixMapping](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#endPrefixMapping(kotlin.String))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Receive notification of the end of a Namespace mapping. By default, do nothing. Application writers may override this method in a subclass to take specific actions at the end of each prefix mapping. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [error](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#error(org.xml.sax.SAXParseException))`(`e:` ` [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException.html#)!`)` <br /> Receive notification of a recoverable parser error. The default implementation does nothing. Application writers may override this method in a subclass to take specific actions for each error, such as inserting the message in a log file or printing it to the console. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fatalError](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#fatalError(org.xml.sax.SAXParseException))`(`e:` ` [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException.html#)!`)` <br /> Report a fatal XML parsing error. The default implementation throws a SAXParseException. Application writers may override this method in a subclass if they need to take specific actions for each fatal error (such as collecting all of the errors into a single report): in any case, the application must stop all regular processing when this method is invoked, since the document is no longer reliable, and the parser may no longer report parsing events. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ignorableWhitespace](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#ignorableWhitespace(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`ch:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Receive notification of ignorable whitespace in element content. By default, do nothing. Application writers may override this method to take specific actions for each chunk of ignorable whitespace (such as adding data to a node or buffer, or printing it to a file). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notationDecl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#notationDecl(kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Receive notification of a notation declaration. By default, do nothing. Application writers may override this method in a subclass if they wish to keep track of the notations declared in a document. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [processingInstruction](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#processingInstruction(kotlin.String,%20kotlin.String))`(`target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Receive notification of a processing instruction. By default, do nothing. Application writers may override this method in a subclass to take specific actions for each processing instruction, such as setting status variables or invoking other methods. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentLocator](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#setDocumentLocator(org.xml.sax.Locator))`(`locator:` ` [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#)!`)` <br /> Receive a Locator object for document events. By default, do nothing. Application writers may override this method in a subclass if they wish to store the locator for use with other document events. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skippedEntity](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#skippedEntity(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Receive notification of a skipped entity. By default, do nothing. Application writers may override this method in a subclass to take specific actions for each processing instruction, such as setting status variables or invoking other methods. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDocument](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#startDocument())`()` <br /> Receive notification of the beginning of the document. By default, do nothing. Application writers may override this method in a subclass to take specific actions at the beginning of a document (such as allocating the root node of a tree or creating an output file). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startElement](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#startElement(kotlin.String,%20kotlin.String,%20kotlin.String,%20org.xml.sax.Attributes))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attributes:` ` [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#)!`)` <br /> Receive notification of the start of an element. By default, do nothing. Application writers may override this method in a subclass to take specific actions at the start of each element (such as allocating a new tree node or writing output to a file). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startPrefixMapping](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#startPrefixMapping(kotlin.String,%20kotlin.String))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Receive notification of the start of a Namespace mapping. By default, do nothing. Application writers may override this method in a subclass to take specific actions at the start of each Namespace prefix scope (such as storing the prefix mapping). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unparsedEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#unparsedEntityDecl(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `notationName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Receive notification of an unparsed entity declaration. By default, do nothing. Application writers may override this method in a subclass to keep track of the unparsed entities declared in a document. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [warning](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#warning(org.xml.sax.SAXParseException))`(`e:` ` [SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException.html#)!`)` <br /> Receive notification of a parser warning. The default implementation does nothing. Application writers may override this method in a subclass to take specific actions for each warning, such as inserting the message in a log file or printing it to the console. <br /> | ||

## Public constructors

### DefaultHandler2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DefaultHandler2()
```

Constructs a handler which ignores all parsing events.

## Public methods

### attributeDecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun attributeDecl(
    eName: String!, 
    aName: String!, 
    type: String!, 
    mode: String!, 
    value: String!
): Unit
```

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `eName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the associated element. |
| `aName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the attribute. |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string representing the attribute type. |
| --- | --- |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string representing the attribute defaulting mode ("#IMPLIED", "#REQUIRED", or "#FIXED") or null if none of these applies. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string representing the attribute's default value, or null if there is none. |

### comment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun comment(
    ch: CharArray!, 
    start: Int, 
    length: Int
): Unit
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:An array holding the characters in the comment. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The starting position in the array. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to use from the array. |
| --- | --- |

### elementDecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun elementDecl(
    name: String!, 
    model: String!
): Unit
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The element type name. |
| `model` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The content model as a normalized string. |

### endCDATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endCDATA(): Unit
```  

### endDTD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endDTD(): Unit
```  

### endEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endEntity(name: String!): Unit
```

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the entity that is ending. |

### externalEntityDecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun externalEntityDecl(
    name: String!, 
    publicId: String!, 
    systemId: String!
): Unit
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the entity. If it is a parameter entity, the name will begin with '%'. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity's public identifier, or null if none was given. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity's system identifier. |
| --- | --- |

### getExternalSubset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExternalSubset(
    name: String!, 
    baseURI: String!
): InputSource!
```

Tells the parser that if no external subset has been declared in the document text, none should be used.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Identifies the document root element. This name comes from a DOCTYPE declaration (where available) or from the actual root element. The parameter is ignored. |
| `baseURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The document's base URI, serving as an additional hint for selecting the external subset. This is always an absolute URI, unless it is null because the XMLReader was given an InputSource without one. The parameter is ignored. |

| Return ||
|----------------------------------------------------------------------------------------------|----------------|
| [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)! | null (always). |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |
| `java.io.IOException` | Probably indicating a failure to create a new InputStream or Reader, or an illegal URL. |

### internalEntityDecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun internalEntityDecl(
    name: String!, 
    value: String!
): Unit
```

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the entity. If it is a parameter entity, the name will begin with '%'. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The replacement text of the entity. |

### resolveEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resolveEntity(
    publicId: String!, 
    systemId: String!
): InputSource!
```

Invokes org.xml.sax.ext.EntityResolver2#resolveEntity with null entity name and base URI. You only need to override that method to use this class.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The public identifier of the external entity being referenced (normalized as required by the XML specification), or null if none was supplied. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier of the external entity being referenced; either a relative or absolute URI. This is never null when invoked by a SAX2 parser; only declared entities, and any external subset, are resolved by such parsers. |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)! | An InputSource object describing the new input source. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |
| `java.io.IOException` | Probably indicating a failure to create a new InputStream or Reader, or an illegal URL. |

### resolveEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resolveEntity(
    name: String!, 
    publicId: String!, 
    baseURI: String!, 
    systemId: String!
): InputSource!
```

Tells the parser to resolve the systemId against the baseURI and read the entity text from that resulting absolute URI. Note that because the older [DefaultHandler.resolveEntity()](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#resolveEntity(kotlin.String,%20kotlin.String)), method is overridden to call this one, this method may sometimes be invoked with null*name* and*baseURI* , and with the*systemId*already absolutized.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Identifies the external entity being resolved. Either "\[dtd\]" for the external subset, or a name starting with "%" to indicate a parameter entity, or else the name of a general entity. This is never null when invoked by a SAX2 parser. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The public identifier of the external entity being referenced (normalized as required by the XML specification), or null if none was supplied. |
| `baseURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The URI with respect to which relative systemIDs are interpreted. This is always an absolute URI, unless it is null (likely because the XMLReader was given an InputSource without one). This URI is defined by the XML specification to be the one associated with the "\<" starting the relevant declaration. |
| --- | --- |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier of the external entity being referenced; either a relative or absolute URI. This is never null when invoked by a SAX2 parser; only declared entities, and any external subset, are resolved by such parsers. |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)! | An InputSource object describing the new input source. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |
| `java.io.IOException` | Probably indicating a failure to create a new InputStream or Reader, or an illegal URL. |

### startCDATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startCDATA(): Unit
```  

### startDTD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startDTD(
    name: String!, 
    publicId: String!, 
    systemId: String!
): Unit
```

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The document type name. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The declared public identifier for the external DTD subset, or null if none was declared. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The declared system identifier for the external DTD subset, or null if none was declared. (Note that this is not resolved against the document base URI.) |
| --- | --- |

### startEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startEntity(name: String!): Unit
```

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the entity. If it is a parameter entity, the name will begin with '%', and if it is the external DTD subset, it will be "\[dtd\]". |
