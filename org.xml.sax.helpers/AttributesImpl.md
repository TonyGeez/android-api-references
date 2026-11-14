# AttributesImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AttributesImpl

```
open class AttributesImpl : Attributes
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xml.sax.helpers.AttributesImpl](AttributesImpl.md) |

| Known Direct Subclasses [Attributes2Impl](../org.xml.sax.ext/Attributes2Impl.md) |---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Attributes2Impl](../org.xml.sax.ext/Attributes2Impl.md) | SAX2 extension helper for additional Attributes information, implementing the [Attributes2](../org.xml.sax.ext/Attributes2.md) interface. | |
| --- | --- | --- | --- | --- | --- | --- |

Default implementation of the Attributes interface.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This class provides a default implementation of the SAX2 [Attributes](../org.xml.sax/Attributes.md) interface, with the addition of manipulators so that the list can be modified or reused.

There are two typical uses of this class:

1. to take a persistent snapshot of an Attributes object in a [startElement](../org.xml.sax/ContentHandler.md))event; or
2. to construct or modify an Attributes object in a SAX2 driver or filter.

This class replaces the now-deprecated SAX1 class; in addition to supporting the updated Attributes interface rather than the deprecated [AttributeList](../org.xml.sax/AttributeList.md) interface, it also includes a much more efficient implementation using a single array rather than a set of Vectors.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AttributesImpl](AttributesImpl.md))`()` Construct a new, empty AttributesImpl object. |
| [AttributesImpl](AttributesImpl.md))`(`atts:` ` [Attributes](../org.xml.sax/Attributes.md)!`)` Copy an existing Attributes object. |

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAttribute](AttributesImpl.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Add an attribute to the end of the list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](AttributesImpl.md))`()` Clear the attribute list for reuse. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](AttributesImpl.md))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up an attribute's index by qualified (prefixed) name. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](AttributesImpl.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up an attribute's index by Namespace name. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](AttributesImpl.md))`()` Return the number of attributes in the list. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocalName](AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return an attribute's local name. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getQName](AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return an attribute's qualified (prefixed) name. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return an attribute's type by index. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](AttributesImpl.md))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up an attribute's type by qualified (prefixed) name. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](AttributesImpl.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up an attribute's type by Namespace-qualified name. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getURI](AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return an attribute's Namespace URI. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return an attribute's value by index. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](AttributesImpl.md))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up an attribute's value by qualified (prefixed) name. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](AttributesImpl.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up an attribute's value by Namespace-qualified name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAttribute](AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Remove an attribute from the list. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAttribute](AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set an attribute in the list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAttributes](AttributesImpl.md))`(`atts:` ` [Attributes](../org.xml.sax/Attributes.md)!`)` Copy an entire Attributes object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocalName](AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the local name of a specific attribute. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setQName](AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the qualified name of a specific attribute. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setType](AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the type of a specific attribute. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setURI](AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the Namespace URI of a specific attribute. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setValue](AttributesImpl.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the value of a specific attribute. |

## Public constructors

### AttributesImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AttributesImpl()
```

Construct a new, empty AttributesImpl object. 

### AttributesImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AttributesImpl(atts: Attributes!)
```

Copy an existing Attributes object.

This constructor is especially useful inside a [startElement](../org.xml.sax/ContentHandler.md))event.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------|
| `atts` | [Attributes](../org.xml.sax/Attributes.md)!:The existing Attributes object. |

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

Add an attribute to the end of the list.

For the sake of speed, this method does no checking to see if the attribute is already in the list: that is the responsibility of the application.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty string if none is available or Namespace processing is not being performed. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The local name, or the empty string if Namespace processing is not being performed. |
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified (prefixed) name, or the empty string if qualified names are not available. |
| --- | --- |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute type as a string. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute value. |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Clear the attribute list for reuse.

Note that little memory is freed by this call: the current array is kept so it can be reused. 

### getIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIndex(qName: String!): Int
```

Look up an attribute's index by qualified (prefixed) name.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified name. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The attribute's index, or -1 if none matches. |

**See Also**

- [org.xml.sax.Attributes#getIndex(java.lang.String)](../org.xml.sax/Attributes.md)) 

### getIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIndex(
    uri: String!, 
    localName: String!
): Int
```

Look up an attribute's index by Namespace name.

In many cases, it will be more efficient to look up the name once and use the index query methods rather than using the name query methods repeatedly.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute's Namespace URI, or the empty string if none is available. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute's local name. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The attribute's index, or -1 if none matches. |

**See Also**

- [org.xml.sax.Attributes#getIndex(java.lang.String,java.lang.String)](../org.xml.sax/Attributes.md)) 

### getLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLength(): Int
```

Return the number of attributes in the list.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of attributes in the list. |

**See Also**

