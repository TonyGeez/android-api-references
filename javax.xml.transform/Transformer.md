# Transformer

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Transformer

```
abstract class Transformer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.xml.transform.Transformer](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#) |

An instance of this abstract class can transform a source tree into a result tree.

An instance of this class can be obtained with the javax.xml.transform.TransformerFactory#newTransformer method. This instance may then be used to process XML from a variety of sources and write the transformation output to a variety of sinks.

An object of this class may not be used in multiple threads running concurrently. Different Transformers may be used concurrently by different threads.

A`Transformer`may be used multiple times. Parameters and output properties are preserved across transformations.

## Summary

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Transformer](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#Transformer())`()` Default constructor is protected on purpose. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearParameters](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#clearParameters())`()` Clear all parameters set with setParameter. |
| abstract [ErrorListener](https://developer.android.com/reference/kotlin/javax/xml/transform/ErrorListener)! | [getErrorListener](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#getErrorListener())`()` Get the error event handler in effect for the transformation. |
| abstract [Properties](https://developer.android.com/reference/kotlin/java/util/Properties.html#)! | [getOutputProperties](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#getOutputProperties())`()` Get a copy of the output properties for the transformation. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOutputProperty](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#getOutputProperty(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get an output property that is in effect for the transformer. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getParameter](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#getParameter(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get a parameter that was explicitly set with setParameter. |
| abstract [URIResolver](https://developer.android.com/reference/kotlin/javax/xml/transform/URIResolver)! | [getURIResolver](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#getURIResolver())`()` Get an object that will be used to resolve URIs used in document(). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#reset())`()` Reset this`Transformer`to its original configuration. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorListener](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#setErrorListener(javax.xml.transform.ErrorListener))`(`listener:` ` [ErrorListener](https://developer.android.com/reference/kotlin/javax/xml/transform/ErrorListener)!`)` Set the error event listener in effect for the transformation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutputProperties](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#setOutputProperties(java.util.Properties))`(`oformat:` ` [Properties](https://developer.android.com/reference/kotlin/java/util/Properties.html#)!`)` Set the output properties for the transformation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutputProperty](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#setOutputProperty(kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set an output property that will be in effect for the transformation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParameter](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#setParameter(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Add a parameter for the transformation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setURIResolver](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#setURIResolver(javax.xml.transform.URIResolver))`(`resolver:` ` [URIResolver](https://developer.android.com/reference/kotlin/javax/xml/transform/URIResolver)!`)` Set an object that will be used to resolve URIs used in document(). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transform](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#transform(javax.xml.transform.Source,%20javax.xml.transform.Result))`(`xmlSource:` ` [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source)!`, `outputTarget:` ` [Result](https://developer.android.com/reference/kotlin/javax/xml/transform/Result)!`)` Transform the XML`Source`to a`Result`. |

## Protected constructors

### Transformer

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Transformer()
```

Default constructor is protected on purpose.

## Public methods

### clearParameters

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearParameters(): Unit
```

Clear all parameters set with setParameter. 

### getErrorListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getErrorListener(): ErrorListener!
```

Get the error event handler in effect for the transformation. Implementations must provide a default error listener.

