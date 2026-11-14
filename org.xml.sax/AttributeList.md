# AttributeList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AttributeList

```
interface AttributeList
```

| [org.xml.sax.AttributeList](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList#) |

| Known Direct Subclasses [AttributeListImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl) |-----------------------------------------------------------------------------------------------------------|-------------------------------------------| | [AttributeListImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl) | Default implementation for AttributeList. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 9.**
|
| This interface has been replaced by the SAX2 [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes) interface, which includes Namespace support.

Interface for an element's attribute specifications.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This is the original SAX1 interface for reporting an element's attributes. Unlike the new [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes) interface, it does not support Namespace-related information.

When an attribute list is supplied as part of a [startElement](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler#startElement(kotlin.String,%20org.xml.sax.AttributeList))event, the list will return valid results only during the scope of the event; once the event handler returns control to the parser, the attribute list is invalid. To save a persistent copy of the attribute list, use the SAX1 [AttributeListImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/AttributeListImpl) helper class.

An attribute list includes only attributes that have been specified or defaulted: #IMPLIED attributes will not be included.

There are two ways for the SAX application to obtain information from the AttributeList. First, it can iterate through the entire list: 

```kotlin
public void startElement (String name, AttributeList atts) {
    for (int i = 0; i < atts.getLength(); i++) {
      String name = atts.getName(i);
      String type = atts.getType(i);
      String value = atts.getValue(i);
      [...]
    }
  }
  
```

(Note that the result of getLength() will be zero if there are no attributes.)

As an alternative, the application can request the value or type of specific attributes: 

```kotlin
public void startElement (String name, AttributeList atts) {
    String identifier = atts.getValue("id");
    String label = atts.getValue("label");
    [...]
  }
  
```

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList#getLength())`()` Return the number of attributes in this list. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList#getName(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the name of an attribute in this list (by position). |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList#getType(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the type of an attribute in the list (by position). |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList#getType(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return the type of an attribute in the list (by name). |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList#getValue(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the value of an attribute in the list (by position). |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList#getValue(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return the value of an attribute in the list (by name). |
| --- | --- |

## Public methods

### getLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLength(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the number of attributes in this list.

The SAX parser may provide attributes in any arbitrary order, regardless of the order in which they were declared or specified. The number of attributes may be zero.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of attributes in the list. |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getName(i: Int): String!
```

**Deprecated:** *Deprecated in Java.*

Return the name of an attribute in this list (by position).

The names must be unique: the SAX parser shall not include the same attribute twice. Attributes without values (those declared #IMPLIED without a value specified in the start tag) will be omitted from the list.

If the attribute name has a namespace prefix, the prefix will still be attached.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute in the list (starting at 0). |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The name of the indexed attribute, or null if the index is out of range. |

**See Also**

- [#getLength](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList#getLength()) 

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getType(i: Int): String!
```

**Deprecated:** *Deprecated in Java.*

Return the type of an attribute in the list (by position).

The attribute type is one of the strings "CDATA", "ID", "IDREF", "IDREFS", "NMTOKEN", "NMTOKENS", "ENTITY", "ENTITIES", or "NOTATION" (always in upper case).

If the parser has not read a declaration for the attribute, or if the parser does not report attribute types, then it must return the value "CDATA" as stated in the XML 1.0 Recommentation (clause 3.3.3, "Attribute-Value Normalization").

For an enumerated attribute that is not a notation, the parser will report the type as "NMTOKEN".

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute in the list (starting at 0). |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute type as a string, or null if the index is out of range. |

**See Also**

- [#getLength](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList#getLength())
- [#getType(java.lang.String)](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList#getType(kotlin.String)) 

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getType(name: String!): String!
```

**Deprecated:** *Deprecated in Java.*

Return the type of an attribute in the list (by name).

The return value is the same as the return value for getType(int).

If the attribute name has a namespace prefix in the document, the application must include the prefix here.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the attribute. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute type as a string, or null if no such attribute exists. |

**See Also**

- [#getType(int)](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList#getType(kotlin.Int)) 

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getValue(i: Int): String!
```

**Deprecated:** *Deprecated in Java.*

Return the value of an attribute in the list (by position).

If the attribute value is a list of tokens (IDREFS, ENTITIES, or NMTOKENS), the tokens will be concatenated into a single string separated by whitespace.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute in the list (starting at 0). |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute value as a string, or null if the index is out of range. |

**See Also**

- [#getLength](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList#getLength())
- [#getValue(java.lang.String)](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList#getValue(kotlin.String)) 

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getValue(name: String!): String!
```

**Deprecated:** *Deprecated in Java.*

Return the value of an attribute in the list (by name).

The return value is the same as the return value for getValue(int).

If the attribute name has a namespace prefix in the document, the application must include the prefix here.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the attribute to return |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute value as a string, or null if no such attribute exists. |

**See Also**

- [#getValue(int)](https://developer.android.com/reference/kotlin/org/xml/sax/AttributeList#getValue(kotlin.Int))
