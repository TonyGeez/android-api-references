# XmlSerializer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XmlSerializer

```
interface XmlSerializer
```

| [org.xmlpull.v1.XmlSerializer](XmlSerializer.md) |

Define an interface to serialization of XML Infoset. This interface abstracts away if serialized XML is XML 1.0 compatible text or other formats of XML 1.0 serializations (such as binary XML for example with WBXML).

**PLEASE NOTE:**This interface will be part of XmlPull 1.2 API. It is included as basis for discussion. It may change in any way.

Exceptions that may be thrown are: IOException or runtime exception (more runtime exceptions can be thrown but are not declared and as such have no semantics defined for this interface):

- *IllegalArgumentException*- for almost all methods to signal that argument is illegal
- *IllegalStateException*- to signal that call has good arguments but is not expected here (violation of contract) and for features/properties when requesting setting unimplemented feature/property (UnsupportedOperationException would be better but it is not in MIDP)

**NOTE:**writing CDSECT, ENTITY_REF, IGNORABLE_WHITESPACE, PROCESSING_INSTRUCTION, COMMENT, and DOCDECL in some implementations may not be supported (for example when serializing to WBXML). In such case IllegalStateException will be thrown and it is recommended to use an optional feature to signal that implementation is not supporting this kind of output.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [XmlSerializer](XmlSerializer.md)! | [attribute](XmlSerializer.md))`(`namespace:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Write an attribute. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cdsect](XmlSerializer.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [comment](XmlSerializer.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [docdecl](XmlSerializer.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endDocument](XmlSerializer.md))`()` Finish writing. |
| abstract [XmlSerializer](XmlSerializer.md)! | [endTag](XmlSerializer.md))`(`namespace:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Write end tag. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [entityRef](XmlSerializer.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](XmlSerializer.md))`()` Write all pending output to the stream. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDepth](XmlSerializer.md))`()` Returns the current depth of the element. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](XmlSerializer.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return the current value of the feature with given name. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](XmlSerializer.md))`()` Returns the name of the current element as set by startTag(). |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNamespace](XmlSerializer.md))`()` Returns the namespace URI of the current element as set by startTag(). |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPrefix](XmlSerializer.md))`(`namespace:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `generatePrefix:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Return namespace that corresponds to given prefix If there is no prefix bound to this namespace return null but if generatePrefix is false then return generated prefix. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getProperty](XmlSerializer.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ignorableWhitespace](XmlSerializer.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [processingInstruction](XmlSerializer.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](XmlSerializer.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `state:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set feature identified by name (recommended to be URI for uniqueness). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutput](XmlSerializer.md))`(`os:` ` [OutputStream](../java.io/OutputStream.md)!`, `encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set to use binary output stream with given encoding. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutput](XmlSerializer.md))`(`writer:` ` [Writer](../java.io/Writer.md)!`)` Set the output to the given writer. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPrefix](XmlSerializer.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `namespace:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Binds the given prefix to the given namespace. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](XmlSerializer.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Set the value of a property. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startDocument](XmlSerializer.md))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `standalone:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!`)` Write \<?xml declaration with encoding (if encoding not null) and standalone flag (if standalone not null) This method can only be called just after setOutput. |
| abstract [XmlSerializer](XmlSerializer.md)! | [startTag](XmlSerializer.md))`(`namespace:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Writes a start tag with the given namespace and name. |
| abstract [XmlSerializer](XmlSerializer.md)! | [text](XmlSerializer.md))`(`buf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes text, where special XML chars are escaped automatically |
| --- | --- |
| abstract [XmlSerializer](XmlSerializer.md)! | [text](XmlSerializer.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Writes text, where special XML chars are escaped automatically |

## Public methods

### attribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun attribute(
    namespace: String!, 
    name: String!, 
    value: String!
): XmlSerializer!
```

Write an attribute. Calls to attribute() MUST follow a call to startTag() immediately. If there is no prefix defined for the given namespace, a prefix will be defined automatically. If namespace is null or empty string no namespace prefix is printed but just name. 

### cdsect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cdsect(text: String!): Unit
```  

### comment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun comment(text: String!): Unit
```  

### docdecl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun docdecl(text: String!): Unit
```  

### endDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun endDocument(): Unit
```

Finish writing. All unclosed start tags will be closed and output will be flushed. After calling this method no more output can be serialized until next call to setOutput() 

### endTag

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun endTag(
    namespace: String!, 
    name: String!
): XmlSerializer!
```

Write end tag. Repetition of namespace and name is just for avoiding errors.

**Background:**in kXML endTag had no arguments, and non matching tags were very difficult to find... If namespace is null no namespace prefix is printed but just name. If namespace is empty string then serializer will make sure that default empty namespace is declared (in XML 1.0 xmlns=''). 

### entityRef

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun entityRef(text: String!): Unit
```  

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun flush(): Unit
```

Write all pending output to the stream. If method startTag() or attribute() was called then start tag is closed (final \>) before flush() is called on underlying output stream.

**NOTE:**if there is need to close start tag (so no more attribute() calls are allowed) but without flushing output call method text() with empty string (text("")). 

