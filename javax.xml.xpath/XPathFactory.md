# XPathFactory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XPathFactory

```
abstract class XPathFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.xpath.XPathFactory](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#) |

An`XPathFactory`instance can be used to create [javax.xml.xpath.XPath](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPath) objects.

See [newInstance(java.lang.String)](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#newInstance(kotlin.String))for lookup mechanism.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEFAULT_OBJECT_MODEL_URI](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#DEFAULT_OBJECT_MODEL_URI:kotlin.String) Default Object Model URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEFAULT_PROPERTY_NAME](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#DEFAULT_PROPERTY_NAME:kotlin.String) The default property name according to the JAXP spec. |

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [XPathFactory](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#XPathFactory())`()` Protected constructor as [newInstance()](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#newInstance()), [newInstance(java.lang.String)](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#newInstance(kotlin.String))or [newInstance(java.lang.String,java.lang.String,java.lang.ClassLoader)](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#newInstance(kotlin.String,%20kotlin.String,%20java.lang.ClassLoader))should be used to create a new instance of an`XPathFactory`. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#getFeature(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the state of the named feature. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isObjectModelSupported](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#isObjectModelSupported(kotlin.String))`(`objectModel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Is specified object model supported by this`XPathFactory`? |
| static [XPathFactory](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#)! | [newInstance](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#newInstance())`()` Get a new`XPathFactory`instance using the default object model, [DEFAULT_OBJECT_MODEL_URI](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#DEFAULT_OBJECT_MODEL_URI:kotlin.String), the W3C DOM. |
| --- | --- |
| static [XPathFactory](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#)! | [newInstance](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#newInstance(kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get a new`XPathFactory`instance using the specified object model. |
| openstatic [XPathFactory](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#)! | [newInstance](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#newInstance(kotlin.String,%20kotlin.String,%20java.lang.ClassLoader))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `factoryClassName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `classLoader:` ` [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!`)` <br /> |
| abstract [XPath](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPath)! | [newXPath](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#newXPath())`()` Return a new`XPath`using the underlying object model determined when the`XPathFactory`was instantiated. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#setFeature(kotlin.String,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set a feature for this`XPathFactory`and`XPath`s created by this factory. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setXPathFunctionResolver](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#setXPathFunctionResolver(javax.xml.xpath.XPathFunctionResolver))`(`resolver:` ` [XPathFunctionResolver](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFunctionResolver)!`)` Establish a default function resolver. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setXPathVariableResolver](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#setXPathVariableResolver(javax.xml.xpath.XPathVariableResolver))`(`resolver:` ` [XPathVariableResolver](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathVariableResolver)!`)` Establish a default variable resolver. |
| --- | --- |

## Constants

### DEFAULT_OBJECT_MODEL_URI

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_OBJECT_MODEL_URI: String
```

Default Object Model URI. 

 Value: "http://java.sun.com/jaxp/xpath/dom"

### DEFAULT_PROPERTY_NAME

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_PROPERTY_NAME: String
```

The default property name according to the JAXP spec. 

 Value: "javax.xml.xpath.XPathFactory"

## Protected constructors

### XPathFactory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected XPathFactory()
```

