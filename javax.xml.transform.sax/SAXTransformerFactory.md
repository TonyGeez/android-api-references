# SAXTransformerFactory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SAXTransformerFactory

```
abstract class SAXTransformerFactory : TransformerFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [javax.xml.transform.TransformerFactory](../javax/xml/transform/TransformerFactory.md) ||
| | ↳ | [javax.xml.transform.sax.SAXTransformerFactory](../javax/xml/transform/sax/SAXTransformerFactory.md) |

This class extends TransformerFactory to provide SAX-specific factory methods. It provides two types of ContentHandlers, one for creating Transformers, the other for creating Templates objects.

If an application wants to set the ErrorHandler or EntityResolver for an XMLReader used during a transformation, it should use a URIResolver to return the SAXSource which provides (with getXMLReader) a reference to the XMLReader.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE](../javax/xml/transform/sax/SAXTransformerFactory.md) If [javax.xml.transform.TransformerFactory#getFeature](../javax/xml/transform/TransformerFactory.md))returns true when passed this value as an argument, the TransformerFactory returned from javax. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_XMLFILTER](../javax/xml/transform/sax/SAXTransformerFactory.md) If [javax.xml.transform.TransformerFactory#getFeature](../javax/xml/transform/TransformerFactory.md))returns true when passed this value as an argument, the [newXMLFilter(javax.xml.transform.Source)](../javax/xml/transform/sax/SAXTransformerFactory.md))and [newXMLFilter(javax.xml.transform.Templates)](../javax/xml/transform/sax/SAXTransformerFactory.md))methods are supported. |

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SAXTransformerFactory](../javax/xml/transform/sax/SAXTransformerFactory.md))`()` The default constructor is protected on purpose. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [TemplatesHandler](../javax/xml/transform/sax/TemplatesHandler.md)! | [newTemplatesHandler](../javax/xml/transform/sax/SAXTransformerFactory.md))`()` Get a TemplatesHandler object that can process SAX ContentHandler events into a Templates object. |
| abstract [TransformerHandler](../javax/xml/transform/sax/TransformerHandler.md)! | [newTransformerHandler](../javax/xml/transform/sax/SAXTransformerFactory.md))`()` Get a TransformerHandler object that can process SAX ContentHandler events into a Result. |
| abstract [TransformerHandler](../javax/xml/transform/sax/TransformerHandler.md)! | [newTransformerHandler](../javax/xml/transform/sax/SAXTransformerFactory.md))`(`src:` ` [Source](../javax/xml/transform/Source.md)!`)` Get a TransformerHandler object that can process SAX ContentHandler events into a Result, based on the transformation instructions specified by the argument. |
| --- | --- |
| abstract [TransformerHandler](../javax/xml/transform/sax/TransformerHandler.md)! | [newTransformerHandler](../javax/xml/transform/sax/SAXTransformerFactory.md))`(`templates:` ` [Templates](../javax/xml/transform/Templates.md)!`)` Get a TransformerHandler object that can process SAX ContentHandler events into a Result, based on the Templates argument. |
| abstract [XMLFilter](../org/xml/sax/XMLFilter.md)! | [newXMLFilter](../javax/xml/transform/sax/SAXTransformerFactory.md))`(`src:` ` [Source](../javax/xml/transform/Source.md)!`)` Create an XMLFilter that uses the given Source as the transformation instructions. |
| abstract [XMLFilter](../org/xml/sax/XMLFilter.md)! | [newXMLFilter](../javax/xml/transform/sax/SAXTransformerFactory.md))`(`templates:` ` [Templates](../javax/xml/transform/Templates.md)!`)` Create an XMLFilter, based on the Templates argument. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [TransformerFactory](../javax/xml/transform/TransformerFactory.md) |--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Source](../javax/xml/transform/Source.md)! | [getAssociatedStylesheet](../javax/xml/transform/TransformerFactory.md))`(`source:` ` [Source](../javax/xml/transform/Source.md)!`, `media:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `title:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `charset:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Get the stylesheet specification(s) associated with the XML`Source`document via the [xml-stylesheet processing instruction](http://www.w3.org/TR/xml-stylesheet/) that match the given criteria. Note that it is possible to return several stylesheets, in which case they are applied as if they were a list of imports or cascades in a single stylesheet. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAttribute](../javax/xml/transform/TransformerFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Allows the user to retrieve specific attributes on the underlying implementation. An`IllegalArgumentException`is thrown if the underlying implementation doesn't recognize the attribute. <br /> | | [ErrorListener](../javax/xml/transform/ErrorListener.md)! | [getErrorListener](../javax/xml/transform/TransformerFactory.md))`()` <br /> Get the error event handler for the TransformerFactory. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](../javax/xml/transform/TransformerFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Look up the value of a feature. Feature names are fully qualified [java.net.URI](../java/net/URI.md) s. Implementations may define their own features.`false`is returned if this`TransformerFactory`or the`Transformer`s or`Template`s it creates cannot support the feature. It is possible for an`TransformerFactory`to expose a feature value but be unable to change its state. <br /> | | [URIResolver](../javax/xml/transform/URIResolver.md)! | [getURIResolver](../javax/xml/transform/TransformerFactory.md))`()` <br /> Get the object that is used by default during the transformation to resolve URIs used in document(), xsl:import, or xsl:include. <br /> | | [TransformerFactory](../javax/xml/transform/TransformerFactory.md)! | [newInstance](../javax/xml/transform/TransformerFactory.md))`()` <br /> Returns Android's implementation of`TransformerFactory`. Unlike other Java implementations, this method does not consult system properties, properties files, or the services API. <br /> | | [TransformerFactory](../javax/xml/transform/TransformerFactory.md)! | [newInstance](../javax/xml/transform/TransformerFactory.md))`(`factoryClassName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `classLoader:` ` [ClassLoader](../java/lang/ClassLoader.md)!`)` <br /> Returns an instance of the named implementation of`TransformerFactory`. <br /> | | [Templates](../javax/xml/transform/Templates.md)! | [newTemplates](../javax/xml/transform/TransformerFactory.md))`(`source:` ` [Source](../javax/xml/transform/Source.md)!`)` <br /> Process the Source into a Templates object, which is a a compiled representation of the source. This Templates object may then be used concurrently across multiple threads. Creating a Templates object allows the TransformerFactory to do detailed performance optimization of transformation instructions, without penalizing runtime transformation. <br /> | | [Transformer](../javax/xml/transform/Transformer.md)! | [newTransformer](../javax/xml/transform/TransformerFactory.md))`()` <br /> Create a new`Transformer`that performs a copy of the`Source`to the`Result`. i.e. the "*identity transform*". <br /> | | [Transformer](../javax/xml/transform/Transformer.md)! | [newTransformer](../javax/xml/transform/TransformerFactory.md))`(`source:` ` [Source](../javax/xml/transform/Source.md)!`)` <br /> Process the`Source`into a`Transformer``Object`. The`Source`is an XSLT document that conforms to [XSL Transformations (XSLT) Version 1.0](http://www.w3.org/TR/xslt). Care must be taken not to use this`Transformer`in multiple`Thread`s running concurrently. Different`TransformerFactories`can be used concurrently by different`Thread`s. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAttribute](../javax/xml/transform/TransformerFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Allows the user to set specific attributes on the underlying implementation. An attribute in this context is defined to be an option that the implementation provides. An`IllegalArgumentException`is thrown if the underlying implementation doesn't recognize the attribute. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorListener](../javax/xml/transform/TransformerFactory.md))`(`listener:` ` [ErrorListener](../javax/xml/transform/ErrorListener.md)!`)` <br /> Set the error event listener for the TransformerFactory, which is used for the processing of transformation instructions, and not for the transformation itself. An`IllegalArgumentException`is thrown if the`ErrorListener`listener is`null`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](../javax/xml/transform/TransformerFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set a feature for this`TransformerFactory`and`Transformer`s or`Template`s created by this factory. Feature names are fully qualified [java.net.URI](../java/net/URI.md) s. Implementations may define their own features. An [TransformerConfigurationException](../javax/xml/transform/TransformerConfigurationException.md) is thrown if this`TransformerFactory`or the`Transformer`s or`Template`s it creates cannot support the feature. It is possible for an`TransformerFactory`to expose a feature value but be unable to change its state. All implementations are required to support the [javax.xml.XMLConstants#FEATURE_SECURE_PROCESSING](../javax/xml/XMLConstants.md) feature. When the feature is: - `true`: the implementation will limit XML processing to conform to implementation limits and behave in a secure fashion as defined by the implementation. Examples include resolving user defined style sheets and functions. If XML processing is limited for security reasons, it will be reported via a call to the registered [ErrorListener.fatalError(TransformerException exception)](../javax/xml/transform/ErrorListener.md)). See [setErrorListener(javax.xml.transform.ErrorListener)](../javax/xml/transform/TransformerFactory.md)). - `false`: the implementation will processing XML according to the XML specifications without regard to possible implementation limits. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setURIResolver](../javax/xml/transform/TransformerFactory.md))`(`resolver:` ` [URIResolver](../javax/xml/transform/URIResolver.md)!`)` <br /> Set an object that is used by default during the transformation to resolve URIs used in document(), xsl:import, or xsl:include. <br /> | ||

## Constants

### FEATURE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE: String
```

If [javax.xml.transform.TransformerFactory#getFeature](../javax/xml/transform/TransformerFactory.md))returns true when passed this value as an argument, the TransformerFactory returned from javax.xml.transform.TransformerFactory#newInstance may be safely cast to a SAXTransformerFactory. 

 Value: "http://javax.xml.transform.sax.SAXTransformerFactory/feature"

### FEATURE_XMLFILTER

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_XMLFILTER: String
```

If [javax.xml.transform.TransformerFactory#getFeature](../javax/xml/transform/TransformerFactory.md))returns true when passed this value as an argument, the [newXMLFilter(javax.xml.transform.Source)](../javax/xml/transform/sax/SAXTransformerFactory.md))and [newXMLFilter(javax.xml.transform.Templates)](../javax/xml/transform/sax/SAXTransformerFactory.md))methods are supported. 

 Value: "http://javax.xml.transform.sax.SAXTransformerFactory/feature/xmlfilter"

## Protected constructors

### SAXTransformerFactory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SAXTransformerFactory()
```

The default constructor is protected on purpose.

## Public methods

### newTemplatesHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newTemplatesHandler(): TemplatesHandler!
```

Get a TemplatesHandler object that can process SAX ContentHandler events into a Templates object.

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [TemplatesHandler](../javax/xml/transform/sax/TemplatesHandler.md)! | A non-null reference to a TransformerHandler, that may be used as a ContentHandler for SAX parse events. |

| Exceptions ||
|---------------------------------------------------------|------------------------------------------------------------|
| `javax.xml.transform.TransformerConfigurationException` | If for some reason the TemplatesHandler cannot be created. |

### newTransformerHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newTransformerHandler(): TransformerHandler!
```

Get a TransformerHandler object that can process SAX ContentHandler events into a Result. The transformation is defined as an identity (or copy) transformation, for example to copy a series of SAX parse events into a DOM tree.

| Return ||
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [TransformerHandler](../javax/xml/transform/sax/TransformerHandler.md)! | A non-null reference to a TransformerHandler, that may be used as a ContentHandler for SAX parse events. |

| Exceptions ||
|---------------------------------------------------------|--------------------------------------------------------------|
| `javax.xml.transform.TransformerConfigurationException` | If for some reason the TransformerHandler cannot be created. |

### newTransformerHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newTransformerHandler(src: Source!): TransformerHandler!
```

Get a TransformerHandler object that can process SAX ContentHandler events into a Result, based on the transformation instructions specified by the argument.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [Source](../javax/xml/transform/Source.md)!:The Source of the transformation instructions. |

| Return ||
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [TransformerHandler](../javax/xml/transform/sax/TransformerHandler.md)! | TransformerHandler ready to transform SAX events. |

| Exceptions ||
|---------------------------------------------------------|---------------------------------------------------------------|
| `javax.xml.transform.TransformerConfigurationException` | If for some reason the TransformerHandler can not be created. |

### newTransformerHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newTransformerHandler(templates: Templates!): TransformerHandler!
```

Get a TransformerHandler object that can process SAX ContentHandler events into a Result, based on the Templates argument.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `templates` | [Templates](../javax/xml/transform/Templates.md)!:The compiled transformation instructions. |

| Return ||
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [TransformerHandler](../javax/xml/transform/sax/TransformerHandler.md)! | TransformerHandler ready to transform SAX events. |

| Exceptions ||
|---------------------------------------------------------|---------------------------------------------------------------|
| `javax.xml.transform.TransformerConfigurationException` | If for some reason the TransformerHandler can not be created. |

### newXMLFilter

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newXMLFilter(src: Source!): XMLFilter!
```

Create an XMLFilter that uses the given Source as the transformation instructions.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [Source](../javax/xml/transform/Source.md)!:The Source of the transformation instructions. |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [XMLFilter](../org/xml/sax/XMLFilter.md)! | An XMLFilter object, or null if this feature is not supported. |

| Exceptions ||
|---------------------------------------------------------|------------------------------------------------------------|
| `javax.xml.transform.TransformerConfigurationException` | If for some reason the TemplatesHandler cannot be created. |

### newXMLFilter

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newXMLFilter(templates: Templates!): XMLFilter!
```

Create an XMLFilter, based on the Templates argument..

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `templates` | [Templates](../javax/xml/transform/Templates.md)!:The compiled transformation instructions. |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [XMLFilter](../org/xml/sax/XMLFilter.md)! | An XMLFilter object, or null if this feature is not supported. |

| Exceptions ||
|---------------------------------------------------------|------------------------------------------------------------|
| `javax.xml.transform.TransformerConfigurationException` | If for some reason the TemplatesHandler cannot be created. |
