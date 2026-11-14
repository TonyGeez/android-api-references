# Attributes2Impl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Attributes2Impl

```
open class Attributes2Impl : AttributesImpl, Attributes2
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [org.xml.sax.helpers.AttributesImpl](../org/xml/sax/helpers/AttributesImpl.md) ||
| | ↳ | [org.xml.sax.ext.Attributes2Impl](../org/xml/sax/ext/Attributes2Impl.md) |

SAX2 extension helper for additional Attributes information, implementing the [Attributes2](../org/xml/sax/ext/Attributes2.md) interface.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.*

This is not part of core-only SAX2 distributions.

The*specified* flag for each attribute will always be true, unless it has been set to false in the copy constructor or using [setSpecified](../org/xml/sax/ext/Attributes2Impl.md)). Similarly, the*declared* flag for each attribute will always be false, except for defaulted attributes (*specified* is false), non-CDATA attributes, or when it is set to true using [setDeclared](../org/xml/sax/ext/Attributes2Impl.md)). If you change an attribute's type by hand, you may need to modify its*declared*flag to match.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Attributes2Impl](../org/xml/sax/ext/Attributes2Impl.md))`()` Construct a new, empty Attributes2Impl object. |
| [Attributes2Impl](../org/xml/sax/ext/Attributes2Impl.md))`(`atts:` ` [Attributes](../org/xml/sax/Attributes.md)!`)` Copy an existing Attributes or Attributes2 object. |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAttribute](../org/xml/sax/ext/Attributes2Impl.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Add an attribute to the end of the list, setting its "specified" flag to true. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDeclared](../org/xml/sax/ext/Attributes2Impl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDeclared](../org/xml/sax/ext/Attributes2Impl.md))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDeclared](../org/xml/sax/ext/Attributes2Impl.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpecified](../org/xml/sax/ext/Attributes2Impl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the current value of an attribute's "specified" flag. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpecified](../org/xml/sax/ext/Attributes2Impl.md))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the current value of an attribute's "specified" flag. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpecified](../org/xml/sax/ext/Attributes2Impl.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the current value of an attribute's "specified" flag. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAttribute](../org/xml/sax/ext/Attributes2Impl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAttributes](../org/xml/sax/ext/Attributes2Impl.md))`(`atts:` ` [Attributes](../org/xml/sax/Attributes.md)!`)` Copy an entire Attributes object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDeclared](../org/xml/sax/ext/Attributes2Impl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Assign a value to the "declared" flag of a specific attribute. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpecified](../org/xml/sax/ext/Attributes2Impl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Assign a value to the "specified" flag of a specific attribute. |

| Inherited functions ||
|---|---|
| From class [AttributesImpl](../org/xml/sax/helpers/AttributesImpl.md) |-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../org/xml/sax/helpers/AttributesImpl.md))`()` <br /> Clear the attribute list for reuse. Note that little memory is freed by this call: the current array is kept so it can be reused. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](../org/xml/sax/helpers/AttributesImpl.md))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Look up an attribute's index by qualified (prefixed) name. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](../org/xml/sax/helpers/AttributesImpl.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Look up an attribute's index by Namespace name. In many cases, it will be more efficient to look up the name once and use the index query methods rather than using the name query methods repeatedly. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](../org/xml/sax/helpers/AttributesImpl.md))`()` <br /> Return the number of attributes in the list. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocalName](../org/xml/sax/helpers/AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return an attribute's local name. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getQName](../org/xml/sax/helpers/AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return an attribute's qualified (prefixed) name. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](../org/xml/sax/helpers/AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return an attribute's type by index. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](../org/xml/sax/helpers/AttributesImpl.md))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Look up an attribute's type by qualified (prefixed) name. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](../org/xml/sax/helpers/AttributesImpl.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Look up an attribute's type by Namespace-qualified name. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getURI](../org/xml/sax/helpers/AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return an attribute's Namespace URI. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](../org/xml/sax/helpers/AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return an attribute's value by index. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](../org/xml/sax/helpers/AttributesImpl.md))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Look up an attribute's value by qualified (prefixed) name. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](../org/xml/sax/helpers/AttributesImpl.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Look up an attribute's value by Namespace-qualified name. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAttribute](../org/xml/sax/helpers/AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Set an attribute in the list. For the sake of speed, this method does no checking for name conflicts or well-formedness: such checks are the responsibility of the application. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocalName](../org/xml/sax/helpers/AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Set the local name of a specific attribute. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setQName](../org/xml/sax/helpers/AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Set the qualified name of a specific attribute. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setType](../org/xml/sax/helpers/AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Set the type of a specific attribute. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setURI](../org/xml/sax/helpers/AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Set the Namespace URI of a specific attribute. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setValue](../org/xml/sax/helpers/AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Set the value of a specific attribute. <br /> | ||

## Public constructors

### Attributes2Impl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Attributes2Impl()
```