### getDepth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDepth(): Int
```

Returns the current depth of the element. Outside the root element, the depth is 0. The depth is incremented by 1 when startTag() is called. The depth is decremented after the call to endTag() event was observed. 

```kotlin
<!-- outside -->     0
  <root>               1
    sometext                 1
      <foobar>         2
      </foobar>        2
  </root>              1
  <!-- outside -->     0
  
```

<br />

### getFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFeature(name: String!): Boolean
```

Return the current value of the feature with given name.

**NOTE:** unknown properties are**always**returned as null

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of feature to be retrieved. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The value of named feature. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if feature string is null |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getName(): String!
```

Returns the name of the current element as set by startTag(). It can only be null before first call to startTag() or when last endTag() is called to close first startTag().

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | namespace set by startTag() that is currently in scope |

### getNamespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNamespace(): String!
```

Returns the namespace URI of the current element as set by startTag().

**NOTE:**that means in particular that:

- if there was startTag("", ...) then getNamespace() returns ""
- if there was startTag(null, ...) then getNamespace() returns null

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | namespace set by startTag() that is currently in scope |

### getPrefix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrefix(
    namespace: String!, 
    generatePrefix: Boolean
): String!
```

Return namespace that corresponds to given prefix If there is no prefix bound to this namespace return null but if generatePrefix is false then return generated prefix.

**NOTE:**if the prefix is empty string "" and default namespace is bound to this prefix then empty string ("") is returned.

**NOTE:** prefixes "xml" and "xmlns" are already bound will have values as defined [Namespaces in XML specification](http://www.w3.org/TR/REC-xml-names/) 

### getProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getProperty(name: String!): Any!
```

Look up the value of a property. The property name is any fully-qualified URI. I

**NOTE:**unknown properties are always returned as null

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of property to be retrieved. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The value of named property. |

### ignorableWhitespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun ignorableWhitespace(text: String!): Unit
```  

### processingInstruction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun processingInstruction(text: String!): Unit
```  

### setFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFeature(
    name: String!, 
    state: Boolean
): Unit
```

Set feature identified by name (recommended to be URI for uniqueness). Some well known optional features are defined in<http://www.xmlpull.org/v1/doc/features.html>. If feature is not recognized or can not be set then IllegalStateException MUST be thrown.

| Exceptions ||
|-----------------------------------|---------------------------------------------------|
| `java.lang.IllegalStateException` | If the feature is not supported or can not be set |

### setOutput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setOutput(
    os: OutputStream!, 
    encoding: String!
): Unit
```

Set to use binary output stream with given encoding. 

### setOutput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setOutput(writer: Writer!): Unit
```

Set the output to the given writer.

**WARNING**no information about encoding is available! 

### setPrefix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setPrefix(
    prefix: String!, 
    namespace: String!
): Unit
```

Binds the given prefix to the given namespace. This call is valid for the next element including child elements. The prefix and namespace MUST be always declared even if prefix is not used in element (startTag() or attribute()) - for XML 1.0 it must result in declaring`xmlns:prefix='namespace'`(or`xmlns:prefix="namespace"`depending what character is used to quote attribute value).

**NOTE:**this method MUST be called directly before startTag() and if anything but startTag() or setPrefix() is called next there will be exception.

**NOTE:** prefixes "xml" and "xmlns" are already bound and can not be redefined see: [Namespaces in XML Errata](http://www.w3.org/XML/xml-names-19990114-errata#NE05).

**NOTE:**to set default namespace use as prefix empty string.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:must be not null (or IllegalArgumentException is thrown) |
| `namespace` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:must be not null |

### setProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setProperty(
    name: String!, 
    value: Any!
): Unit
```

Set the value of a property. (the property name is recommended to be URI for uniqueness). Some well known optional properties are defined in<http://www.xmlpull.org/v1/doc/properties.html>. If property is not recognized or can not be set then IllegalStateException MUST be thrown.

| Exceptions ||
|-----------------------------------|----------------------------------------------------|
| `java.lang.IllegalStateException` | if the property is not supported or can not be set |

### startDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startDocument(
    encoding: String!, 
    standalone: Boolean!
): Unit
```

Write \<?xml declaration with encoding (if encoding not null) and standalone flag (if standalone not null) This method can only be called just after setOutput. 

### startTag

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startTag(
    namespace: String!, 
    name: String!
): XmlSerializer!
```

Writes a start tag with the given namespace and name. If there is no prefix defined for the given namespace, a prefix will be defined automatically. The explicit prefixes for namespaces can be established by calling setPrefix() immediately before this method. If namespace is null no namespace prefix is printed but just name. If namespace is empty string then serializer will make sure that default empty namespace is declared (in XML 1.0 xmlns='') or throw IllegalStateException if default namespace is already bound to non-empty string. 

### text

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun text(
    buf: CharArray!, 
    start: Int, 
    len: Int
): XmlSerializer!
```

Writes text, where special XML chars are escaped automatically 

### text

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun text(text: String!): XmlSerializer!
```

Writes text, where special XML chars are escaped automatically
