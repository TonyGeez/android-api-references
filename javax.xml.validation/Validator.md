# Validator

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Validator

```
abstract class Validator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.validation.Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) |

A processor that checks an XML document against [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema).

A validator is a thread-unsafe and non-reentrant object. In other words, it is the application's responsibility to make sure that one [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) object is not used from more than one thread at any given time, and while the validate method is invoked, applications may not recursively call the validate method.

Note that while the [validate(javax.xml.transform.Source)](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#validate(javax.xml.transform.Source))and [validate(javax.xml.transform.Source,javax.xml.transform.Result)](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#validate(javax.xml.transform.Source,%20javax.xml.transform.Result))methods take a [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#) instance, the`Source`instance must be a`SAXSource`,`DOMSource`,`StAXSource`or`StreamSource`.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#Validator())`()` Constructor for derived classes. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)! | [getErrorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#getErrorHandler())`()` Gets the current [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) set to this [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#getFeature(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a feature flag. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getProperty](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#getProperty(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a property. |
| --- | --- |
| abstract [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#)! | [getResourceResolver](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#getResourceResolver())`()` Gets the current [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) set to this [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#reset())`()` Reset this`Validator`to its original configuration. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#setErrorHandler(org.xml.sax.ErrorHandler))`(`errorHandler:` ` [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)!`)` Sets the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) to receive errors encountered during the`validate`method invocation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#setFeature(kotlin.String,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the value of a feature flag. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#setProperty(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Set the value of a property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceResolver](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#setResourceResolver(org.w3c.dom.ls.LSResourceResolver))`(`resourceResolver:` ` [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#)!`)` Sets the [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) to customize resource resolution while in a validation episode. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [validate](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#validate(javax.xml.transform.Source))`(`source:` ` [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!`)` Validates the specified input. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [validate](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#validate(javax.xml.transform.Source,%20javax.xml.transform.Result))`(`source:` ` [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!`, `result:` ` [Result](https://developer.android.com/reference/kotlin/javax/xml/transform/Result.html#)!`)` Validates the specified input and send the augmented validation result to the specified output. |

## Protected constructors

### Validator

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Validator()
```

Constructor for derived classes.

The constructor does nothing.

Derived classes must create [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) objects that have null [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) and null [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#).

## Public methods

### getErrorHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getErrorHandler(): ErrorHandler!
```

Gets the current [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) set to this [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#).

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)! | This method returns the object that was last set through the [setErrorHandler(org.xml.sax.ErrorHandler)](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#setErrorHandler(org.xml.sax.ErrorHandler))method, or null if that method has never been called since this [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) has created. |

**See Also**

- [#setErrorHandler(ErrorHandler)](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#setErrorHandler(org.xml.sax.ErrorHandler)) 

### getFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFeature(name: String!): Boolean
```

Look up the value of a feature flag.

The feature name is any fully-qualified URI. It is possible for a [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) to recognize a feature name but temporarily be unable to return its value. Some feature values may be available only in specific contexts, such as before, during, or after a validation.

Implementors are free (and encouraged) to invent their own features, using names built on their own URIs.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The feature name, which is a non-null fully-qualified URI. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The current value of the feature (true or false). |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | When the name parameter is null. |
| `org.xml.sax.SAXNotRecognizedException` | If the feature value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) recognizes the feature name but cannot determine its value at this time. |
| --- | --- |

**See Also**