Construct a new, empty Attributes2Impl object. 

### Attributes2Impl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Attributes2Impl(atts: Attributes!)
```

Copy an existing Attributes or Attributes2 object. If the object implements Attributes2, values of the*specified* and*declared* flags for each attribute are copied. Otherwise the flag values are defaulted to assume no DTD was used, unless there is evidence to the contrary (such as attributes with type other than CDATA, which must have been*declared*).

This constructor is especially useful inside a [startElement](../org/xml/sax/ContentHandler.md))event.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------|
| `atts` | [Attributes](../org/xml/sax/Attributes.md)!:The existing Attributes object. |

## Public methods

### addAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAttribute(
    uri: String!, 
    localName: String!, 
    qName: String!, 
    type: String!, 
    value: String!
): Unit
```

Add an attribute to the end of the list, setting its "specified" flag to true. To set that flag's value to false, use [setSpecified](../org/xml/sax/ext/Attributes2Impl.md)).

Unless the attribute*type* is CDATA, this attribute is marked as being declared in the DTD. To set that flag's value to true for CDATA attributes, use [setDeclared](../org/xml/sax/ext/Attributes2Impl.md)).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty string if none is available or Namespace processing is not being performed. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The local name, or the empty string if Namespace processing is not being performed. |
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified (prefixed) name, or the empty string if qualified names are not available. |
| --- | --- |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute type as a string. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute value. |

**See Also**

- [org.xml.sax.helpers.AttributesImpl#addAttribute](../org/xml/sax/helpers/AttributesImpl.md)) 

### isDeclared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDeclared(index: Int): Boolean
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute index (zero-based). |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the attribute was declared in the DTD, false otherwise. |

### isDeclared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDeclared(qName: String!): Boolean
```

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------|
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The XML qualified (prefixed) name. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the attribute was declared in the DTD, false otherwise. |

### isDeclared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDeclared(
    uri: String!, 
    localName: String!
): Boolean
```

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty string if the name has no Namespace URI. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute's local name. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the attribute was declared in the DTD, false otherwise. |

### isSpecified

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSpecified(index: Int): Boolean
```

Returns the current value of an attribute's "specified" flag.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute index (zero-based). |

| Return ||
|------------------------------------------------------------------------------------|--------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | current flag value |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | When the supplied index does not identify an attribute. |

### isSpecified

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSpecified(qName: String!): Boolean
```

Returns the current value of an attribute's "specified" flag.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------|
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The XML qualified (prefixed) name. |

| Return ||
|------------------------------------------------------------------------------------|--------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | current flag value |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------|
| `java.lang.IllegalArgumentException` | When the supplied name does not identify an attribute. |

### isSpecified

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSpecified(
    uri: String!, 
    localName: String!
): Boolean
```

Returns the current value of an attribute's "specified" flag.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty string if the name has no Namespace URI. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute's local name. |

| Return ||
|------------------------------------------------------------------------------------|--------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | current flag value |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | When the supplied names do not identify an attribute. |

### removeAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAttribute(index: Int): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute (zero-based). |

### setAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAttributes(atts: Attributes!): Unit
```

Copy an entire Attributes object. The "specified" flags are assigned as true, and "declared" flags as false (except when an attribute's type is not CDATA), unless the object is an Attributes2 object. In that case those flag values are all copied.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------|
| `atts` | [Attributes](../org/xml/sax/Attributes.md)!:The attributes to copy. |

**See Also**

- [org.xml.sax.helpers.AttributesImpl#setAttributes](../org/xml/sax/helpers/AttributesImpl.md)) 

### setDeclared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDeclared(
    index: Int, 
    value: Boolean
): Unit
```

Assign a value to the "declared" flag of a specific attribute. This is normally needed only for attributes of type CDATA, including attributes whose type is changed to or from CDATA.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute (zero-based). |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The desired flag value. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | When the supplied index does not identify an attribute. |

**See Also**

- [#setType](../org/xml/sax/helpers/AttributesImpl.md)) 

### setSpecified

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSpecified(
    index: Int, 
    value: Boolean
): Unit
```

Assign a value to the "specified" flag of a specific attribute. This is the only way this flag can be cleared, except clearing by initialization with the copy constructor.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute (zero-based). |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The desired flag value. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | When the supplied index does not identify an attribute. |
