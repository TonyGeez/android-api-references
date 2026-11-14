# Validator

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Validator

```
abstract class Validator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.validation.Validator](../javax/xml/validation/Validator.md) |

A processor that checks an XML document against [Schema](../javax/xml/validation/Schema.md).

A validator is a thread-unsafe and non-reentrant object. In other words, it is the application's responsibility to make sure that one [Validator](../javax/xml/validation/Validator.md) object is not used from more than one thread at any given time, and while the validate method is invoked, applications may not recursively call the validate method.

Note that while the [validate(javax.xml.transform.Source)](../javax/xml/validation/Validator.md))and [validate(javax.xml.transform.Source,javax.xml.transform.Result)](../javax/xml/validation/Validator.md))methods take a [Source](../javax/xml/transform/Source.md) instance, the`Source`instance must be a`SAXSource`,`DOMSource`,`StAXSource`or`StreamSource`.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Validator](../javax/xml/validation/Validator.md))`()` Constructor for derived classes. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ErrorHandler](../org/xml/sax/ErrorHandler.md)! | [getErrorHandler](../javax/xml/validation/Validator.md))`()` Gets the current [ErrorHandler](../org/xml/sax/ErrorHandler.md) set to this [Validator](../javax/xml/validation/Validator.md). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](../javax/xml/validation/Validator.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a feature flag. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getProperty](../javax/xml/validation/Validator.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a property. |
| --- | --- |
| abstract [LSResourceResolver](../org/w3c/dom/ls/LSResourceResolver.md)! | [getResourceResolver](../javax/xml/validation/Validator.md))`()` Gets the current [LSResourceResolver](../org/w3c/dom/ls/LSResourceResolver.md) set to this [Validator](../javax/xml/validation/Validator.md). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](../javax/xml/validation/Validator.md))`()` Reset this`Validator`to its original configuration. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](../javax/xml/validation/Validator.md))`(`errorHandler:` ` [ErrorHandler](../org/xml/sax/ErrorHandler.md)!`)` Sets the [ErrorHandler](../org/xml/sax/ErrorHandler.md) to receive errors encountered during the`validate`method invocation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](../javax/xml/validation/Validator.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the value of a feature flag. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](../javax/xml/validation/Validator.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Set the value of a property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceResolver](../javax/xml/validation/Validator.md))`(`resourceResolver:` ` [LSResourceResolver](../org/w3c/dom/ls/LSResourceResolver.md)!`)` Sets the [LSResourceResolver](../org/w3c/dom/ls/LSResourceResolver.md) to customize resource resolution while in a validation episode. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [validate](../javax/xml/validation/Validator.md))`(`source:` ` [Source](../javax/xml/transform/Source.md)!`)` Validates the specified input. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [validate](../javax/xml/validation/Validator.md))`(`source:` ` [Source](../javax/xml/transform/Source.md)!`, `result:` ` [Result](../javax/xml/transform/Result.md)!`)` Validates the specified input and send the augmented validation result to the specified output. |

## Protected constructors

### Validator

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Validator()
```

Constructor for derived classes.

The constructor does nothing.

Derived classes must create [Validator](../javax/xml/validation/Validator.md) objects that have null [ErrorHandler](../org/xml/sax/ErrorHandler.md) and null [LSResourceResolver](../org/w3c/dom/ls/LSResourceResolver.md).

## Public methods

### getErrorHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getErrorHandler(): ErrorHandler!
```

Gets the current [ErrorHandler](../org/xml/sax/ErrorHandler.md) set to this [Validator](../javax/xml/validation/Validator.md).

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ErrorHandler](../org/xml/sax/ErrorHandler.md)! | This method returns the object that was last set through the [setErrorHandler(org.xml.sax.ErrorHandler)](../javax/xml/validation/Validator.md))method, or null if that method has never been called since this [Validator](../javax/xml/validation/Validator.md) has created. |

**See Also**

- [#setErrorHandler(ErrorHandler)](../javax/xml/validation/Validator.md)) 

### getFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFeature(name: String!): Boolean
```

Look up the value of a feature flag.

The feature name is any fully-qualified URI. It is possible for a [Validator](../javax/xml/validation/Validator.md) to recognize a feature name but temporarily be unable to return its value. Some feature values may be available only in specific contexts, such as before, during, or after a validation.

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
| `org.xml.sax.SAXNotSupportedException` | When the [Validator](../javax/xml/validation/Validator.md) recognizes the feature name but cannot determine its value at this time. |
| --- | --- |

**See Also**

- [#setFeature(String, boolean)](../javax/xml/validation/Validator.md)) 

### getProperty

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProperty(name: String!): Any!
```

Look up the value of a property.

The property name is any fully-qualified URI. It is possible for a [Validator](../javax/xml/validation/Validator.md) to recognize a property name but temporarily be unable to return its value. Some property values may be available only in specific contexts, such as before, during, or after a validation.

[Validator](../javax/xml/validation/Validator.md) s are not required to recognize any specific property names.

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

- [#setProperty(String, Object)](../javax/xml/validation/Validator.md)) 

### getResourceResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getResourceResolver(): LSResourceResolver!
```

Gets the current [LSResourceResolver](../org/w3c/dom/ls/LSResourceResolver.md) set to this [Validator](../javax/xml/validation/Validator.md).

| Return ||
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LSResourceResolver](../org/w3c/dom/ls/LSResourceResolver.md)! | This method returns the object that was last set through the [setResourceResolver(org.w3c.dom.ls.LSResourceResolver)](../javax/xml/validation/Validator.md))method, or null if that method has never been called since this [Validator](../javax/xml/validation/Validator.md) has created. |

