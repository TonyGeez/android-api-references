# DocumentBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DocumentBuilder

```
abstract class DocumentBuilder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.parsers.DocumentBuilder](DocumentBuilder.md) |

Defines the API to obtain DOM Document instances from an XML document. Using this class, an application programmer can obtain a [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) from XML.

An instance of this class can be obtained from the [DocumentBuilderFactory.newDocumentBuilder()](DocumentBuilderFactory.md))method. Once an instance of this class is obtained, XML can be parsed from a variety of input sources. These input sources are InputStreams, Files, URLs, and SAX InputSources.

Note that this class reuses several classes from the SAX API. This does not require that the implementor of the underlying DOM implementation use a SAX parser to parse XML document into a`Document`. It merely requires that the implementation communicate with the application using these existing APIs.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DocumentBuilder](DocumentBuilder.md))`()` Protected constructor |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DOMImplementation](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-implementation/index.html)! | [getDOMImplementation](DocumentBuilder.md))`()` Obtain an instance of a [DOMImplementation](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-implementation/index.html) object. |
| open [Schema](../javax.xml.validation/Schema.md)! | [getSchema](DocumentBuilder.md))`()` Get a reference to the the [Schema](../javax.xml.validation/Schema.md) being used by the XML processor. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNamespaceAware](DocumentBuilder.md))`()` Indicates whether or not this parser is configured to understand namespaces. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidating](DocumentBuilder.md))`()` Indicates whether or not this parser is configured to validate XML documents. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isXIncludeAware](DocumentBuilder.md))`()` Get the XInclude processing mode for this parser. |
| abstract [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [newDocument](DocumentBuilder.md))`()` Obtain a new instance of a DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object to build a DOM tree with. |
| --- | --- |
| open [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [parse](DocumentBuilder.md))`(`f:` ` [File](../java.io/File.md)!`)` Parse the content of the given file as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. |
| open [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [parse](DocumentBuilder.md))`(`is:` ` [InputStream](../java.io/InputStream.md)!`)` Parse the content of the given`InputStream`as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. |
| open [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [parse](DocumentBuilder.md))`(`is:` ` [InputStream](../java.io/InputStream.md)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse the content of the given`InputStream`as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. |
| --- | --- |
| open [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [parse](DocumentBuilder.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse the content of the given URI as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. |
| abstract [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [parse](DocumentBuilder.md))`(`is:` ` [InputSource](../org.xml.sax/InputSource.md)!`)` Parse the content of the given input source as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](DocumentBuilder.md))`()` Reset this`DocumentBuilder`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntityResolver](DocumentBuilder.md))`(`er:` ` [EntityResolver](../org.xml.sax/EntityResolver.md)!`)` Specify the [EntityResolver](../org.xml.sax/EntityResolver.md) to be used to resolve entities present in the XML document to be parsed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](DocumentBuilder.md))`(`eh:` ` [ErrorHandler](../org.xml.sax/ErrorHandler.md)!`)` Specify the [ErrorHandler](../org.xml.sax/ErrorHandler.md) to be used by the parser. |

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

Get a reference to the the [Schema](../javax.xml.validation/Schema.md) being used by the XML processor.

If no schema is being used,`null`is returned.

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Schema](../javax.xml.validation/Schema.md)! | [Schema](../javax.xml.validation/Schema.md) being used or`null`if none in use |

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
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the return value of the [DocumentBuilderFactory.isXIncludeAware()](DocumentBuilderFactory.md))when this parser was created from factory. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | For backward compatibility, when implementations for earlier versions of JAXP is used, this exception will be thrown. |

**See Also**

- [javax.xml.parsers.DocumentBuilderFactory#setXIncludeAware(boolean)](DocumentBuilderFactory.md)) 

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
| `f` | [File](../java.io/File.md)!:The file containing the XML to parse. |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | A new DOM Document object. |

| Exceptions ||
|----------------------------|----------------------------|
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any parse errors occur. |

**See Also**

- [org.xml.sax.DocumentHandler](../org.xml.sax/DocumentHandler.md) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(is: InputStream!): Document!
```

Parse the content of the given`InputStream`as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. An`IllegalArgumentException`is thrown if the`InputStream`is null.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](../java.io/InputStream.md)!:InputStream containing the content to be parsed. |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | `Document`result of parsing the`InputStream` |

| Exceptions ||
|----------------------------|----------------------------|
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any parse errors occur. |

**See Also**

- [org.xml.sax.DocumentHandler](../org.xml.sax/DocumentHandler.md) 

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
| `is` | [InputStream](../java.io/InputStream.md)!:InputStream containing the content to be parsed. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Provide a base for resolving relative URIs. |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | A new DOM Document object. |

| Exceptions ||
|----------------------------|----------------------------|
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any parse errors occur. |

**See Also**

- [org.xml.sax.DocumentHandler](../org.xml.sax/DocumentHandler.md) 

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

- [org.xml.sax.DocumentHandler](../org.xml.sax/DocumentHandler.md) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parse(is: InputSource!): Document!
```

Parse the content of the given input source as an XML document and return a new DOM [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) object. An`IllegalArgumentException`is thrown if the`InputSource`is`null`null.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputSource](../org.xml.sax/InputSource.md)!:InputSource containing the content to be parsed. |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | A new DOM Document object. |

| Exceptions ||
|----------------------------|----------------------------|
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any parse errors occur. |

**See Also**

- [org.xml.sax.DocumentHandler](../org.xml.sax/DocumentHandler.md) 

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Reset this`DocumentBuilder`.
This method removes both the`EntityResolver`and`ErrorHandler`instances associated with this`DocumentBuilder`and sets all internal properties to false including those set by the`DocumentBuilderFactory`when this`DocumentBuilder`was created. 
**See Also**

- [#setEntityResolver(EntityResolver)](DocumentBuilder.md))
- [#setErrorHandler(ErrorHandler)](DocumentBuilder.md))
- [javax.xml.parsers.DocumentBuilderFactory](DocumentBuilderFactory.md) 

### setEntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEntityResolver(er: EntityResolver!): Unit
```

Specify the [EntityResolver](../org.xml.sax/EntityResolver.md) to be used to resolve entities present in the XML document to be parsed. Setting this to`null`will result in the underlying implementation using it's own default implementation and behavior.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `er` | [EntityResolver](../org.xml.sax/EntityResolver.md)!:The`EntityResolver`to be used to resolve entities present in the XML document to be parsed. |

### setErrorHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setErrorHandler(eh: ErrorHandler!): Unit
```

Specify the [ErrorHandler](../org.xml.sax/ErrorHandler.md) to be used by the parser. Setting this to`null`will result in the underlying implementation using it's own default implementation and behavior.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `eh` | [ErrorHandler](../org.xml.sax/ErrorHandler.md)!:The`ErrorHandler`to be used by the parser. |
