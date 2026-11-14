# DocumentBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DocumentBuilder

```
abstract class DocumentBuilder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.xml.parsers.DocumentBuilder](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#) |

Defines the API to obtain DOM Document instances from an XML document. Using this class, an application programmer can obtain a [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) from XML.

An instance of this class can be obtained from the [DocumentBuilderFactory.newDocumentBuilder()](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#newDocumentBuilder())method. Once an instance of this class is obtained, XML can be parsed from a variety of input sources. These input sources are InputStreams, Files, URLs, and SAX InputSources.

Note that this class reuses several classes from the SAX API. This does not require that the implementor of the underlying DOM implementation use a SAX parser to parse XML document into a`Document`. It merely requires that the implementation communicate with the application using these existing APIs.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DocumentBuilder](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#DocumentBuilder())`()` Protected constructor |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DOMImplementation](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-implementation/index.html)! | [getDOMImplementation](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#getDOMImplementation())`()` Obtain an instance of a [DOMImplementation](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-implementation/index.html) object. |
| open [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#)! | [getSchema](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#getSchema())`()` Get a reference to the the [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#) being used by the XML processor. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNamespaceAware](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#isNamespaceAware())`()` Indicates whether or not this parser is configured to understand namespaces. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidating](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#isValidating())`()` Indicates whether or not this parser is configured to validate XML documents. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isXIncludeAware](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#isXIncludeAware())`()` Get the XInclude processing mode for this parser. |
| abstract [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [newDocument](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#newDocument())`()` Obtain a new instance of a DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object to build a DOM tree with. |
| open [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#parse(java.io.File))`(`f:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Parse the content of the given file as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. |
| open [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#parse(java.io.InputStream))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Parse the content of the given`InputStream`as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. |
| open [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#parse(java.io.InputStream,%20kotlin.String))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse the content of the given`InputStream`as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. |
| open [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#parse(kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse the content of the given URI as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. |
| abstract [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#parse(org.xml.sax.InputSource))`(`is:` ` [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!`)` Parse the content of the given input source as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#reset())`()` Reset this`DocumentBuilder`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntityResolver](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#setEntityResolver(org.xml.sax.EntityResolver))`(`er:` ` [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)!`)` Specify the [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#) to be used to resolve entities present in the XML document to be parsed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#setErrorHandler(org.xml.sax.ErrorHandler))`(`eh:` ` [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)!`)` Specify the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) to be used by the parser. |

## Protected constructors

### DocumentBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected DocumentBuilder()
```

Protected constructor

## Public methods

### getDOMImplementation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDOMImplementation(): DOMImplementation!
```

Obtain an instance of a [DOMImplementation](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-implementation/index.html) object.

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [DOMImplementation](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-implementation/index.html)! | A new instance of a`DOMImplementation`. |

### getSchema

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSchema(): Schema!
```

Get a reference to the the [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#) being used by the XML processor.

If no schema is being used,`null`is returned.

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#)! | [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#) being used or`null`if none in use |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | For backward compatibility, when implementations for earlier versions of JAXP is used, this exception will be thrown. |

### isNamespaceAware

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isNamespaceAware(): Boolean
```

Indicates whether or not this parser is configured to understand namespaces.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this parser is configured to understand namespaces; false otherwise. |

### isValidating

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isValidating(): Boolean
```

Indicates whether or not this parser is configured to validate XML documents.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this parser is configured to validate XML documents; false otherwise. |

### isXIncludeAware

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isXIncludeAware(): Boolean
```

Get the XInclude processing mode for this parser.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the return value of the [DocumentBuilderFactory.isXIncludeAware()](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#isXIncludeAware())when this parser was created from factory. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | For backward compatibility, when implementations for earlier versions of JAXP is used, this exception will be thrown. |

**See Also**

- [javax.xml.parsers.DocumentBuilderFactory#setXIncludeAware(boolean)](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setXIncludeAware(kotlin.Boolean)) 

### newDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newDocument(): Document!
```

Obtain a new instance of a DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object to build a DOM tree with.

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------------------|
| [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | A new instance of a DOM Document object. |

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(f: File!): Document!
```

Parse the content of the given file as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. An`IllegalArgumentException`is thrown if the`File`is`null`null.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `f` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:The file containing the XML to parse. |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | A new DOM Document object. |

| Exceptions ||
|----------------------------|----------------------------|
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any parse errors occur. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(is: InputStream!): Document!
```

Parse the content of the given`InputStream`as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. An`IllegalArgumentException`is thrown if the`InputStream`is null.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:InputStream containing the content to be parsed. |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | `Document`result of parsing the`InputStream` |

| Exceptions ||
|----------------------------|----------------------------|
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any parse errors occur. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    is: InputStream!, 
    systemId: String!
): Document!
```

Parse the content of the given`InputStream`as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. An`IllegalArgumentException`is thrown if the`InputStream`is null.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:InputStream containing the content to be parsed. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Provide a base for resolving relative URIs. |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | A new DOM Document object. |

| Exceptions ||
|----------------------------|----------------------------|
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any parse errors occur. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(uri: String!): Document!
```

Parse the content of the given URI as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. An`IllegalArgumentException`is thrown if the URI is`null`null.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The location of the content to be parsed. |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | A new DOM Document object. |

| Exceptions ||
|----------------------------|----------------------------|
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any parse errors occur. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parse(is: InputSource!): Document!
```

Parse the content of the given input source as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. An`IllegalArgumentException`is thrown if the`InputSource`is`null`null.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!:InputSource containing the content to be parsed. |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | A new DOM Document object. |

| Exceptions ||
|----------------------------|----------------------------|
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any parse errors occur. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Reset this`DocumentBuilder`.
This method removes both the`EntityResolver`and`ErrorHandler`instances associated with this`DocumentBuilder`and sets all internal properties to false including those set by the`DocumentBuilderFactory`when this`DocumentBuilder`was created. 
**See Also**

- [#setEntityResolver(EntityResolver)](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#setEntityResolver(org.xml.sax.EntityResolver))
- [#setErrorHandler(ErrorHandler)](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder#setErrorHandler(org.xml.sax.ErrorHandler))
- [javax.xml.parsers.DocumentBuilderFactory](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory) 

### setEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEntityResolver(er: EntityResolver!): Unit
```

Specify the [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#) to be used to resolve entities present in the XML document to be parsed. Setting this to`null`will result in the underlying implementation using it's own default implementation and behavior.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `er` | [EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#)!:The`EntityResolver`to be used to resolve entities present in the XML document to be parsed. |

### setErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setErrorHandler(eh: ErrorHandler!): Unit
```

Specify the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) to be used by the parser. Setting this to`null`will result in the underlying implementation using it's own default implementation and behavior.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `eh` | [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)!:The`ErrorHandler`to be used by the parser. |
