# TransformerFactory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransformerFactory

```
abstract class TransformerFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.transform.TransformerFactory](TransformerFactory.md) |

| Known Direct Subclasses [SAXTransformerFactory](../javax.xml.transform.sax/SAXTransformerFactory.md) |-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------| | [SAXTransformerFactory](../javax.xml.transform.sax/SAXTransformerFactory.md) | This class extends TransformerFactory to provide SAX-specific factory methods. | |
| --- | --- | --- | --- | --- | --- | --- |

A TransformerFactory instance can be used to create [javax.xml.transform.Transformer](Transformer.md) and [javax.xml.transform.Templates](Templates.md) objects.

The system property that determines which Factory implementation to create is named`"javax.xml.transform.TransformerFactory"`. This property names a concrete subclass of the`TransformerFactory`abstract class. If the property is not defined, a platform default is be used.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TransformerFactory](TransformerFactory.md))`()` Default constructor is protected on purpose. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Source](Source.md)! | [getAssociatedStylesheet](TransformerFactory.md))`(`source:` ` [Source](Source.md)!`, `media:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `title:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `charset:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the stylesheet specification(s) associated with the XML`Source`document via the [xml-stylesheet processing instruction](http://www.w3.org/TR/xml-stylesheet/) that match the given criteria. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAttribute](TransformerFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Allows the user to retrieve specific attributes on the underlying implementation. |
| abstract [ErrorListener](ErrorListener.md)! | [getErrorListener](TransformerFactory.md))`()` Get the error event handler for the TransformerFactory. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](TransformerFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a feature. |
| abstract [URIResolver](URIResolver.md)! | [getURIResolver](TransformerFactory.md))`()` Get the object that is used by default during the transformation to resolve URIs used in document(), xsl:import, or xsl:include. |
| openstatic [TransformerFactory](TransformerFactory.md)! | [newInstance](TransformerFactory.md))`()` Returns Android's implementation of`TransformerFactory`. |
| --- | --- |
| openstatic [TransformerFactory](TransformerFactory.md)! | [newInstance](TransformerFactory.md))`(`factoryClassName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `classLoader:` ` [ClassLoader](../java.lang/ClassLoader.md)!`)` Returns an instance of the named implementation of`TransformerFactory`. |
| abstract [Templates](Templates.md)! | [newTemplates](TransformerFactory.md))`(`source:` ` [Source](Source.md)!`)` Process the Source into a Templates object, which is a a compiled representation of the source. |
| abstract [Transformer](Transformer.md)! | [newTransformer](TransformerFactory.md))`()` Create a new`Transformer`that performs a copy of the`Source`to the`Result`. |
| --- | --- |
| abstract [Transformer](Transformer.md)! | [newTransformer](TransformerFactory.md))`(`source:` ` [Source](Source.md)!`)` Process the`Source`into a`Transformer``Object`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAttribute](TransformerFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Allows the user to set specific attributes on the underlying implementation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorListener](TransformerFactory.md))`(`listener:` ` [ErrorListener](ErrorListener.md)!`)` Set the error event listener for the TransformerFactory, which is used for the processing of transformation instructions, and not for the transformation itself. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](TransformerFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set a feature for this`TransformerFactory`and`Transformer`s or`Template`s created by this factory. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setURIResolver](TransformerFactory.md))`(`resolver:` ` [URIResolver](URIResolver.md)!`)` Set an object that is used by default during the transformation to resolve URIs used in document(), xsl:import, or xsl:include. |

## Protected constructors

### TransformerFactory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected TransformerFactory()
```

Default constructor is protected on purpose.

## Public methods

### getAssociatedStylesheet

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAssociatedStylesheet(
    source: Source!, 
    media: String!, 
    title: String!, 
    charset: String!
): Source!
```

Get the stylesheet specification(s) associated with the XML`Source`document via the [xml-stylesheet processing instruction](http://www.w3.org/TR/xml-stylesheet/) that match the given criteria. Note that it is possible to return several stylesheets, in which case they are applied as if they were a list of imports or cascades in a single stylesheet.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Source](Source.md)!:The XML source document. |
| `media` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The media attribute to be matched. May be null, in which case the preferred templates will be used (i.e. alternate = no). |
| `title` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The value of the title attribute to match. May be null. |
| --- | --- |
| `charset` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The value of the charset attribute to match. May be null. |

| Return ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Source](Source.md)! | A`Source``Object`suitable for passing to the`TransformerFactory`. |

| Exceptions ||
|---------------------------------------------------------|--------------------------------------------------------------------------|
| `javax.xml.transform.TransformerConfigurationException` | An`Exception`is thrown if an error occurs during parsing of the`source`. |

**See Also**

### getAttribute

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttribute(name: String!): Any!
```

Allows the user to retrieve specific attributes on the underlying implementation. An`IllegalArgumentException`is thrown if the underlying implementation doesn't recognize the attribute.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the attribute. |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | value The value of the attribute. |

### getErrorListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getErrorListener(): ErrorListener!
```

Get the error event handler for the TransformerFactory.

| Return ||
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ErrorListener](ErrorListener.md)! | The current error handler, which should never be null. |

### getFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFeature(name: String!): Boolean
```

Look up the value of a feature.

Feature names are fully qualified [java.net.URI](../java.net/URI.md) s. Implementations may define their own features.`false`is returned if this`TransformerFactory`or the`Transformer`s or`Template`s it creates cannot support the feature. It is possible for an`TransformerFactory`to expose a feature value but be unable to change its state.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Feature name. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The current state of the feature,`true`or`false`. |

| Exceptions ||
|----------------------------------|--------------------------------|
| `java.lang.NullPointerException` | If the`name`parameter is null. |

### getURIResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getURIResolver(): URIResolver!
```

