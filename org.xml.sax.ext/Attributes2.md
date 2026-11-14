# Attributes2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Attributes2

```
interface Attributes2 : Attributes
```

| [org.xml.sax.ext.Attributes2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2#) |

| Known Direct Subclasses [Attributes2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2Impl) |---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Attributes2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2Impl) | SAX2 extension helper for additional Attributes information, implementing the [Attributes2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2#) interface. | |

SAX2 extension to augment the per-attribute information provided though [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#). If an implementation supports this extension, the attributes provided in [ContentHandler.startElement()](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startElement(kotlin.String,%20kotlin.String,%20kotlin.String,%20org.xml.sax.Attributes))will implement this interface, and the*http://xml.org/sax/features/use-attributes2* feature flag will have the value*true* .*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.*

XMLReader implementations are not required to support this information, and it is not part of core-only SAX2 distributions.

Note that if an attribute was defaulted (*!isSpecified()* ) it will of necessity also have been declared (*isDeclared()*) in the DTD. Similarly if an attribute's type is anything except CDATA, then it must have been declared.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDeclared](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2#isDeclared(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns false unless the attribute was declared in the DTD. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDeclared](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2#isDeclared(kotlin.String))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns false unless the attribute was declared in the DTD. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDeclared](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2#isDeclared(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns false unless the attribute was declared in the DTD. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpecified](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2#isSpecified(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true unless the attribute value was provided by DTD defaulting. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpecified](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2#isSpecified(kotlin.String))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns true unless the attribute value was provided by DTD defaulting. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpecified](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2#isSpecified(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns true unless the attribute value was provided by DTD defaulting. |

| Inherited functions ||
|---|---|
| From class [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#) |-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getIndex(kotlin.String))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Look up the index of an attribute by XML qualified (prefixed) name. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getIndex(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Look up the index of an attribute by Namespace name. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getLength())`()` <br /> Return the number of attributes in the list. Once you know the number of attributes, you can iterate through the list. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocalName](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getLocalName(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Look up an attribute's local name by index. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getQName](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getQName(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Look up an attribute's XML qualified (prefixed) name by index. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getType(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Look up an attribute's type by index. The attribute type is one of the strings "CDATA", "ID", "IDREF", "IDREFS", "NMTOKEN", "NMTOKENS", "ENTITY", "ENTITIES", or "NOTATION" (always in upper case). If the parser has not read a declaration for the attribute, or if the parser does not report attribute types, then it must return the value "CDATA" as stated in the XML 1.0 Recommendation (clause 3.3.3, "Attribute-Value Normalization"). For an enumerated attribute that is not a notation, the parser will report the type as "NMTOKEN". <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getType(kotlin.String))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Look up an attribute's type by XML qualified (prefixed) name. See [getType(int)](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getType(kotlin.Int))for a description of the possible types. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getType(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Look up an attribute's type by Namespace name. See [getType(int)](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getType(kotlin.Int))for a description of the possible types. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getURI](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getURI(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Look up an attribute's Namespace URI by index. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getValue(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Look up an attribute's value by index. If the attribute value is a list of tokens (IDREFS, ENTITIES, or NMTOKENS), the tokens will be concatenated into a single string with each token separated by a single space. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getValue(kotlin.String))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Look up an attribute's value by XML qualified (prefixed) name. See [getValue(int)](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getValue(kotlin.Int))for a description of the possible values. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getValue(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Look up an attribute's value by Namespace name. See [getValue(int)](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#getValue(kotlin.Int))for a description of the possible values. <br /> | ||

## Public methods

### isDeclared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDeclared(index: Int): Boolean
```

Returns false unless the attribute was declared in the DTD. This helps distinguish two kinds of attributes that SAX reports as CDATA: ones that were declared (and hence are usually valid), and those that were not (and which are never valid).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute index (zero-based). |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the attribute was declared in the DTD, false otherwise. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | When the supplied index does not identify an attribute. |

### isDeclared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDeclared(qName: String!): Boolean
```

Returns false unless the attribute was declared in the DTD. This helps distinguish two kinds of attributes that SAX reports as CDATA: ones that were declared (and hence are usually valid), and those that were not (and which are never valid).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------|
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The XML qualified (prefixed) name. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the attribute was declared in the DTD, false otherwise. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------|
| `java.lang.IllegalArgumentException` | When the supplied name does not identify an attribute. |

### isDeclared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDeclared(
    uri: String!, 
    localName: String!
): Boolean
```

Returns false unless the attribute was declared in the DTD. This helps distinguish two kinds of attributes that SAX reports as CDATA: ones that were declared (and hence are usually valid), and those that were not (and which are never valid).

Remember that since DTDs do not "understand" namespaces, the namespace URI associated with an attribute may not have come from the DTD. The declaration will have applied to the attribute's*qName*.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty string if the name has no Namespace URI. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute's local name. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the attribute was declared in the DTD, false otherwise. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | When the supplied names do not identify an attribute. |

### isSpecified

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSpecified(index: Int): Boolean
```

Returns true unless the attribute value was provided by DTD defaulting.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute index (zero-based). |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the value was found in the XML text, false if the value was provided by DTD defaulting. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | When the supplied index does not identify an attribute. |

### isSpecified

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSpecified(qName: String!): Boolean
```

Returns true unless the attribute value was provided by DTD defaulting.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------|
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The XML qualified (prefixed) name. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the value was found in the XML text, false if the value was provided by DTD defaulting. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------|
| `java.lang.IllegalArgumentException` | When the supplied name does not identify an attribute. |

### isSpecified

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSpecified(
    uri: String!, 
    localName: String!
): Boolean
```

Returns true unless the attribute value was provided by DTD defaulting.

Remember that since DTDs do not "understand" namespaces, the namespace URI associated with an attribute may not have come from the DTD. The declaration will have applied to the attribute's*qName*.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty string if the name has no Namespace URI. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute's local name. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the value was found in the XML text, false if the value was provided by DTD defaulting. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | When the supplied names do not identify an attribute. |