**See Also**

- [#setErrorHandler(ErrorHandler)](../javax/xml/validation/Validator.md)) 

### reset

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reset(): Unit
```

Reset this`Validator`to its original configuration.

`Validator`is reset to the same state as when it was created with [Schema.newValidator()](../javax/xml/validation/Schema.md)).`reset()`is designed to allow the reuse of existing`Validator`s thus saving resources associated with the creation of new`Validator`s.

The reset`Validator`is not guaranteed to have the same [LSResourceResolver](../org/w3c/dom/ls/LSResourceResolver.md) or [ErrorHandler](../org/xml/sax/ErrorHandler.md)`Object`s, e.g. [Object.equals(Object obj)](../java/lang/Object.md)). It is guaranteed to have a functionally equal`LSResourceResolver`and`ErrorHandler`. 

### setErrorHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setErrorHandler(errorHandler: ErrorHandler!): Unit
```

Sets the [ErrorHandler](../org/xml/sax/ErrorHandler.md) to receive errors encountered during the`validate`method invocation.

Error handler can be used to customize the error handling process during a validation. When an [ErrorHandler](../org/xml/sax/ErrorHandler.md) is set, errors found during the validation will be first sent to the [ErrorHandler](../org/xml/sax/ErrorHandler.md).

The error handler can abort further validation immediately by throwing [SAXException](../org/xml/sax/SAXException.md) from the handler. Or for example it can print an error to the screen and try to continue the validation by returning normally from the [ErrorHandler](../org/xml/sax/ErrorHandler.md)

If any [Throwable](../java/lang/Throwable.md) is thrown from an [ErrorHandler](../org/xml/sax/ErrorHandler.md), the caller of the`validate`method will be thrown the same [Throwable](../java/lang/Throwable.md) object.

[Validator](../javax/xml/validation/Validator.md) is not allowed to throw [SAXException](../org/xml/sax/SAXException.md) without first reporting it to [ErrorHandler](../org/xml/sax/ErrorHandler.md).

When the [ErrorHandler](../org/xml/sax/ErrorHandler.md) is null, the implementation will behave as if the following [ErrorHandler](../org/xml/sax/ErrorHandler.md) is set: 

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

When a new [Validator](../javax/xml/validation/Validator.md) object is created, initially this field is set to null.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorHandler` | [ErrorHandler](../org/xml/sax/ErrorHandler.md)!:A new error handler to be set. This parameter can be null. |

### setFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFeature(
    name: String!, 
    value: Boolean
): Unit
```

Set the value of a feature flag.

Feature can be used to control the way a [Validator](../javax/xml/validation/Validator.md) parses schemas, although [Validator](../javax/xml/validation/Validator.md) s are not required to recognize any specific property names.

The feature name is any fully-qualified URI. It is possible for a [Validator](../javax/xml/validation/Validator.md) to expose a feature value but to be unable to change the current value. Some feature values may be immutable or mutable only in specific contexts, such as before, during, or after a validation.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The feature name, which is a non-null fully-qualified URI. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The requested value of the feature (true or false). |

| Exceptions ||
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | When the name parameter is null. |
| `org.xml.sax.SAXNotRecognizedException` | If the feature value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the [Validator](../javax/xml/validation/Validator.md) recognizes the feature name but cannot set the requested value. |
| --- | --- |

**See Also**

- [#getFeature(String)](../javax/xml/validation/Validator.md)) 

### setProperty

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProperty(
    name: String!, 
    object: Any!
): Unit
```

Set the value of a property.

The property name is any fully-qualified URI. It is possible for a [Validator](../javax/xml/validation/Validator.md) to recognize a property name but to be unable to change the current value. Some property values may be immutable or mutable only in specific contexts, such as before, during, or after a validation.

[Validator](../javax/xml/validation/Validator.md) s are not required to recognize setting any specific property names.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property name, which is a non-null fully-qualified URI. |
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The requested value for the property. |

| Exceptions ||
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | When the name parameter is null. |
| `org.xml.sax.SAXNotRecognizedException` | If the property value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the [Validator](../javax/xml/validation/Validator.md) recognizes the property name but cannot set the requested value. |
| --- | --- |

### setResourceResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setResourceResolver(resourceResolver: LSResourceResolver!): Unit
```

Sets the [LSResourceResolver](../org/w3c/dom/ls/LSResourceResolver.md) to customize resource resolution while in a validation episode.

[Validator](../javax/xml/validation/Validator.md) uses a [LSResourceResolver](../org/w3c/dom/ls/LSResourceResolver.md) when it needs to locate external resources while a validation, although exactly what constitutes "locating external resources" is up to each schema language.

When the [LSResourceResolver](../org/w3c/dom/ls/LSResourceResolver.md) is null, the implementation will behave as if the following [LSResourceResolver](../org/w3c/dom/ls/LSResourceResolver.md) is set: 

```kotlin
class DumbLSResourceResolver implements <code><a docref="org.w3c.dom.ls.LSResourceResolver">LSResourceResolver</a></code>{
      public <code><a docref="org.w3c.dom.ls.LSInput">org.w3c.dom.ls.LSInput</a></code>resolveResource(
          String publicId, String systemId, String baseURI) {
 
          return null; // always return null
      }
  }
  
```

If a [LSResourceResolver](../org/w3c/dom/ls/LSResourceResolver.md) throws a [RuntimeException](../java/lang/RuntimeException.md)(or instances of its derived classes), then the [Validator](../javax/xml/validation/Validator.md) will abort the parsing and the caller of the`validate`method will receive the same [RuntimeException](../java/lang/RuntimeException.md).

When a new [Validator](../javax/xml/validation/Validator.md) object is created, initially this field is set to null.

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resourceResolver` | [LSResourceResolver](../org/w3c/dom/ls/LSResourceResolver.md)!:A new resource resolver to be set. This parameter can be null. |

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

- [#setErrorHandler(ErrorHandler)](../javax/xml/validation/Validator.md)) 

### validate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun validate(
    source: Source!, 
    result: Result!
): Unit
```

Validates the specified input and send the augmented validation result to the specified output.

This method places the following restrictions on the types of the [Source](../javax/xml/transform/Source.md)/ [Result](../javax/xml/transform/Result.md) accepted.

#### [Source](../javax/xml/transform/Source.md)/ [Result](../javax/xml/transform/Result.md) accepted:

| | [javax.xml.transform.sax.SAXSource](../javax/xml/transform/sax/SAXSource.md) | [javax.xml.transform.dom.DOMSource](../javax/xml/transform/dom/DOMSource.md) | [javax.xml.transform.stream.StreamSource](../javax/xml/transform/stream/StreamSource.md) |
| --- | --- | --- | --- |
| null | OK | OK | OK | OK |
| [javax.xml.transform.sax.SAXResult](../javax/xml/transform/sax/SAXResult.md) | OK | Err | Err | Err |
| [javax.xml.transform.dom.DOMResult](../javax/xml/transform/dom/DOMResult.md) | Err | OK | Err | Err |
| --- | --- | --- | --- | --- |
| [javax.xml.transform.stream.StreamResult](../javax/xml/transform/stream/StreamResult.md) | Err | Err | Err | OK |

To validate one [Source](../javax/xml/transform/Source.md) into another kind of [Result](../javax/xml/transform/Result.md), use the identity transformer (see [javax.xml.transform.TransformerFactory#newTransformer()](../javax/xml/transform/TransformerFactory.md))).

Errors found during the validation is sent to the specified [ErrorHandler](../org/xml/sax/ErrorHandler.md).

If a document is valid, or if a document contains some errors but none of them were fatal and the [ErrorHandler](../org/xml/sax/ErrorHandler.md) didn't throw any exception, then the method returns normally.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Source](../javax/xml/transform/Source.md)!:XML to be validated. Must not be null. |
| `result` | [Result](../javax/xml/transform/Result.md)!:The [Result](../javax/xml/transform/Result.md) object that receives (possibly augmented) XML. This parameter can be null if the caller is not interested in it. Note that when a [javax.xml.transform.dom.DOMResult](../javax/xml/transform/dom/DOMResult.md) is used, a validator might just pass the same DOM node from [javax.xml.transform.dom.DOMSource](../javax/xml/transform/dom/DOMSource.md) to [javax.xml.transform.dom.DOMResult](../javax/xml/transform/dom/DOMResult.md)(in which case source.getNode()==result.getNode()), it might copy the entire DOM tree, or it might alter the node given by the source. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the [Result](../javax/xml/transform/Result.md) type doesn't match the [Source](../javax/xml/transform/Source.md) type, or if the specified source is not a [javax.xml.transform.sax.SAXSource](../javax/xml/transform/sax/SAXSource.md), [javax.xml.transform.dom.DOMSource](../javax/xml/transform/dom/DOMSource.md) or [javax.xml.transform.stream.StreamSource](../javax/xml/transform/stream/StreamSource.md). |
| `org.xml.sax.SAXException` | If the [ErrorHandler](../org/xml/sax/ErrorHandler.md) throws a [SAXException](../org/xml/sax/SAXException.md) or if a fatal error is found and the [ErrorHandler](../org/xml/sax/ErrorHandler.md) returns normally. |
| `java.io.IOException` | If the validator is processing a [javax.xml.transform.sax.SAXSource](../javax/xml/transform/sax/SAXSource.md) and the underlying [org.xml.sax.XMLReader](../org/xml/sax/XMLReader.md) throws an [IOException](../java/io/IOException.md). |
| --- | --- |
| `java.lang.NullPointerException` | If the source parameter is null. |

**See Also**

- [#validate(Source)](../javax/xml/validation/Validator.md))