Get the object that is used by default during the transformation to resolve URIs used in document(), xsl:import, or xsl:include.

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [URIResolver](URIResolver.md)! | The URIResolver that was set with setURIResolver. |

### newInstance

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(): TransformerFactory!
```

Returns Android's implementation of`TransformerFactory`. Unlike other Java implementations, this method does not consult system properties, properties files, or the services API.

| Exceptions ||
|------------------------------------------------------------|------------------------------------------------------------------------|
| `javax.xml.transform.TransformerFactoryConfigurationError` | never. Included for API compatibility with other Java implementations. |

### newInstance

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(
    factoryClassName: String!, 
    classLoader: ClassLoader!
): TransformerFactory!
```

Returns an instance of the named implementation of`TransformerFactory`.

| Exceptions ||
|------------------------------------------------------------|-----------------------------------------------------------------|
| `javax.xml.transform.TransformerFactoryConfigurationError` | if`factoryClassName`is not available or cannot be instantiated. |

### newTemplates

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newTemplates(source: Source!): Templates!
```

Process the Source into a Templates object, which is a a compiled representation of the source. This Templates object may then be used concurrently across multiple threads. Creating a Templates object allows the TransformerFactory to do detailed performance optimization of transformation instructions, without penalizing runtime transformation.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Source](Source.md)!:An object that holds a URL, input stream, etc. |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Templates](Templates.md)! | A Templates object capable of being used for transformation purposes, never null. |

| Exceptions ||
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| `javax.xml.transform.TransformerConfigurationException` | May throw this during the parse when it is constructing the Templates object and fails. |

### newTransformer

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newTransformer(): Transformer!
```

Create a new`Transformer`that performs a copy of the`Source`to the`Result`. i.e. the "*identity transform*".

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Transformer](Transformer.md)! | A Transformer object that may be used to perform a transformation in a single thread, never null. |

| Exceptions ||
|---------------------------------------------------------|----------------------------------------------------------------|
| `javax.xml.transform.TransformerConfigurationException` | Thrown if it is not possible to create a`Transformer`instance. |

### newTransformer

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newTransformer(source: Source!): Transformer!
```

Process the`Source`into a`Transformer``Object`. The`Source`is an XSLT document that conforms to [XSL Transformations (XSLT) Version 1.0](http://www.w3.org/TR/xslt). Care must be taken not to use this`Transformer`in multiple`Thread`s running concurrently. Different`TransformerFactories`can be used concurrently by different`Thread`s.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Source](Source.md)!:`Source `of XSLT document used to create`Transformer`. Examples of XML`Source`s include [StreamSource](../javax.xml.transform.stream/StreamSource.md), [SAXSource](../javax.xml.transform.sax/SAXSource.md) and [DOMSource](../javax.xml.transform.dom/DOMSource.md). |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Transformer](Transformer.md)! | A`Transformer`object that may be used to perform a transformation in a single`Thread`, never`null`. |

| Exceptions ||
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| `javax.xml.transform.TransformerConfigurationException` | Thrown if there are errors when parsing the`Source`or it is not possible to create a`Transformer`instance. |

**See Also**

### setAttribute

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAttribute(
    name: String!, 
    value: Any!
): Unit
```

Allows the user to set specific attributes on the underlying implementation. An attribute in this context is defined to be an option that the implementation provides. An`IllegalArgumentException`is thrown if the underlying implementation doesn't recognize the attribute.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the attribute. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The value of the attribute. |

### setErrorListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setErrorListener(listener: ErrorListener!): Unit
```

Set the error event listener for the TransformerFactory, which is used for the processing of transformation instructions, and not for the transformation itself. An`IllegalArgumentException`is thrown if the`ErrorListener`listener is`null`.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `listener` | [ErrorListener](ErrorListener.md)!:The new error listener. |

### setFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFeature(
    name: String!, 
    value: Boolean
): Unit
```

Set a feature for this`TransformerFactory`and`Transformer`s or`Template`s created by this factory.

Feature names are fully qualified [java.net.URI](../java.net/URI.md) s. Implementations may define their own features. An [TransformerConfigurationException](TransformerConfigurationException.md) is thrown if this`TransformerFactory`or the`Transformer`s or`Template`s it creates cannot support the feature. It is possible for an`TransformerFactory`to expose a feature value but be unable to change its state.

All implementations are required to support the [javax.xml.XMLConstants#FEATURE_SECURE_PROCESSING](../javax.xml/XMLConstants.md) feature. When the feature is:

- `true`: the implementation will limit XML processing to conform to implementation limits and behave in a secure fashion as defined by the implementation. Examples include resolving user defined style sheets and functions. If XML processing is limited for security reasons, it will be reported via a call to the registered [ErrorListener.fatalError(TransformerException exception)](ErrorListener.md)). See [setErrorListener(javax.xml.transform.ErrorListener)](TransformerFactory.md)).
- `false`: the implementation will processing XML according to the XML specifications without regard to possible implementation limits.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Feature name. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Is feature state`true`or`false`. |

| Exceptions ||
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| `javax.xml.transform.TransformerConfigurationException` | if this`TransformerFactory`or the`Transformer`s or`Template`s it creates cannot support this feature. |
| `java.lang.NullPointerException` | If the`name`parameter is null. |

### setURIResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setURIResolver(resolver: URIResolver!): Unit
```

Set an object that is used by default during the transformation to resolve URIs used in document(), xsl:import, or xsl:include.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resolver` | [URIResolver](URIResolver.md)!:An object that implements the URIResolver interface, or null. |
