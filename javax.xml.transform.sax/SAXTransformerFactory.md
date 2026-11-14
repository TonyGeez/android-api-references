# SAXTransformerFactory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SAXTransformerFactory

```
abstract class SAXTransformerFactory : TransformerFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [javax.xml.transform.TransformerFactory](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#) ||
| | ↳ | [javax.xml.transform.sax.SAXTransformerFactory](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory#) |

This class extends TransformerFactory to provide SAX-specific factory methods. It provides two types of ContentHandlers, one for creating Transformers, the other for creating Templates objects.

If an application wants to set the ErrorHandler or EntityResolver for an XMLReader used during a transformation, it should use a URIResolver to return the SAXSource which provides (with getXMLReader) a reference to the XMLReader.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory#FEATURE:kotlin.String) If [javax.xml.transform.TransformerFactory#getFeature](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String))returns true when passed this value as an argument, the TransformerFactory returned from javax. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_XMLFILTER](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory#FEATURE_XMLFILTER:kotlin.String) If [javax.xml.transform.TransformerFactory#getFeature](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String))returns true when passed this value as an argument, the [newXMLFilter(javax.xml.transform.Source)](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory#newXMLFilter(javax.xml.transform.Source))and [newXMLFilter(javax.xml.transform.Templates)](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory#newXMLFilter(javax.xml.transform.Templates))methods are supported. |

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SAXTransformerFactory](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory#SAXTransformerFactory())`()` The default constructor is protected on purpose. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [TemplatesHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/TemplatesHandler)! | [newTemplatesHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory#newTemplatesHandler())`()` Get a TemplatesHandler object that can process SAX ContentHandler events into a Templates object. |
| abstract [TransformerHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/TransformerHandler)! | [newTransformerHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory#newTransformerHandler())`()` Get a TransformerHandler object that can process SAX ContentHandler events into a Result. |
| abstract [TransformerHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/TransformerHandler)! | [newTransformerHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory#newTransformerHandler(javax.xml.transform.Source))`(`src:` ` [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!`)` Get a TransformerHandler object that can process SAX ContentHandler events into a Result, based on the transformation instructions specified by the argument. |
| --- | --- |
| abstract [TransformerHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/TransformerHandler)! | [newTransformerHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory#newTransformerHandler(javax.xml.transform.Templates))`(`templates:` ` [Templates](https://developer.android.com/reference/kotlin/javax/xml/transform/Templates.html#)!`)` Get a TransformerHandler object that can process SAX ContentHandler events into a Result, based on the Templates argument. |
| abstract [XMLFilter](https://developer.android.com/reference/kotlin/org/xml/sax/XMLFilter.html#)! | [newXMLFilter](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory#newXMLFilter(javax.xml.transform.Source))`(`src:` ` [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!`)` Create an XMLFilter that uses the given Source as the transformation instructions. |
| abstract [XMLFilter](https://developer.android.com/reference/kotlin/org/xml/sax/XMLFilter.html#)! | [newXMLFilter](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory#newXMLFilter(javax.xml.transform.Templates))`(`templates:` ` [Templates](https://developer.android.com/reference/kotlin/javax/xml/transform/Templates.html#)!`)` Create an XMLFilter, based on the Templates argument. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [TransformerFactory](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#) |--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)! | [getAssociatedStylesheet](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getAssociatedStylesheet(javax.xml.transform.Source,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`source:` ` [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!`, `media:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `title:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `charset:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Get the stylesheet specification(s) associated with the XML`Source`document via the [xml-stylesheet processing instruction](http://www.w3.org/TR/xml-stylesheet/) that match the given criteria. Note that it is possible to return several stylesheets, in which case they are applied as if they were a list of imports or cascades in a single stylesheet. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAttribute](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getAttribute(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Allows the user to retrieve specific attributes on the underlying implementation. An`IllegalArgumentException`is thrown if the underlying implementation doesn't recognize the attribute. <br /> | | [ErrorListener](https://developer.android.com/reference/kotlin/javax/xml/transform/ErrorListener.html#)! | [getErrorListener](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getErrorListener())`()` <br /> Get the error event handler for the TransformerFactory. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Look up the value of a feature. Feature names are fully qualified [java.net.URI](https://developer.android.com/reference/kotlin/java/net/URI.html#) s. Implementations may define their own features.`false`is returned if this`TransformerFactory`or the`Transformer`s or`Template`s it creates cannot support the feature. It is possible for an`TransformerFactory`to expose a feature value but be unable to change its state. <br /> | | [URIResolver](https://developer.android.com/reference/kotlin/javax/xml/transform/URIResolver.html#)! | [getURIResolver](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getURIResolver())`()` <br /> Get the object that is used by default during the transformation to resolve URIs used in document(), xsl:import, or xsl:include. <br /> | | [TransformerFactory](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#)! | [newInstance](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#newInstance())`()` <br /> Returns Android's implementation of`TransformerFactory`. Unlike other Java implementations, this method does not consult system properties, properties files, or the services API. <br /> | | [TransformerFactory](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#)! | [newInstance](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#newInstance(kotlin.String,%20java.lang.ClassLoader))`(`factoryClassName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `classLoader:` ` [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!`)` <br /> Returns an instance of the named implementation of`TransformerFactory`. <br /> | | [Templates](https://developer.android.com/reference/kotlin/javax/xml/transform/Templates.html#)! | [newTemplates](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#newTemplates(javax.xml.transform.Source))`(`source:` ` [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!`)` <br /> Process the Source into a Templates object, which is a a compiled representation of the source. This Templates object may then be used concurrently across multiple threads. Creating a Templates object allows the TransformerFactory to do detailed performance optimization of transformation instructions, without penalizing runtime transformation. <br /> | | [Transformer](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer.html#)! | [newTransformer](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#newTransformer())`()` <br /> Create a new`Transformer`that performs a copy of the`Source`to the`Result`. i.e. the "*identity transform*". <br /> | | [Transformer](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer.html#)! | [newTransformer](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#newTransformer(javax.xml.transform.Source))`(`source:` ` [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!`)` <br /> Process the`Source`into a`Transformer``Object`. The`Source`is an XSLT document that conforms to [XSL Transformations (XSLT) Version 1.0](http://www.w3.org/TR/xslt). Care must be taken not to use this`Transformer`in multiple`Thread`s running concurrently. Different`TransformerFactories`can be used concurrently by different`Thread`s. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAttribute](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#setAttribute(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Allows the user to set specific attributes on the underlying implementation. An attribute in this context is defined to be an option that the implementation provides. An`IllegalArgumentException`is thrown if the underlying implementation doesn't recognize the attribute. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorListener](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#setErrorListener(javax.xml.transform.ErrorListener))`(`listener:` ` [ErrorListener](https://developer.android.com/reference/kotlin/javax/xml/transform/ErrorListener.html#)!`)` <br /> Set the error event listener for the TransformerFactory, which is used for the processing of transformation instructions, and not for the transformation itself. An`IllegalArgumentException`is thrown if the`ErrorListener`listener is`null`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#setFeature(kotlin.String,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set a feature for this`TransformerFactory`and`Transformer`s or`Template`s created by this factory. Feature names are fully qualified [java.net.URI](https://developer.android.com/reference/kotlin/java/net/URI.html#) s. Implementations may define their own features. An [TransformerConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerConfigurationException.html#) is thrown if this`TransformerFactory`or the`Transformer`s or`Template`s it creates cannot support the feature. It is possible for an`TransformerFactory`to expose a feature value but be unable to change its state. All implementations are required to support the [javax.xml.XMLConstants#FEATURE_SECURE_PROCESSING](https://developer.android.com/reference/kotlin/javax/xml/XMLConstants.html#FEATURE_SECURE_PROCESSING:kotlin.String) feature. When the feature is: - `true`: the implementation will limit XML processing to conform to implementation limits and behave in a secure fashion as defined by the implementation. Examples include resolving user defined style sheets and functions. If XML processing is limited for security reasons, it will be reported via a call to the registered [ErrorListener.fatalError(TransformerException exception)](https://developer.android.com/reference/kotlin/javax/xml/transform/ErrorListener.html#fatalError(javax.xml.transform.TransformerException)). See [setErrorListener(javax.xml.transform.ErrorListener)](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#setErrorListener(javax.xml.transform.ErrorListener)). - `false`: the implementation will processing XML according to the XML specifications without regard to possible implementation limits. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setURIResolver](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#setURIResolver(javax.xml.transform.URIResolver))`(`resolver:` ` [URIResolver](https://developer.android.com/reference/kotlin/javax/xml/transform/URIResolver.html#)!`)` <br /> Set an object that is used by default during the transformation to resolve URIs used in document(), xsl:import, or xsl:include. <br /> | ||

## Constants

### FEATURE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE: String
```

If [javax.xml.transform.TransformerFactory#getFeature](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String))returns true when passed this value as an argument, the TransformerFactory returned from javax.xml.transform.TransformerFactory#newInstance may be safely cast to a SAXTransformerFactory. 

 Value: "http://javax.xml.transform.sax.SAXTransformerFactory/feature"

### FEATURE_XMLFILTER

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_XMLFILTER: String
```

If [javax.xml.transform.TransformerFactory#getFeature](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String))returns true when passed this value as an argument, the [newXMLFilter(javax.xml.transform.Source)](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory#newXMLFilter(javax.xml.transform.Source))and [newXMLFilter(javax.xml.transform.Templates)](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory#newXMLFilter(javax.xml.transform.Templates))methods are supported. 

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
| [TemplatesHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/TemplatesHandler)! | A non-null reference to a TransformerHandler, that may be used as a ContentHandler for SAX parse events. |

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
| [TransformerHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/TransformerHandler)! | A non-null reference to a TransformerHandler, that may be used as a ContentHandler for SAX parse events. |

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
| `src` | [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!:The Source of the transformation instructions. |

| Return ||
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [TransformerHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/TransformerHandler)! | TransformerHandler ready to transform SAX events. |

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
| `templates` | [Templates](https://developer.android.com/reference/kotlin/javax/xml/transform/Templates.html#)!:The compiled transformation instructions. |

| Return ||
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [TransformerHandler](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/TransformerHandler)! | TransformerHandler ready to transform SAX events. |

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
| `src` | [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!:The Source of the transformation instructions. |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [XMLFilter](https://developer.android.com/reference/kotlin/org/xml/sax/XMLFilter.html#)! | An XMLFilter object, or null if this feature is not supported. |

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
| `templates` | [Templates](https://developer.android.com/reference/kotlin/javax/xml/transform/Templates.html#)!:The compiled transformation instructions. |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [XMLFilter](https://developer.android.com/reference/kotlin/org/xml/sax/XMLFilter.html#)! | An XMLFilter object, or null if this feature is not supported. |

| Exceptions ||
|---------------------------------------------------------|------------------------------------------------------------|
| `javax.xml.transform.TransformerConfigurationException` | If for some reason the TemplatesHandler cannot be created. |
