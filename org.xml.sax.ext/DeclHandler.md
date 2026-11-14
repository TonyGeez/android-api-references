# DeclHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeclHandler

```
interface DeclHandler
```

| [org.xml.sax.ext.DeclHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler#) |

| Known Direct Subclasses [DefaultHandler2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2) |---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DefaultHandler2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2) | This class extends the SAX2 base handler class to support the SAX2 [LexicalHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler), [DeclHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler#), and [EntityResolver2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/EntityResolver2) extensions. | |

SAX2 extension handler for DTD declaration events.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This is an optional extension handler for SAX2 to provide more complete information about DTD declarations in an XML document. XML readers are not required to recognize this handler, and it is not part of core-only SAX2 distributions.

Note that data-related DTD declarations (unparsed entities and notations) are already reported through the interface.

If you are using the declaration handler together with a lexical handler, all of the events will occur between the [startDTD](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#startDTD(kotlin.String,%20kotlin.String,%20kotlin.String))and the [endDTD](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#endDTD())events.

To set the DeclHandler for an XML reader, use the [setProperty](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#setProperty(kotlin.String,%20kotlin.Any))method with the property name`http://xml.org/sax/properties/declaration-handler`and an object implementing this interface (or null) as the value. If the reader does not report declaration events, it will throw a [SAXNotRecognizedException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXNotRecognizedException.html#) when you attempt to register the handler.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attributeDecl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler#attributeDecl(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`eName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `aName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Report an attribute type declaration. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [elementDecl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler#elementDecl(kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `model:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Report an element type declaration. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [externalEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler#externalEntityDecl(kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Report a parsed external entity declaration. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [internalEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler#internalEntityDecl(kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Report an internal entity declaration. |

## Public methods

### attributeDecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun attributeDecl(
    eName: String!, 
    aName: String!, 
    type: String!, 
    mode: String!, 
    value: String!
): Unit
```

Report an attribute type declaration.

Only the effective (first) declaration for an attribute will be reported. The type will be one of the strings "CDATA", "ID", "IDREF", "IDREFS", "NMTOKEN", "NMTOKENS", "ENTITY", "ENTITIES", a parenthesized token group with the separator "|" and all whitespace removed, or the word "NOTATION" followed by a space followed by a parenthesized token group with all whitespace removed.

The value will be the value as reported to applications, appropriately normalized and with entity and character references expanded.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `eName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the associated element. |
| `aName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the attribute. |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string representing the attribute type. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string representing the attribute defaulting mode ("#IMPLIED", "#REQUIRED", or "#FIXED") or null if none of these applies. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string representing the attribute's default value, or null if there is none. |

| Exceptions ||
|----------------------------|-----------------------------------------|
| `org.xml.sax.SAXException` | The application may raise an exception. |

### elementDecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun elementDecl(
    name: String!, 
    model: String!
): Unit
```

Report an element type declaration.

The content model will consist of the string "EMPTY", the string "ANY", or a parenthesised group, optionally followed by an occurrence indicator. The model will be normalized so that all parameter entities are fully resolved and all whitespace is removed,and will include the enclosing parentheses. Other normalization (such as removing redundant parentheses or simplifying occurrence indicators) is at the discretion of the parser.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The element type name. |
| `model` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The content model as a normalized string. |

| Exceptions ||
|----------------------------|-----------------------------------------|
| `org.xml.sax.SAXException` | The application may raise an exception. |

### externalEntityDecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun externalEntityDecl(
    name: String!, 
    publicId: String!, 
    systemId: String!
): Unit
```

Report a parsed external entity declaration.

Only the effective (first) declaration for each entity will be reported.

If the system identifier is a URL, the parser must resolve it fully before passing it to the application.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the entity. If it is a parameter entity, the name will begin with '%'. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity's public identifier, or null if none was given. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity's system identifier. |

| Exceptions ||
|----------------------------|-----------------------------------------|
| `org.xml.sax.SAXException` | The application may raise an exception. |

**See Also**

- [#internalEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler#internalEntityDecl(kotlin.String,%20kotlin.String))
- [org.xml.sax.DTDHandler#unparsedEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#unparsedEntityDecl(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String)) 

### internalEntityDecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun internalEntityDecl(
    name: String!, 
    value: String!
): Unit
```

Report an internal entity declaration.

Only the effective (first) declaration for each entity will be reported. All parameter entities in the value will be expanded, but general entities will not.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the entity. If it is a parameter entity, the name will begin with '%'. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The replacement text of the entity. |

| Exceptions ||
|----------------------------|-----------------------------------------|
| `org.xml.sax.SAXException` | The application may raise an exception. |

**See Also**

- [#externalEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler#externalEntityDecl(kotlin.String,%20kotlin.String,%20kotlin.String))
- [org.xml.sax.DTDHandler#unparsedEntityDecl](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#unparsedEntityDecl(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))