- [org.xml.sax.Attributes#getLength](../org.xml.sax/Attributes.md)) 

### getLocalName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalName(index: Int): String!
```

Return an attribute's local name.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute's index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute's local name, the empty string if none is available, or null if the index if out of range. |

**See Also**

- [org.xml.sax.Attributes#getLocalName](../org.xml.sax/Attributes.md)) 

### getQName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQName(index: Int): String!
```

Return an attribute's qualified (prefixed) name.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute's index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute's qualified name, the empty string if none is available, or null if the index is out of bounds. |

**See Also**

- [org.xml.sax.Attributes#getQName](../org.xml.sax/Attributes.md)) 

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(index: Int): String!
```

Return an attribute's type by index.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute's index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute's type, "CDATA" if the type is unknown, or null if the index is out of bounds. |

**See Also**

- [org.xml.sax.Attributes#getType(int)](../org.xml.sax/Attributes.md)) 

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(qName: String!): String!
```

Look up an attribute's type by qualified (prefixed) name.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified name. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute's type, or null if there is no matching attribute. |

**See Also**

- [org.xml.sax.Attributes#getType(java.lang.String)](../org.xml.sax/Attributes.md)) 

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(
    uri: String!, 
    localName: String!
): String!
```

Look up an attribute's type by Namespace-qualified name.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty string for a name with no explicit Namespace URI. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The local name. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute's type, or null if there is no matching attribute. |

**See Also**

- [org.xml.sax.Attributes#getType(java.lang.String,java.lang.String)](../org.xml.sax/Attributes.md)) 

### getURI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getURI(index: Int): String!
```

Return an attribute's Namespace URI.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute's index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The Namespace URI, the empty string if none is available, or null if the index is out of range. |

**See Also**

- [org.xml.sax.Attributes#getURI](../org.xml.sax/Attributes.md)) 

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(index: Int): String!
```

Return an attribute's value by index.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute's index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute's value or null if the index is out of bounds. |

**See Also**

- [org.xml.sax.Attributes#getValue(int)](../org.xml.sax/Attributes.md)) 

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(qName: String!): String!
```

Look up an attribute's value by qualified (prefixed) name.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified name. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute's value, or null if there is no matching attribute. |

**See Also**

- [org.xml.sax.Attributes#getValue(java.lang.String)](../org.xml.sax/Attributes.md)) 

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(
    uri: String!, 
    localName: String!
): String!
```

Look up an attribute's value by Namespace-qualified name.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty string for a name with no explicit Namespace URI. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The local name. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute's value, or null if there is no matching attribute. |

**See Also**

- [org.xml.sax.Attributes#getValue(java.lang.String,java.lang.String)](../org.xml.sax/Attributes.md)) 

### removeAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAttribute(index: Int): Unit
```

Remove an attribute from the list.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute (zero-based). |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | When the supplied index does not point to an attribute in the list. |

### setAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAttribute(
    index: Int, 
    uri: String!, 
    localName: String!, 
    qName: String!, 
    type: String!, 
    value: String!
): Unit
```

Set an attribute in the list.

For the sake of speed, this method does no checking for name conflicts or well-formedness: such checks are the responsibility of the application.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute (zero-based). |
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty string if none is available or Namespace processing is not being performed. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The local name, or the empty string if Namespace processing is not being performed. |
| --- | --- |
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified name, or the empty string if qualified names are not available. |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute type as a string. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute value. |
| --- | --- |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | When the supplied index does not point to an attribute in the list. |

### setAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAttributes(atts: Attributes!): Unit
```

Copy an entire Attributes object.

It may be more efficient to reuse an existing object rather than constantly allocating new ones.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------|
| `atts` | [Attributes](../org.xml.sax/Attributes.md)!:The attributes to copy. |

### setLocalName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLocalName(
    index: Int, 
    localName: String!
): Unit
```

Set the local name of a specific attribute.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute (zero-based). |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute's local name, or the empty string for none. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | When the supplied index does not point to an attribute in the list. |

### setQName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setQName(
    index: Int, 
    qName: String!
): Unit
```

Set the qualified name of a specific attribute.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute (zero-based). |
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute's qualified name, or the empty string for none. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | When the supplied index does not point to an attribute in the list. |

### setType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setType(
    index: Int, 
    type: String!
): Unit
```

Set the type of a specific attribute.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute (zero-based). |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute's type. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | When the supplied index does not point to an attribute in the list. |

### setURI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setURI(
    index: Int, 
    uri: String!
): Unit
```

Set the Namespace URI of a specific attribute.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute (zero-based). |
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute's Namespace URI, or the empty string for none. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | When the supplied index does not point to an attribute in the list. |

### setValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setValue(
    index: Int, 
    value: String!
): Unit
```

Set the value of a specific attribute.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute (zero-based). |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute's value. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | When the supplied index does not point to an attribute in the list. |
