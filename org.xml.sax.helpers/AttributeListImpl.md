# AttributeListImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AttributeListImpl

```
open class AttributeListImpl : AttributeList
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xml.sax.helpers.AttributeListImpl](../org/xml/sax/helpers/AttributeListImpl.md) |

| **This class was deprecated in API level 9.**
|
| This class implements a deprecated interface, [AttributeList](../org/xml/sax/AttributeList.md); that interface has been replaced by [Attributes](../org/xml/sax/Attributes.md), which is implemented in the [AttributesImpl](../org/xml/sax/helpers/AttributesImpl.md) helper class.

Default implementation for AttributeList.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

AttributeList implements the deprecated SAX1 interface, and has been replaced by the new SAX2 [AttributesImpl](../org/xml/sax/helpers/AttributesImpl.md) interface.

This class provides a convenience implementation of the SAX [AttributeList](../org/xml/sax/AttributeList.md) interface. This implementation is useful both for SAX parser writers, who can use it to provide attributes to the application, and for SAX application writers, who can use it to create a persistent copy of an element's attribute specifications: 

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
| [AttributeListImpl](../org/xml/sax/helpers/AttributeListImpl.md))`()` Create an empty attribute list. |
| [AttributeListImpl](../org/xml/sax/helpers/AttributeListImpl.md))`(`atts:` ` [AttributeList](../org/xml/sax/AttributeList.md)!`)` Construct a persistent copy of an existing attribute list. |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAttribute](../org/xml/sax/helpers/AttributeListImpl.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Add an attribute to an attribute list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../org/xml/sax/helpers/AttributeListImpl.md))`()` Clear the attribute list. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](../org/xml/sax/helpers/AttributeListImpl.md))`()` Return the number of attributes in the list. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../org/xml/sax/helpers/AttributeListImpl.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the name of an attribute (by position). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](../org/xml/sax/helpers/AttributeListImpl.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the type of an attribute (by position). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](../org/xml/sax/helpers/AttributeListImpl.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the type of an attribute (by name). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](../org/xml/sax/helpers/AttributeListImpl.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the value of an attribute (by position). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](../org/xml/sax/helpers/AttributeListImpl.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the value of an attribute (by name). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAttribute](../org/xml/sax/helpers/AttributeListImpl.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Remove an attribute from the list. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAttributeList](../org/xml/sax/helpers/AttributeListImpl.md))`(`atts:` ` [AttributeList](../org/xml/sax/AttributeList.md)!`)` Set the attribute list, discarding previous contents. |

## Public constructors

### AttributeListImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AttributeListImpl()
```

Create an empty attribute list.

This constructor is most useful for parser writers, who will use it to create a single, reusable attribute list that can be reset with the clear method between elements. 
**See Also**

- [#addAttribute](../org/xml/sax/helpers/AttributeListImpl.md))
- [#clear](../org/xml/sax/helpers/AttributeListImpl.md)) 

### AttributeListImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AttributeListImpl(atts: AttributeList!)
```

Construct a persistent copy of an existing attribute list.

This constructor is most useful for application writers, who will use it to create a persistent copy of an existing attribute list.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `atts` | [AttributeList](../org/xml/sax/AttributeList.md)!:The attribute list to copy |

**See Also**

- [org.xml.sax.DocumentHandler#startElement](../org/xml/sax/DocumentHandler.md))

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

- [#removeAttribute](../org/xml/sax/helpers/AttributeListImpl.md))
- [org.xml.sax.DocumentHandler#startElement](../org/xml/sax/DocumentHandler.md)) 

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

**Deprecated:** *Deprecated in Java.*

Clear the attribute list.

SAX parser writers can use this method to reset the attribute list between DocumentHandler.startElement events. Normally, it will make sense to reuse the same AttributeListImpl object rather than allocating a new one each time. 
**See Also**

- [org.xml.sax.DocumentHandler#startElement](../org/xml/sax/DocumentHandler.md)) 

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

- [org.xml.sax.AttributeList#getLength](../org/xml/sax/AttributeList.md)) 

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

- [org.xml.sax.AttributeList#getName(int)](../org/xml/sax/AttributeList.md)) 

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

- [org.xml.sax.AttributeList#getType(int)](../org/xml/sax/AttributeList.md)) 

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

- [org.xml.sax.AttributeList#getType(java.lang.String)](../org/xml/sax/AttributeList.md)) 

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

- [org.xml.sax.AttributeList#getValue(int)](../org/xml/sax/AttributeList.md)) 

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

- [org.xml.sax.AttributeList#getValue(java.lang.String)](../org/xml/sax/AttributeList.md)) 

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

- [#addAttribute](../org/xml/sax/helpers/AttributeListImpl.md)) 

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
| `atts` | [AttributeList](../org/xml/sax/AttributeList.md)!:The attribute list to copy. |