- [#setFeature(String, boolean)](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#setFeature(kotlin.String,%20kotlin.Boolean)) 

### getProperty

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProperty(name: String!): Any!
```

Look up the value of a property.

The property name is any fully-qualified URI. It is possible for a [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) to recognize a property name but temporarily be unable to return its value. Some property values may be available only in specific contexts, such as before, during, or after a validation.

[Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) s are not required to recognize any specific property names.

Implementors are free (and encouraged) to invent their own properties, using names built on their own URIs.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property name, which is a non-null fully-qualified URI. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The current value of the property. |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | When the name parameter is null. |
| `org.xml.sax.SAXNotRecognizedException` | If the property value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the XMLReader recognizes the property name but cannot determine its value at this time. |
| --- | --- |

**See Also**

- [#setProperty(String, Object)](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#setProperty(kotlin.String,%20kotlin.Any)) 

### getResourceResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getResourceResolver(): LSResourceResolver!
```

Gets the current [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) set to this [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#).

| Return ||
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#)! | This method returns the object that was last set through the [setResourceResolver(org.w3c.dom.ls.LSResourceResolver)](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#setResourceResolver(org.w3c.dom.ls.LSResourceResolver))method, or null if that method has never been called since this [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) has created. |

**See Also**

- [#setErrorHandler(ErrorHandler)](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#setErrorHandler(org.xml.sax.ErrorHandler)) 

### reset

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reset(): Unit
```

Reset this`Validator`to its original configuration.

`Validator`is reset to the same state as when it was created with [Schema.newValidator()](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema#newValidator()).`reset()`is designed to allow the reuse of existing`Validator`s thus saving resources associated with the creation of new`Validator`s.

The reset`Validator`is not guaranteed to have the same [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) or [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)`Object`s, e.g. [Object.equals(Object obj)](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)). It is guaranteed to have a functionally equal`LSResourceResolver`and`ErrorHandler`. 

### setErrorHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setErrorHandler(errorHandler: ErrorHandler!): Unit
```

Sets the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) to receive errors encountered during the`validate`method invocation.

Error handler can be used to customize the error handling process during a validation. When an [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) is set, errors found during the validation will be first sent to the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#).

The error handler can abort further validation immediately by throwing [SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException.html#) from the handler. Or for example it can print an error to the screen and try to continue the validation by returning normally from the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)

If any [Throwable](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#) is thrown from an [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#), the caller of the`validate`method will be thrown the same [Throwable](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#) object.

[Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) is not allowed to throw [SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException.html#) without first reporting it to [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#).

When the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) is null, the implementation will behave as if the following [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) is set: 

```kotlin
class DraconianErrorHandler implements <code><a docref="org.xml.sax.ErrorHandler">ErrorHandler</a></code>{
      public void fatalError( <code><a docref="org.xml.sax.SAXParseException">org.xml.sax.SAXParseException</a></code>e ) throws <code><a docref="org.xml.sax.SAXException">SAXException</a></code>{
          throw e;
      }
      public void error( <code><a docref="org.xml.sax.SAXParseException">org.xml.sax.SAXParseException</a></code>e ) throws <code><a docref="org.xml.sax.SAXException">SAXException</a></code>{
          throw e;
      }
      public void warning( <code><a docref="org.xml.sax.SAXParseException">org.xml.sax.SAXParseException</a></code>e ) throws <code><a docref="org.xml.sax.SAXException">SAXException</a></code>{
          // noop
      }
  }
  
```

When a new [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) object is created, initially this field is set to null.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorHandler` | [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)!:A new error handler to be set. This parameter can be null. |

### setFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFeature(
    name: String!, 
    value: Boolean
): Unit
```

Set the value of a feature flag.

Feature can be used to control the way a [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) parses schemas, although [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) s are not required to recognize any specific property names.

The feature name is any fully-qualified URI. It is possible for a [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) to expose a feature value but to be unable to change the current value. Some feature values may be immutable or mutable only in specific contexts, such as before, during, or after a validation.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The feature name, which is a non-null fully-qualified URI. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The requested value of the feature (true or false). |

| Exceptions ||
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | When the name parameter is null. |
| `org.xml.sax.SAXNotRecognizedException` | If the feature value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) recognizes the feature name but cannot set the requested value. |
| --- | --- |

**See Also**

- [#getFeature(String)](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#getFeature(kotlin.String)) 

### setProperty

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProperty(
    name: String!, 
    object: Any!
): Unit
```

Set the value of a property.

The property name is any fully-qualified URI. It is possible for a [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) to recognize a property name but to be unable to change the current value. Some property values may be immutable or mutable only in specific contexts, such as before, during, or after a validation.

[Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) s are not required to recognize setting any specific property names.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property name, which is a non-null fully-qualified URI. |
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The requested value for the property. |

| Exceptions ||
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | When the name parameter is null. |
| `org.xml.sax.SAXNotRecognizedException` | If the property value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) recognizes the property name but cannot set the requested value. |
| --- | --- |

### setResourceResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setResourceResolver(resourceResolver: LSResourceResolver!): Unit
```

Sets the [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) to customize resource resolution while in a validation episode.

[Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) uses a [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) when it needs to locate external resources while a validation, although exactly what constitutes "locating external resources" is up to each schema language.

When the [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) is null, the implementation will behave as if the following [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) is set: 

```kotlin
class DumbLSResourceResolver implements <code><a docref="org.w3c.dom.ls.LSResourceResolver">LSResourceResolver</a></code>{
      public <code><a docref="org.w3c.dom.ls.LSInput">org.w3c.dom.ls.LSInput</a></code>resolveResource(
          String publicId, String systemId, String baseURI) {
 
          return null; // always return null
      }
  }
  
```

If a [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) throws a [RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#)(or instances of its derived classes), then the [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) will abort the parsing and the caller of the`validate`method will receive the same [RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#).

When a new [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#) object is created, initially this field is set to null.

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resourceResolver` | [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#)!:A new resource resolver to be set. This parameter can be null. |

### validate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun validate(source: Source!): Unit
```

Validates the specified input.

This is just a convenience method of: 

```kotlin
validate(source,null);
  
```  
**See Also**

- [#setErrorHandler(ErrorHandler)](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#setErrorHandler(org.xml.sax.ErrorHandler)) 

### validate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun validate(
    source: Source!, 
    result: Result!
): Unit
```

Validates the specified input and send the augmented validation result to the specified output.

This method places the following restrictions on the types of the [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)/ [Result](https://developer.android.com/reference/kotlin/javax/xml/transform/Result.html#) accepted.

#### [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)/ [Result](https://developer.android.com/reference/kotlin/javax/xml/transform/Result.html#) accepted:

| | [javax.xml.transform.sax.SAXSource](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource.html#) | [javax.xml.transform.dom.DOMSource](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMSource.html#) | [javax.xml.transform.stream.StreamSource](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource.html#) |
| --- | --- | --- | --- |
| null | OK | OK | OK | OK |
| [javax.xml.transform.sax.SAXResult](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXResult.html#) | OK | Err | Err | Err |
| [javax.xml.transform.dom.DOMResult](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult.html#) | Err | OK | Err | Err |
| --- | --- | --- | --- | --- |
| [javax.xml.transform.stream.StreamResult](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult.html#) | Err | Err | Err | OK |

To validate one [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#) into another kind of [Result](https://developer.android.com/reference/kotlin/javax/xml/transform/Result.html#), use the identity transformer (see [javax.xml.transform.TransformerFactory#newTransformer()](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#newTransformer())).

Errors found during the validation is sent to the specified [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#).

If a document is valid, or if a document contains some errors but none of them were fatal and the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) didn't throw any exception, then the method returns normally.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!:XML to be validated. Must not be null. |
| `result` | [Result](https://developer.android.com/reference/kotlin/javax/xml/transform/Result.html#)!:The [Result](https://developer.android.com/reference/kotlin/javax/xml/transform/Result.html#) object that receives (possibly augmented) XML. This parameter can be null if the caller is not interested in it. Note that when a [javax.xml.transform.dom.DOMResult](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult.html#) is used, a validator might just pass the same DOM node from [javax.xml.transform.dom.DOMSource](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMSource.html#) to [javax.xml.transform.dom.DOMResult](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult.html#)(in which case source.getNode()==result.getNode()), it might copy the entire DOM tree, or it might alter the node given by the source. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the [Result](https://developer.android.com/reference/kotlin/javax/xml/transform/Result.html#) type doesn't match the [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#) type, or if the specified source is not a [javax.xml.transform.sax.SAXSource](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource.html#), [javax.xml.transform.dom.DOMSource](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMSource.html#) or [javax.xml.transform.stream.StreamSource](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource.html#). |
| `org.xml.sax.SAXException` | If the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) throws a [SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException.html#) or if a fatal error is found and the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) returns normally. |
| `java.io.IOException` | If the validator is processing a [javax.xml.transform.sax.SAXSource](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource.html#) and the underlying [org.xml.sax.XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#) throws an [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#). |
| --- | --- |
| `java.lang.NullPointerException` | If the source parameter is null. |

**See Also**

- [#validate(Source)](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator#validate(javax.xml.transform.Source))
