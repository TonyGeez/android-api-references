# Driver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Driver

```
open class Driver : Attributes, Locator, XMLReader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xmlpull.v1.sax2.Driver](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#) |

SAX2 Driver that pulls events from XmlPullParser and converts them into SAX2 callbacks.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APACHE_DYNAMIC_VALIDATION_FEATURE](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#APACHE_DYNAMIC_VALIDATION_FEATURE:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APACHE_SCHEMA_VALIDATION_FEATURE](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#APACHE_SCHEMA_VALIDATION_FEATURE:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DECLARATION_HANDLER_PROPERTY](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#DECLARATION_HANDLER_PROPERTY:kotlin.String) <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LEXICAL_HANDLER_PROPERTY](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#LEXICAL_HANDLER_PROPERTY:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAMESPACES_FEATURE](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#NAMESPACES_FEATURE:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAMESPACE_PREFIXES_FEATURE](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#NAMESPACE_PREFIXES_FEATURE:kotlin.String) <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [VALIDATION_FEATURE](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#VALIDATION_FEATURE:kotlin.String) <br /> |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Driver](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#Driver())`()` <br /> |
| [Driver](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#Driver(org.xmlpull.v1.XmlPullParser))`(`pp:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)!`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnNumber](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getColumnNumber())`()` <br /> |
| open [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)! | [getContentHandler](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getContentHandler())`()` <br /> |
| open [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#)! | [getDTDHandler](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getDTDHandler())`()` <br /> |
| --- | --- |
| open [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)! | [getEntityResolver](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getEntityResolver())`()` <br /> |
| open [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)! | [getErrorHandler](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getErrorHandler())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getFeature(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getIndex(kotlin.String))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getIndex(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getLength())`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineNumber](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getLineNumber())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocalName](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getLocalName(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getProperty](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getProperty(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPublicId](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getPublicId())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getQName](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getQName(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getSystemId())`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getType(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getType(kotlin.String))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getType(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getURI](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getURI(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getValue(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getValue(kotlin.String))`(`qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#getValue(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#parse(kotlin.String))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#parse(org.xml.sax.InputSource))`(`source:` ` [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parseSubTree](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#parseSubTree(org.xmlpull.v1.XmlPullParser))`(`pp:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentHandler](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#setContentHandler(org.xml.sax.ContentHandler))`(`handler:` ` [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDTDHandler](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#setDTDHandler(org.xml.sax.DTDHandler))`(`handler:` ` [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntityResolver](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#setEntityResolver(org.xml.sax.EntityResolver))`(`resolver:` ` [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#setErrorHandler(org.xml.sax.ErrorHandler))`(`handler:` ` [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#setFeature(kotlin.String,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#setProperty(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startElement](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#startElement(kotlin.String,%20kotlin.String,%20kotlin.String))`(`namespace:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Calls [startElement](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startElement(kotlin.String,%20kotlin.String,%20kotlin.String,%20org.xml.sax.Attributes))on the`ContentHandler`with`this`driver object as the [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#) implementation. |

| Properties ||
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)! | [contentHandler](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#contentHandler:org.xml.sax.ContentHandler) <br /> |
| [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)! | [errorHandler](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#errorHandler:org.xml.sax.ErrorHandler) <br /> |
| [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)! | [pp](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#pp:org.xmlpull.v1.XmlPullParser) <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [systemId](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver#systemId:kotlin.String) <br /> |

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
| [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)! | The current content handler, or null if none has been registered. |

### getDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDTDHandler(): DTDHandler!
```

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#)! | The current DTD handler, or null if none has been registered. |

### getEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEntityResolver(): EntityResolver!
```

| Return ||
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)! | The current entity resolver, or null if none has been registered. |

### getErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorHandler(): ErrorHandler!
```

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)! | The current error handler, or null if none has been registered. |

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
| `handler` | [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)!:The content handler. |

### setDTDHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDTDHandler(handler: DTDHandler!): Unit
```

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------|
| `handler` | [DTDHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DTDHandler.html#)!:The DTD handler. |

### setEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEntityResolver(resolver: EntityResolver!): Unit
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `resolver` | [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)!:The entity resolver. |

### setErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setErrorHandler(handler: ErrorHandler!): Unit
```

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------|
| `handler` | [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)!:The error handler. |

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

Calls [startElement](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startElement(kotlin.String,%20kotlin.String,%20kotlin.String,%20org.xml.sax.Attributes))on the`ContentHandler`with`this`driver object as the [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#) implementation. In default implementation [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#) object is valid only during this method call and may not be stored. Sub-classes can overwrite this method to cache attributes.

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
