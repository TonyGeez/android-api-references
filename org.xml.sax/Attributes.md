# Attributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Attributes

```
interface Attributes
```

| [org.xml.sax.Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#) |

| Known Direct Subclasses [Attributes2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2), [AttributesImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributesImpl), [Driver](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver.html#) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Attributes2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2) | SAX2 extension to augment the per-attribute information provided though [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#). | | [AttributesImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributesImpl) | Default implementation of the Attributes interface. | | [Driver](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver.html#) | SAX2 Driver that pulls events from XmlPullParser and converts them into SAX2 callbacks. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [Attributes2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2Impl) [Attributes2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2Impl) |---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Attributes2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2Impl) | SAX2 extension helper for additional Attributes information, implementing the [Attributes2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2) interface. | | [Attributes2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2Impl) | SAX2 extension helper for additional Attributes information, implementing the [Attributes2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Attributes2) interface. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface for a list of XML attributes.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This interface allows access to a list of attributes in three different ways:

1. by attribute index;
2. by Namespace-qualified name; or
3. by qualified (prefixed) name.

The list will not contain attributes that were declared #IMPLIED but not specified in the start tag. It will also not contain attributes used as Namespace declarations (xmlns\*) unless the`http://xml.org/sax/features/namespace-prefixes`feature is set to true (it is false by default). Because SAX2 conforms to the original "Namespaces in XML" recommendation, it normally does not give namespace declaration attributes a namespace URI.

Some SAX2 parsers may support using an optional feature flag (`http://xml.org/sax/features/xmlns-uris`) to request that those attributes be given URIs, conforming to a later backwards-incompatible revision of that recommendation. (The attribute's "local name" will be the prefix, or "xmlns" when defining a default element namespace.) For portability, handler code should always resolve that conflict, rather than requiring parsers that can change the setting of that feature flag.

If the namespace-prefixes feature (see above) is false, access by qualified name may not be available; if the`http://xml.org/sax/features/namespaces`feature is false, access by Namespace-qualified names may not be available.

This interface replaces the now-deprecated SAX1 interface, which does not contain Namespace support. In addition to Namespace support, it adds the getIndex methods (below).

The order of attributes in the list is unspecified, and will vary from implementation to implementation.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getIndex(kotlin.String))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the index of an attribute by XML qualified (prefixed) name. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getIndex(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the index of an attribute by Namespace name. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getLength())`()` Return the number of attributes in the list. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocalName](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getLocalName(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Look up an attribute's local name by index. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getQName](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getQName(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Look up an attribute's XML qualified (prefixed) name by index. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getType(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Look up an attribute's type by index. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getType(kotlin.String))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up an attribute's type by XML qualified (prefixed) name. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getType(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up an attribute's type by Namespace name. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getURI](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getURI(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Look up an attribute's Namespace URI by index. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getValue(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Look up an attribute's value by index. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getValue(kotlin.String))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up an attribute's value by XML qualified (prefixed) name. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getValue(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up an attribute's value by Namespace name. |
| --- | --- |

## Public methods

### getIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIndex(qName: String!): Int
```

Look up the index of an attribute by XML qualified (prefixed) name.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified (prefixed) name. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index of the attribute, or -1 if it does not appear in the list. |

### getIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIndex(
    uri: String!, 
    localName: String!
): Int
```

Look up the index of an attribute by Namespace name.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty string if the name has no Namespace URI. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute's local name. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index of the attribute, or -1 if it does not appear in the list. |

### getLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLength(): Int
```

Return the number of attributes in the list.

Once you know the number of attributes, you can iterate through the list.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of attributes in the list. |

**See Also**

- [#getURI(int)](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getURI(kotlin.Int))
- [#getLocalName(int)](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getLocalName(kotlin.Int))
- [#getQName(int)](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getQName(kotlin.Int))
- [#getType(int)](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getType(kotlin.Int))
- [#getValue(int)](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getValue(kotlin.Int)) 

### getLocalName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLocalName(index: Int): String!
```

Look up an attribute's local name by index.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The local name, or the empty string if Namespace processing is not being performed, or null if the index is out of range. |

**See Also**

- [#getLength](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getLength()) 

### getQName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getQName(index: Int): String!
```

Look up an attribute's XML qualified (prefixed) name by index.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The XML qualified name, or the empty string if none is available, or null if the index is out of range. |

**See Also**

- [#getLength](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getLength()) 

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getType(index: Int): String!
```

Look up an attribute's type by index.

The attribute type is one of the strings "CDATA", "ID", "IDREF", "IDREFS", "NMTOKEN", "NMTOKENS", "ENTITY", "ENTITIES", or "NOTATION" (always in upper case).

If the parser has not read a declaration for the attribute, or if the parser does not report attribute types, then it must return the value "CDATA" as stated in the XML 1.0 Recommendation (clause 3.3.3, "Attribute-Value Normalization").

For an enumerated attribute that is not a notation, the parser will report the type as "NMTOKEN".

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute's type as a string, or null if the index is out of range. |

**See Also**

- [#getLength](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getLength()) 

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getType(qName: String!): String!
```

Look up an attribute's type by XML qualified (prefixed) name.

See [getType(int)](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getType(kotlin.Int))for a description of the possible types.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------|
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The XML qualified name. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute type as a string, or null if the attribute is not in the list or if qualified names are not available. |

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getType(
    uri: String!, 
    localName: String!
): String!
```

Look up an attribute's type by Namespace name.

See [getType(int)](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getType(kotlin.Int))for a description of the possible types.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty String if the name has no Namespace URI. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The local name of the attribute. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute type as a string, or null if the attribute is not in the list or if Namespace processing is not being performed. |

### getURI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getURI(index: Int): String!
```

Look up an attribute's Namespace URI by index.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The Namespace URI, or the empty string if none is available, or null if the index is out of range. |

**See Also**

- [#getLength](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getLength()) 

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getValue(index: Int): String!
```

Look up an attribute's value by index.

If the attribute value is a list of tokens (IDREFS, ENTITIES, or NMTOKENS), the tokens will be concatenated into a single string with each token separated by a single space.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute's value as a string, or null if the index is out of range. |

**See Also**

- [#getLength](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getLength()) 

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getValue(qName: String!): String!
```

Look up an attribute's value by XML qualified (prefixed) name.

See [getValue(int)](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getValue(kotlin.Int))for a description of the possible values.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------|
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The XML qualified name. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute value as a string, or null if the attribute is not in the list or if qualified names are not available. |

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getValue(
    uri: String!, 
    localName: String!
): String!
```

Look up an attribute's value by Namespace name.

See [getValue(int)](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes#getValue(kotlin.Int))for a description of the possible values.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty String if the name has no Namespace URI. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The local name of the attribute. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute value as a string, or null if the attribute is not in the list. |