Protected constructor as [newInstance()](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#newInstance()), [newInstance(java.lang.String)](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#newInstance(kotlin.String))or [newInstance(java.lang.String,java.lang.String,java.lang.ClassLoader)](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#newInstance(kotlin.String,%20kotlin.String,%20java.lang.ClassLoader))should be used to create a new instance of an`XPathFactory`.

## Public methods

### getFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFeature(name: String!): Boolean
```

Get the state of the named feature.

Feature names are fully qualified [java.net.URI](https://developer.android.com/reference/kotlin/java/net/URI.html#) s. Implementations may define their own features. An [XPathFactoryConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactoryConfigurationException) is thrown if this`XPathFactory`or the`XPath`s it creates cannot support the feature. It is possible for an`XPathFactory`to expose a feature value but be unable to change its state.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Feature name. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | State of the named feature. |

| Exceptions ||
|------------------------------------------------------|-----------------------------------------------------------------------------|
| `javax.xml.xpath.XPathFactoryConfigurationException` | if this`XPathFactory`or the`XPath`s it creates cannot support this feature. |
| `java.lang.NullPointerException` | if`name`is`null`. |

### isObjectModelSupported

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isObjectModelSupported(objectModel: String!): Boolean
```

Is specified object model supported by this`XPathFactory`?

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `objectModel` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Specifies the object model which the returned`XPathFactory`will understand. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`XPathFactory`supports`objectModel`, else`false`. |

| Exceptions ||
|--------------------------------------|--------------------------------|
| `java.lang.NullPointerException` | If`objectModel`is`null`. |
| `java.lang.IllegalArgumentException` | If`objectModel.length() == 0`. |

### newInstance

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInstance(): XPathFactory!
```

Get a new`XPathFactory`instance using the default object model, [DEFAULT_OBJECT_MODEL_URI](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#DEFAULT_OBJECT_MODEL_URI:kotlin.String), the W3C DOM.

This method is functionally equivalent to: 

```kotlin
newInstance(DEFAULT_OBJECT_MODEL_URI)
  
```

Since the implementation for the W3C DOM is always available, this method will never fail.

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------|
| [XPathFactory](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#)! | Instance of an`XPathFactory`. |

### newInstance

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInstance(uri: String!): XPathFactory!
```

Get a new`XPathFactory`instance using the specified object model.

To find a`XPathFactory`object, this method looks the following places in the following order where "the class loader" refers to the context class loader:

1. If the system property [DEFAULT_PROPERTY_NAME](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#DEFAULT_PROPERTY_NAME:kotlin.String)+ ":uri" is present, where uri is the parameter to this method, then its value is read as a class name. The method will try to create a new instance of this class by using the class loader, and returns it if it is successfully created.
2. ${java.home}/lib/jaxp.properties is read and the value associated with the key being the system property above is looked for. If present, the value is processed just like above.
3. The class loader is asked for service provider provider-configuration files matching`javax.xml.xpath.XPathFactory`in the resource directory META-INF/services. See the JAR File Specification for file format and parsing rules. Each potential service provider is required to implement the method: 

   ```kotlin
   <code><a docref="javax.xml.xpath.XPathFactory$isObjectModelSupported(kotlin.String)">#isObjectModelSupported(java.lang.String)</a></code>
   ```
 The first service provider found in class loader order that supports the specified object model is returned.
4. Platform default`XPathFactory`is located in a platform specific way. There must be a platform default XPathFactory for the W3C DOM, i.e. [DEFAULT_OBJECT_MODEL_URI](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#DEFAULT_OBJECT_MODEL_URI:kotlin.String).

If everything fails, an`XPathFactoryConfigurationException`will be thrown.

Tip for Trouble-shooting:

See [java.util.Properties#load(java.io.InputStream)](https://developer.android.com/reference/kotlin/java/util/Properties.html#load(java.io.InputStream))for exactly how a property file is parsed. In particular, colons ':' need to be escaped in a property file, so make sure the URIs are properly escaped in it. For example: 

```kotlin
http\://java.sun.com/jaxp/xpath/dom=org.acme.DomXPathFactory
  
```

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Identifies the underlying object model. The specification only defines the URI [DEFAULT_OBJECT_MODEL_URI](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#DEFAULT_OBJECT_MODEL_URI:kotlin.String),`http://java.sun.com/jaxp/xpath/dom`for the W3C DOM, the org.w3c.dom package, and implementations are free to introduce other URIs for other object models. |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------|
| [XPathFactory](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#)! | Instance of an`XPathFactory`. |

| Exceptions ||
|------------------------------------------------------|-----------------------------------------------|
| `javax.xml.xpath.XPathFactoryConfigurationException` | If the specified object model is unavailable. |
| `java.lang.NullPointerException` | If`uri`is`null`. |
| `java.lang.IllegalArgumentException` | If`uri.length() == 0`. |
| --- | --- |

### newInstance

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(
    uri: String!, 
    factoryClassName: String!, 
    classLoader: ClassLoader!
): XPathFactory!
```

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------|
| [XPathFactory](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactory#)! | Instance of an`XPathFactory`. |

| Exceptions ||
|------------------------------------------------------|-----------------------------------------------|
| `javax.xml.xpath.XPathFactoryConfigurationException` | If the specified object model is unavailable. |
| `java.lang.NullPointerException` | If`uri`is`null`. |
| `java.lang.IllegalArgumentException` | If`uri.length() == 0`. |
| --- | --- |

### newXPath

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newXPath(): XPath!
```

Return a new`XPath`using the underlying object model determined when the`XPathFactory`was instantiated.

| Return ||
|--------------------------------------------------------------------------------|----------------------------|
| [XPath](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPath)! | New instance of an`XPath`. |

### setFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFeature(
    name: String!, 
    value: Boolean
): Unit
```

Set a feature for this`XPathFactory`and`XPath`s created by this factory.

Feature names are fully qualified [java.net.URI](https://developer.android.com/reference/kotlin/java/net/URI.html#) s. Implementations may define their own features. An [XPathFactoryConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactoryConfigurationException) is thrown if this`XPathFactory`or the`XPath`s it creates cannot support the feature. It is possible for an`XPathFactory`to expose a feature value but be unable to change its state.

All implementations are required to support the [javax.xml.XMLConstants#FEATURE_SECURE_PROCESSING](https://developer.android.com/reference/kotlin/javax/xml/XMLConstants.html#FEATURE_SECURE_PROCESSING:kotlin.String) feature. When the feature is`true`, any reference to an external function is an error. Under these conditions, the implementation must not call the [XPathFunctionResolver](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFunctionResolver) and must throw an [XPathFunctionException](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFunctionException).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Feature name. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Is feature state`true`or`false`. |

| Exceptions ||
|------------------------------------------------------|-----------------------------------------------------------------------------|
| `javax.xml.xpath.XPathFactoryConfigurationException` | if this`XPathFactory`or the`XPath`s it creates cannot support this feature. |
| `java.lang.NullPointerException` | if`name`is`null`. |

### setXPathFunctionResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setXPathFunctionResolver(resolver: XPathFunctionResolver!): Unit
```

Establish a default function resolver.

Any`XPath`objects constructed from this factory will use the specified resolver by default.

A`NullPointerException`is thrown if`resolver`is`null`.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `resolver` | [XPathFunctionResolver](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFunctionResolver)!:XPath function resolver. |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | If`resolver`is`null`. |

### setXPathVariableResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setXPathVariableResolver(resolver: XPathVariableResolver!): Unit
```

Establish a default variable resolver.

Any`XPath`objects constructed from this factory will use the specified resolver by default.

A`NullPointerException`is thrown if`resolver`is`null`.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `resolver` | [XPathVariableResolver](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathVariableResolver)!:Variable resolver. |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | If`resolver`is`null`. |
