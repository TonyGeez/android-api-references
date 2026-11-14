# SAXParser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SAXParser

```
abstract class SAXParser
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.xml.parsers.SAXParser](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#) |

Defines the API that wraps an [org.xml.sax.XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#) implementation class. In JAXP 1.0, this class wrapped the [org.xml.sax.Parser](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#) interface, however this interface was replaced by the [org.xml.sax.XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#). For ease of transition, this class continues to support the same name and interface as well as supporting new methods. An instance of this class can be obtained from the [javax.xml.parsers.SAXParserFactory#newSAXParser()](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#newSAXParser())method. Once an instance of this class is obtained, XML can be parsed from a variety of input sources. These input sources are InputStreams, Files, URLs, and SAX InputSources.

This static method creates a new factory instance based on a system property setting or uses the platform default if no property has been defined.

The system property that controls which Factory implementation to create is named`"javax.xml.parsers.SAXParserFactory"`. This property names a class that is a concrete subclass of this abstract class. If no property is defined, a platform default will be used.
As the content is parsed by the underlying parser, methods of the given [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#) or the [org.xml.sax.helpers.DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#) are called.

Implementations of this class which wrap an underlying implementation can consider using the [org.xml.sax.helpers.ParserAdapter](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserAdapter.html#) class to initially adapt their SAX1 implementation to work under this revised class.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SAXParser](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#SAXParser())`()` Protected constructor to prevent instantiation. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Parser](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#)! | [getParser](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#getParser())`()` Returns the SAX parser that is encapsulated by the implementation of this class. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getProperty](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#getProperty(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the particular property requested for in the underlying implementation of [org.xml.sax.XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#). |
| open [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#)! | [getSchema](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#getSchema())`()` Get a reference to the the [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#) being used by the XML processor. |
| abstract [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#)! | [getXMLReader](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#getXMLReader())`()` Returns the [org.xml.sax.XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#) that is encapsulated by the implementation of this class. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNamespaceAware](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#isNamespaceAware())`()` Indicates whether or not this parser is configured to understand namespaces. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidating](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#isValidating())`()` Indicates whether or not this parser is configured to validate XML documents. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isXIncludeAware](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#isXIncludeAware())`()` Get the XInclude processing mode for this parser. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#parse(java.io.File,%20org.xml.sax.HandlerBase))`(`f:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`, `hb:` ` [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#)!`)` Parse the content of the file specified as XML using the specified [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#parse(java.io.File,%20org.xml.sax.helpers.DefaultHandler))`(`f:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`, `dh:` ` [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#)!`)` Parse the content of the file specified as XML using the specified [org.xml.sax.helpers.DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#parse(java.io.InputStream,%20org.xml.sax.HandlerBase))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `hb:` ` [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#)!`)` Parse the content of the given [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) instance as XML using the specified [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#parse(java.io.InputStream,%20org.xml.sax.HandlerBase,%20kotlin.String))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `hb:` ` [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse the content of the given [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) instance as XML using the specified [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#parse(java.io.InputStream,%20org.xml.sax.helpers.DefaultHandler))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `dh:` ` [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#)!`)` Parse the content of the given [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) instance as XML using the specified [org.xml.sax.helpers.DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#parse(java.io.InputStream,%20org.xml.sax.helpers.DefaultHandler,%20kotlin.String))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `dh:` ` [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse the content of the given [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) instance as XML using the specified [org.xml.sax.helpers.DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#parse(kotlin.String,%20org.xml.sax.HandlerBase))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `hb:` ` [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#)!`)` Parse the content described by the giving Uniform Resource Identifier (URI) as XML using the specified [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#parse(kotlin.String,%20org.xml.sax.helpers.DefaultHandler))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `dh:` ` [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#)!`)` Parse the content described by the giving Uniform Resource Identifier (URI) as XML using the specified [org.xml.sax.helpers.DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#parse(org.xml.sax.InputSource,%20org.xml.sax.HandlerBase))`(`is:` ` [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!`, `hb:` ` [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#)!`)` Parse the content given [org.xml.sax.InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#) as XML using the specified [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#parse(org.xml.sax.InputSource,%20org.xml.sax.helpers.DefaultHandler))`(`is:` ` [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!`, `dh:` ` [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#)!`)` Parse the content given [org.xml.sax.InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#) as XML using the specified [org.xml.sax.helpers.DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#reset())`()` Reset this`SAXParser`to its original configuration. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser#setProperty(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the particular property in the underlying implementation of [org.xml.sax.XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#). |

## Protected constructors

### SAXParser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SAXParser()
```

Protected constructor to prevent instantiation. Use [javax.xml.parsers.SAXParserFactory#newSAXParser()](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#newSAXParser()).

## Public methods

### getParser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParser(): Parser!
```

Returns the SAX parser that is encapsulated by the implementation of this class.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Parser](https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#)! | The SAX parser that is encapsulated by the implementation of this class. |

| Exceptions ||
|----------------------------|--------------------------------------------|
| `org.xml.sax.SAXException` | If any SAX errors occur during processing. |

### getProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getProperty(name: String!): Any!
```

Returns the particular property requested for in the underlying implementation of [org.xml.sax.XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property to be retrieved. |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | Value of the requested property. |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | When the underlying XMLReader does not recognize the property name. |
| `org.xml.sax.SAXNotSupportedException` | When the underlying XMLReader recognizes the property name but doesn't support the property. |

**See Also**

- [org.xml.sax.XMLReader#getProperty](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#getProperty(kotlin.String)) 

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

### getXMLReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getXMLReader(): XMLReader!
```

Returns the [org.xml.sax.XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#) that is encapsulated by the implementation of this class.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#)! | The XMLReader that is encapsulated by the implementation of this class. |

| Exceptions ||
|----------------------------|--------------------------------------------|
| `org.xml.sax.SAXException` | If any SAX errors occur during processing. |

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
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the return value of the [SAXParserFactory.isXIncludeAware()](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#isXIncludeAware())when this parser was created from factory. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | For backward compatibility, when implementations for earlier versions of JAXP is used, this exception will be thrown. |

**See Also**

- [javax.xml.parsers.SAXParserFactory#setXIncludeAware(boolean)](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#setXIncludeAware(kotlin.Boolean)) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    f: File!, 
    hb: HandlerBase!
): Unit
```

Parse the content of the file specified as XML using the specified [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#).*Use of the DefaultHandler version of this method is recommended as the HandlerBase class has been deprecated in SAX 2.0*

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------|
| `f` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:The file containing the XML to parse |
| `hb` | [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#)!:The SAX HandlerBase to use. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | If the File object is null. |
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any SAX errors occur during processing. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    f: File!, 
    dh: DefaultHandler!
): Unit
```

Parse the content of the file specified as XML using the specified [org.xml.sax.helpers.DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#).

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `f` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:The file containing the XML to parse |
| `dh` | [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#)!:The SAX DefaultHandler to use. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | If the File object is null. |
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any SAX errors occur during processing. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    is: InputStream!, 
    hb: HandlerBase!
): Unit
```

Parse the content of the given [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) instance as XML using the specified [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#).*Use of the DefaultHandler version of this method is recommended as the HandlerBase class has been deprecated in SAX 2.0*.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:InputStream containing the content to be parsed. |
| `hb` | [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#)!:The SAX HandlerBase to use. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the given InputStream is null. |
| `org.xml.sax.SAXException` | If parse produces a SAX error. |
| `java.io.IOException` | If an IO error occurs interacting with the`InputStream`. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    is: InputStream!, 
    hb: HandlerBase!, 
    systemId: String!
): Unit
```

Parse the content of the given [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) instance as XML using the specified [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#).*Use of the DefaultHandler version of this method is recommended as the HandlerBase class has been deprecated in SAX 2.0*.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:InputStream containing the content to be parsed. |
| `hb` | [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#)!:The SAX HandlerBase to use. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The systemId which is needed for resolving relative URIs. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the given`InputStream`is`null`. |
| `java.io.IOException` | If any IO error occurs interacting with the`InputStream`. |
| `org.xml.sax.SAXException` | If any SAX errors occur during processing. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    is: InputStream!, 
    dh: DefaultHandler!
): Unit
```

Parse the content of the given [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) instance as XML using the specified [org.xml.sax.helpers.DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#).

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:InputStream containing the content to be parsed. |
| `dh` | [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#)!:The SAX DefaultHandler to use. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | If the given InputStream is null. |
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any SAX errors occur during processing. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    is: InputStream!, 
    dh: DefaultHandler!, 
    systemId: String!
): Unit
```

Parse the content of the given [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) instance as XML using the specified [org.xml.sax.helpers.DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:InputStream containing the content to be parsed. |
| `dh` | [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#)!:The SAX DefaultHandler to use. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The systemId which is needed for resolving relative URIs. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | If the given InputStream is null. |
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any SAX errors occur during processing. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    uri: String!, 
    hb: HandlerBase!
): Unit
```

Parse the content described by the giving Uniform Resource Identifier (URI) as XML using the specified [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#).*Use of the DefaultHandler version of this method is recommended as the`HandlerBase`class has been deprecated in SAX 2.0*

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The location of the content to be parsed. |
| `hb` | [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#)!:The SAX HandlerBase to use. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | If the uri is null. |
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any SAX errors occur during processing. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    uri: String!, 
    dh: DefaultHandler!
): Unit
```

Parse the content described by the giving Uniform Resource Identifier (URI) as XML using the specified [org.xml.sax.helpers.DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#).

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The location of the content to be parsed. |
| `dh` | [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#)!:The SAX DefaultHandler to use. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | If the uri is null. |
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any SAX errors occur during processing. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    is: InputSource!, 
    hb: HandlerBase!
): Unit
```

Parse the content given [org.xml.sax.InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#) as XML using the specified [org.xml.sax.HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#).*Use of the DefaultHandler version of this method is recommended as the HandlerBase class has been deprecated in SAX 2.0*

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!:The InputSource containing the content to be parsed. |
| `hb` | [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase.html#)!:The SAX HandlerBase to use. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | If the`InputSource`object is`null`. |
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any SAX errors occur during processing. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    is: InputSource!, 
    dh: DefaultHandler!
): Unit
```

Parse the content given [org.xml.sax.InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#) as XML using the specified [org.xml.sax.helpers.DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#).

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!:The InputSource containing the content to be parsed. |
| `dh` | [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler.html#)!:The SAX DefaultHandler to use. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | If the`InputSource`object is`null`. |
| `java.io.IOException` | If any IO errors occur. |
| `org.xml.sax.SAXException` | If any SAX errors occur during processing. |

**See Also**

- [org.xml.sax.DocumentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/DocumentHandler.html#) 

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Reset this`SAXParser`to its original configuration.

`SAXParser`is reset to the same state as when it was created with [SAXParserFactory.newSAXParser()](https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#newSAXParser()).`reset()`is designed to allow the reuse of existing`SAXParser`s thus saving resources associated with the creation of new`SAXParser`s.

The reset`SAXParser`is not guaranteed to have the same [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#)`Object`, e.g. [Object.equals(Object obj)](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)). It is guaranteed to have a functionally equal`Schema`. 

### setProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setProperty(
    name: String!, 
    value: Any!
): Unit
```

Sets the particular property in the underlying implementation of [org.xml.sax.XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#). A list of the core features and properties can be found at<http://sax.sourceforge.net/?selected=get-set>.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property to be set. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The value of the property to be set. |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | When the underlying XMLReader does not recognize the property name. |
| `org.xml.sax.SAXNotSupportedException` | When the underlying XMLReader recognizes the property name but doesn't support the property. |

**See Also**

- [org.xml.sax.XMLReader#setProperty](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#setProperty(kotlin.String,%20kotlin.Any))