| Return ||
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ErrorListener](https://developer.android.com/reference/kotlin/javax/xml/transform/ErrorListener)! | The current error handler, which should never be null. |

### getOutputProperties

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOutputProperties(): Properties!
```

Get a copy of the output properties for the transformation.

The properties returned should contain properties set by the user, and properties set by the stylesheet, and these properties are "defaulted" by default properties specified by [section 16 of the XSL Transformations (XSLT) W3C Recommendation](http://www.w3.org/TR/xslt#output). The properties that were specifically set by the user or the stylesheet should be in the base Properties list, while the XSLT default properties that were not specifically set should be the default Properties list. Thus, getOutputProperties().getProperty(String key) will obtain any property in that was set by [setOutputProperty](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#setOutputProperty(kotlin.String,%20kotlin.String)), [setOutputProperties](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#setOutputProperties(java.util.Properties)), in the stylesheet,*or* the default properties, while getOutputProperties().get(String key) will only retrieve properties that were explicitly set by [setOutputProperty](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#setOutputProperty(kotlin.String,%20kotlin.String)), [setOutputProperties](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#setOutputProperties(java.util.Properties)), or in the stylesheet.

Note that mutation of the Properties object returned will not effect the properties that the transformer contains.

If any of the argument keys are not recognized and are not namespace qualified, the property will be ignored and not returned. In other words the behavior is not orthogonal with [setOutputProperties](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#setOutputProperties(java.util.Properties)).

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Properties](https://developer.android.com/reference/kotlin/java/util/Properties.html#)! | A copy of the set of output properties in effect for the next transformation. |

**See Also**

- [javax.xml.transform.OutputKeys](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys)
- [java.util.Properties](https://developer.android.com/reference/kotlin/java/util/Properties.html#) 

### getOutputProperty

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOutputProperty(name: String!): String!
```

Get an output property that is in effect for the transformer. The property specified may be a property that was set with setOutputProperty, or it may be a property specified in the stylesheet.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A non-null String that specifies an output property name, which may be namespace qualified. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The string value of the output property, or null if no property was found. |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.IllegalArgumentException` | If the property is not supported. |

**See Also**

- [javax.xml.transform.OutputKeys](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys) 

### getParameter

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParameter(name: String!): Any!
```

Get a parameter that was explicitly set with setParameter.

This method does not return a default parameter value, which cannot be determined until the node context is evaluated during the transformation process.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:of`Object`to get |

| Return ||
|-----------------------------------------------------------------------------|--------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | A parameter that has been set with setParameter. |

### getURIResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getURIResolver(): URIResolver!
```

Get an object that will be used to resolve URIs used in document().

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [URIResolver](https://developer.android.com/reference/kotlin/javax/xml/transform/URIResolver)! | An object that implements the URIResolver interface, or null. |

### reset

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Reset this`Transformer`to its original configuration.

`Transformer`is reset to the same state as when it was created with [TransformerFactory.newTransformer()](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory#newTransformer()), [TransformerFactory.newTransformer(Source source)](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory#newTransformer(javax.xml.transform.Source))or [Templates.newTransformer()](https://developer.android.com/reference/kotlin/javax/xml/transform/Templates#newTransformer()).`reset()`is designed to allow the reuse of existing`Transformer`s thus saving resources associated with the creation of new`Transformer`s.

The reset`Transformer`is not guaranteed to have the same [URIResolver](https://developer.android.com/reference/kotlin/javax/xml/transform/URIResolver) or [ErrorListener](https://developer.android.com/reference/kotlin/javax/xml/transform/ErrorListener)`Object`s, e.g. [Object.equals(Object obj)](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)). It is guaranteed to have a functionally equal`URIResolver`and`ErrorListener`. 

### setErrorListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setErrorListener(listener: ErrorListener!): Unit
```

Set the error event listener in effect for the transformation.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `listener` | [ErrorListener](https://developer.android.com/reference/kotlin/javax/xml/transform/ErrorListener)!:The new error listener. |

| Exceptions ||
|--------------------------------------|----------------------|
| `java.lang.IllegalArgumentException` | if listener is null. |

### setOutputProperties

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setOutputProperties(oformat: Properties!): Unit
```

Set the output properties for the transformation. These properties will override properties set in the Templates with xsl:output.

If argument to this function is null, any properties previously set are removed, and the value will revert to the value defined in the templates object.

Pass a qualified property key name as a two-part string, the namespace URI enclosed in curly braces ({}), followed by the local name. If the name has a null URL, the String only contain the local name. An application can safely check for a non-null URI by testing to see if the first character of the name is a '{' character.

For example, if a URI and local name were obtained from an element defined with \<xyz:foo xmlns:xyz="http://xyz.foo.com/yada/baz.html"/\>, then the qualified name would be "{http://xyz.foo.com/yada/baz.html}foo". Note that no prefix is used.
An`IllegalArgumentException`is thrown if any of the argument keys are not recognized and are not namespace qualified.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `oformat` | [Properties](https://developer.android.com/reference/kotlin/java/util/Properties.html#)!:A set of output properties that will be used to override any of the same properties in affect for the transformation. |

**See Also**

- [javax.xml.transform.OutputKeys](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys)
- [java.util.Properties](https://developer.android.com/reference/kotlin/java/util/Properties.html#) 

### setOutputProperty

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setOutputProperty(
    name: String!, 
    value: String!
): Unit
```

Set an output property that will be in effect for the transformation.

Pass a qualified property name as a two-part string, the namespace URI enclosed in curly braces ({}), followed by the local name. If the name has a null URL, the String only contain the local name. An application can safely check for a non-null URI by testing to see if the first character of the name is a '{' character.

For example, if a URI and local name were obtained from an element defined with \<xyz:foo xmlns:xyz="http://xyz.foo.com/yada/baz.html"/\>, then the qualified name would be "{http://xyz.foo.com/yada/baz.html}foo". Note that no prefix is used.

The Properties object that was passed to [setOutputProperties](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#setOutputProperties(java.util.Properties))won't be effected by calling this method.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A non-null String that specifies an output property name, which may be namespace qualified. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The non-null string value of the output property. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the property is not supported, and is not qualified with a namespace. |

**See Also**

- [javax.xml.transform.OutputKeys](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys) 

### setParameter

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setParameter(
    name: String!, 
    value: Any!
): Unit
```

Add a parameter for the transformation.

Pass a qualified name as a two-part string, the namespace URI enclosed in curly braces ({}), followed by the local name. If the name has a null URL, the String only contain the local name. An application can safely check for a non-null URI by testing to see if the first character of the name is a '{' character.

For example, if a URI and local name were obtained from an element defined with \<xyz:foo xmlns:xyz="http://xyz.foo.com/yada/baz.html"/\>, then the qualified name would be "{http://xyz.foo.com/yada/baz.html}foo". Note that no prefix is used.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the parameter, which may begin with a namespace URI in curly braces ({}). |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The value object. This can be any valid Java object. It is up to the processor to provide the proper object coercion or to simply pass the object on for use in an extension. |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | If value is null. |

### setURIResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setURIResolver(resolver: URIResolver!): Unit
```

Set an object that will be used to resolve URIs used in document().

If the resolver argument is null, the URIResolver value will be cleared and the transformer will no longer have a resolver.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resolver` | [URIResolver](https://developer.android.com/reference/kotlin/javax/xml/transform/URIResolver)!:An object that implements the URIResolver interface, or null. |

### transform

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun transform(
    xmlSource: Source!, 
    outputTarget: Result!
): Unit
```

Transform the XML`Source`to a`Result`. Specific transformation behavior is determined by the settings of the`TransformerFactory`in effect when the`Transformer`was instantiated and any modifications made to the`Transformer`instance.

An empty`Source`is represented as an empty document as constructed by [javax.xml.parsers.DocumentBuilder#newDocument()](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder.html#newDocument()). The result of transforming an empty`Source`depends on the transformation behavior; it is not always an empty`Result`.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `xmlSource` | [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source)!:The XML input to transform. |
| `outputTarget` | [Result](https://developer.android.com/reference/kotlin/javax/xml/transform/Result)!:The`Result`of transforming the`xmlSource`. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------|
| `javax.xml.transform.TransformerException` | If an unrecoverable error occurs during the course of the transformation. |
