# Driver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Driver

```
open class Driver : Attributes, Locator, XMLReader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xmlpull.v1.sax2.Driver](Driver.md) |

SAX2 Driver that pulls events from XmlPullParser and converts them into SAX2 callbacks.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APACHE_DYNAMIC_VALIDATION_FEATURE](Driver.md) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APACHE_SCHEMA_VALIDATION_FEATURE](Driver.md) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DECLARATION_HANDLER_PROPERTY](Driver.md) <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LEXICAL_HANDLER_PROPERTY](Driver.md) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAMESPACES_FEATURE](Driver.md) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAMESPACE_PREFIXES_FEATURE](Driver.md) <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [VALIDATION_FEATURE](Driver.md) <br /> |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Driver](Driver.md))`()` <br /> |
| [Driver](Driver.md))`(`pp:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)!`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnNumber](Driver.md))`()` <br /> |
| open [ContentHandler](../org.xml.sax/ContentHandler.md)! | [getContentHandler](Driver.md))`()` <br /> |
| open [DTDHandler](../org.xml.sax/DTDHandler.md)! | [getDTDHandler](Driver.md))`()` <br /> |
| --- | --- |
| open [EntityResolver](../org.xml.sax/EntityResolver.md)! | [getEntityResolver](Driver.md))`()` <br /> |
| open [ErrorHandler](../org.xml.sax/ErrorHandler.md)! | [getErrorHandler](Driver.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](Driver.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](Driver.md))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](Driver.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](Driver.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineNumber](Driver.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocalName](Driver.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getProperty](Driver.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPublicId](Driver.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getQName](Driver.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](Driver.md))`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](Driver.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](Driver.md))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](Driver.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getURI](Driver.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](Driver.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](Driver.md))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](Driver.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](Driver.md))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](Driver.md))`(`source:` ` [InputSource](../org.xml.sax/InputSource.md)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parseSubTree](Driver.md))`(`pp:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentHandler](Driver.md))`(`handler:` ` [ContentHandler](../org.xml.sax/ContentHandler.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDTDHandler](Driver.md))`(`handler:` ` [DTDHandler](../org.xml.sax/DTDHandler.md)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntityResolver](Driver.md))`(`resolver:` ` [EntityResolver](../org.xml.sax/EntityResolver.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](Driver.md))`(`handler:` ` [ErrorHandler](../org.xml.sax/ErrorHandler.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](Driver.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](Driver.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startElement](Driver.md))`(`namespace:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Calls [startElement](../org.xml.sax/ContentHandler.md))on the`ContentHandler`with`this`driver object as the [Attributes](../org.xml.sax/Attributes.md) implementation. |

| Properties ||
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentHandler](../org.xml.sax/ContentHandler.md)! | [contentHandler](Driver.md) <br /> |
| [ErrorHandler](../org.xml.sax/ErrorHandler.md)! | [errorHandler](Driver.md) <br /> |
| [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)! | [pp](Driver.md) <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [systemId](Driver.md) <br /> |

## Constants

### APACHE_DYNAMIC_VALIDATION_FEATURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected static val APACHE_DYNAMIC_VALIDATION_FEATURE: String
```  

 Value: "http://apache.org/xml/features/validation/dynamic"

### APACHE_SCHEMA_VALIDATION_FEATURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected static val APACHE_SCHEMA_VALIDATION_FEATURE: String
```  

 Value: "http://apache.org/xml/features/validation/schema"

### DECLARATION_HANDLER_PROPERTY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected static val DECLARATION_HANDLER_PROPERTY: String
```  

 Value: "http://xml.org/sax/properties/declaration-handler"

### LEXICAL_HANDLER_PROPERTY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected static val LEXICAL_HANDLER_PROPERTY: String
```  

 Value: "http://xml.org/sax/properties/lexical-handler"

### NAMESPACES_FEATURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected static val NAMESPACES_FEATURE: String
```  

 Value: "http://xml.org/sax/features/namespaces"

### NAMESPACE_PREFIXES_FEATURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected static val NAMESPACE_PREFIXES_FEATURE: String
```  

 Value: "http://xml.org/sax/features/namespace-prefixes"

### VALIDATION_FEATURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected static val VALIDATION_FEATURE: String
```  

 Value: "http://xml.org/sax/features/validation"

## Public constructors

### Driver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Driver()
```  

### Driver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Driver(pp: XmlPullParser!)
```

## Public methods

### getColumnNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColumnNumber(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The column number, or -1 if none is available. |

### getContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContentHandler(): ContentHandler!
```

| Return ||
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [ContentHandler](../org.xml.sax/ContentHandler.md)! | The current content handler, or null if none has been registered. |

### getDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDTDHandler(): DTDHandler!
```

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [DTDHandler](../org.xml.sax/DTDHandler.md)! | The current DTD handler, or null if none has been registered. |

### getEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEntityResolver(): EntityResolver!
```

| Return ||
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [EntityResolver](../org.xml.sax/EntityResolver.md)! | The current entity resolver, or null if none has been registered. |

### getErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorHandler(): ErrorHandler!
```

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [ErrorHandler](../org.xml.sax/ErrorHandler.md)! | The current error handler, or null if none has been registered. |

### getFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFeature(name: String!): Boolean
```

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The feature name, which is a fully-qualified URI. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The current value of the feature (true or false). |

### getIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIndex(qName: String!): Int
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified (prefixed) name. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index of the attribute, or -1 if it does not appear in the list. |

### getIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIndex(
    uri: String!, 
    localName: String!
): Int
```

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
open fun getLength(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of attributes in the list. |

### getLineNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineNumber(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The line number, or -1 if none is available. |

### getLocalName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalName(index: Int): String!
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The local name, or the empty string if Namespace processing is not being performed, or null if the index is out of range. |

### getProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProperty(name: String!): Any!
```

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property name, which is a fully-qualified URI. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The current value of the property. |

### getPublicId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPublicId(): String!
```

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string containing the public identifier, or null if none is available. |

### getQName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQName(index: Int): String!
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The XML qualified name, or the empty string if none is available, or null if the index is out of range. |

### getSystemId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSystemId(): String!
```

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string containing the system identifier, or null if none is available. |

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(index: Int): String!
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute's type as a string, or null if the index is out of range. |

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(qName: String!): String!
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------|
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The XML qualified name. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute type as a string, or null if the attribute is not in the list or if qualified names are not available. |

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(
    uri: String!, 
    localName: String!
): String!
```

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
open fun getURI(index: Int): String!
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The Namespace URI, or the empty string if none is available, or null if the index is out of range. |

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(index: Int): String!
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute index (zero-based). |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute's value as a string, or null if the index is out of range. |

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(qName: String!): String!
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------|
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The XML qualified name. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute value as a string, or null if the attribute is not in the list or if qualified names are not available. |

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(
    uri: String!, 
    localName: String!
): String!
```

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The Namespace URI, or the empty String if the name has no Namespace URI. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The local name of the attribute. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute value as a string, or null if the attribute is not in the list. |

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(systemId: String!): Unit
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier (URI). |

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(source: InputSource!): Unit
```

| Parameters ||
|---------|---------------------------------------------------------|
| `input` | The input source for the top-level of the XML document. |

### parseSubTree

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parseSubTree(pp: XmlPullParser!): Unit
```  

### setContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentHandler(handler: ContentHandler!): Unit
```

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| `handler` | [ContentHandler](../org.xml.sax/ContentHandler.md)!:The content handler. |

### setDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDTDHandler(handler: DTDHandler!): Unit
```

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------|
| `handler` | [DTDHandler](../org.xml.sax/DTDHandler.md)!:The DTD handler. |

### setEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEntityResolver(resolver: EntityResolver!): Unit
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `resolver` | [EntityResolver](../org.xml.sax/EntityResolver.md)!:The entity resolver. |

### setErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setErrorHandler(handler: ErrorHandler!): Unit
```

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------|
| `handler` | [ErrorHandler](../org.xml.sax/ErrorHandler.md)!:The error handler. |

### setFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFeature(
    name: String!, 
    value: Boolean
): Unit
```

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The feature name, which is a fully-qualified URI. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The requested value of the feature (true or false). |

### setProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProperty(
    name: String!, 
    value: Any!
): Unit
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property name, which is a fully-qualified URI. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The requested value for the property. |

## Protected methods

### startElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun startElement(
    namespace: String!, 
    localName: String!, 
    qName: String!
): Unit
```

Calls [startElement](../org.xml.sax/ContentHandler.md))on the`ContentHandler`with`this`driver object as the [Attributes](../org.xml.sax/Attributes.md) implementation. In default implementation [Attributes](../org.xml.sax/Attributes.md) object is valid only during this method call and may not be stored. Sub-classes can overwrite this method to cache attributes.

## Properties

### contentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var contentHandler: ContentHandler!
```  

### errorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var errorHandler: ErrorHandler!
```  

### pp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var pp: XmlPullParser!
```  

### systemId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var systemId: String!
```
