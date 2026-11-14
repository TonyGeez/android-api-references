# AttributeListImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AttributeListImpl

```
open class AttributeListImpl : AttributeList
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xml.sax.helpers.AttributeListImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#) |

| **This class was deprecated in API level 9.**
|
| This class implements a deprecated interface, [AttributeList](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList.html#); that interface has been replaced by [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#), which is implemented in the [AttributesImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributesImpl) helper class.

Default implementation for AttributeList.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

AttributeList implements the deprecated SAX1 interface, and has been replaced by the new SAX2 [AttributesImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributesImpl) interface.

This class provides a convenience implementation of the SAX [AttributeList](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList.html#) interface. This implementation is useful both for SAX parser writers, who can use it to provide attributes to the application, and for SAX application writers, who can use it to create a persistent copy of an element's attribute specifications: 

```kotlin
private AttributeList myatts;
 
  public void startElement (String name, AttributeList atts)
  {
               // create a persistent copy of the attribute list
               // for use outside this method
    myatts = new AttributeListImpl(atts);
    [...]
  }
  
```

Please note that SAX parsers are not required to use this class to provide an implementation of AttributeList; it is supplied only as an optional convenience. In particular, parser writers are encouraged to invent more efficient implementations.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AttributeListImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#AttributeListImpl())`()` Create an empty attribute list. |
| [AttributeListImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#AttributeListImpl(org.xml.sax.AttributeList))`(`atts:` ` [AttributeList](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList.html#)!`)` Construct a persistent copy of an existing attribute list. |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAttribute](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#addAttribute(kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Add an attribute to an attribute list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#clear())`()` Clear the attribute list. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#getLength())`()` Return the number of attributes in the list. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#getName(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the name of an attribute (by position). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#getType(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the type of an attribute (by position). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#getType(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the type of an attribute (by name). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#getValue(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the value of an attribute (by position). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#getValue(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the value of an attribute (by name). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAttribute](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#removeAttribute(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Remove an attribute from the list. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAttributeList](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#setAttributeList(org.xml.sax.AttributeList))`(`atts:` ` [AttributeList](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList.html#)!`)` Set the attribute list, discarding previous contents. |

## Public constructors

### AttributeListImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AttributeListImpl()
```

Create an empty attribute list.

This constructor is most useful for parser writers, who will use it to create a single, reusable attribute list that can be reset with the clear method between elements. 
**See Also**

- [#addAttribute](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#addAttribute(kotlin.String,%20kotlin.String,%20kotlin.String))
- [#clear](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#clear()) 

### AttributeListImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AttributeListImpl(atts: AttributeList!)
```

Construct a persistent copy of an existing attribute list.

This constructor is most useful for application writers, who will use it to create a persistent copy of an existing attribute list.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `atts` | [AttributeList](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList.html#)!:The attribute list to copy |

**See Also**

- [org.xml.sax.DocumentHandler#startElement](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#startElement(kotlin.String,%20org.xml.sax.AttributeList))

## Public methods

### addAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAttribute(
    name: String!, 
    type: String!, 
    value: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Add an attribute to an attribute list.

This method is provided for SAX parser writers, to allow them to build up an attribute list incrementally before delivering it to the application.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute name. |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute type ("NMTOKEN" for an enumeration). |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute value (must not be null). |
| --- | --- |

**See Also**

- [#removeAttribute](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#removeAttribute(kotlin.String))
- [org.xml.sax.DocumentHandler#startElement](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#startElement(kotlin.String,%20org.xml.sax.AttributeList)) 

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

**Deprecated:** *Deprecated in Java.*

Clear the attribute list.

SAX parser writers can use this method to reset the attribute list between DocumentHandler.startElement events. Normally, it will make sense to reuse the same AttributeListImpl object rather than allocating a new one each time. 
**See Also**

- [org.xml.sax.DocumentHandler#startElement](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#startElement(kotlin.String,%20org.xml.sax.AttributeList)) 

### getLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLength(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the number of attributes in the list.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of attributes in the list. |

**See Also**

- [org.xml.sax.AttributeList#getLength](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList.html#getLength()) 

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(i: Int): String!
```

**Deprecated:** *Deprecated in Java.*

Get the name of an attribute (by position).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the attribute in the list. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute name as a string, or null if there is no attribute at that position. |

**See Also**

- [org.xml.sax.AttributeList#getName(int)](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList.html#getName(kotlin.Int)) 

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(i: Int): String!
```

**Deprecated:** *Deprecated in Java.*

Get the type of an attribute (by position).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the attribute in the list. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute type as a string ("NMTOKEN" for an enumeration, and "CDATA" if no declaration was read), or null if there is no attribute at that position. |

**See Also**

- [org.xml.sax.AttributeList#getType(int)](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList.html#getType(kotlin.Int)) 

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(name: String!): String!
```

**Deprecated:** *Deprecated in Java.*

Get the type of an attribute (by name).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute name. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute type as a string ("NMTOKEN" for an enumeration, and "CDATA" if no declaration was read). |

**See Also**

- [org.xml.sax.AttributeList#getType(java.lang.String)](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList.html#getType(kotlin.String)) 

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(i: Int): String!
```

**Deprecated:** *Deprecated in Java.*

Get the value of an attribute (by position).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the attribute in the list. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute value as a string, or null if there is no attribute at that position. |

**See Also**

- [org.xml.sax.AttributeList#getValue(int)](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList.html#getValue(kotlin.Int)) 

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(name: String!): String!
```

**Deprecated:** *Deprecated in Java.*

Get the value of an attribute (by name).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute name. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the named attribute's value or null, if the attribute does not exist. |

**See Also**

- [org.xml.sax.AttributeList#getValue(java.lang.String)](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList.html#getValue(kotlin.String)) 

### removeAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAttribute(name: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Remove an attribute from the list.

SAX application writers can use this method to filter an attribute out of an AttributeList. Note that invoking this method will change the length of the attribute list and some of the attribute's indices.

If the requested attribute is not in the list, this is a no-op.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The attribute name. |

**See Also**

- [#addAttribute](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl#addAttribute(kotlin.String,%20kotlin.String,%20kotlin.String)) 

### setAttributeList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAttributeList(atts: AttributeList!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the attribute list, discarding previous contents.

This method allows an application writer to reuse an attribute list easily.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------|
| `atts` | [AttributeList](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList.html#)!:The attribute list to copy. |
