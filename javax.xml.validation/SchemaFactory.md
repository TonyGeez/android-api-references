# SchemaFactory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SchemaFactory

```
abstract class SchemaFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.validation.SchemaFactory](SchemaFactory.md) |

Factory that creates [Schema](Schema.md) objects. Entry-point to the validation API.

[SchemaFactory](SchemaFactory.md) is a schema compiler. It reads external representations of schemas and prepares them for validation.

The [SchemaFactory](SchemaFactory.md) class is not thread-safe. In other words, it is the application's responsibility to ensure that at most one thread is using a [SchemaFactory](SchemaFactory.md) object at any given moment. Implementations are encouraged to mark methods as synchronized to protect themselves from broken clients.

[SchemaFactory](SchemaFactory.md) is not re-entrant. While one of the`newSchema`methods is being invoked, applications may not attempt to recursively invoke the`newSchema`method, even from the same thread.

## Schema Language

This spec uses a namespace URI to designate a schema language. The following table shows the values defined by this specification.

To be compliant with the spec, the implementation is only required to support W3C XML Schema 1.0. However, if it chooses to support other schema languages listed here, it must conform to the relevant behaviors described in this spec.

Schema languages not listed here are expected to introduce their own URIs to represent themselves. The [SchemaFactory](SchemaFactory.md) class is capable of locating other implementations for other schema languages at run-time.

Note that because the XML DTD is strongly tied to the parsing process and has a significant effect on the parsing process, it is impossible to define the DTD validation as a process independent from parsing. For this reason, this specification does not define the semantics for the XML DTD. This doesn't prohibit implementers from implementing it in a way they see fit, but*users are warned that any DTD validation implemented on this interface necessarily deviate from the XML DTD semantics as defined in the XML 1.0*.

| value | language |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [javax.xml.XMLConstants#W3C_XML_SCHEMA_NS_URI](../javax.xml/XMLConstants.md)("`http://www.w3.org/2001/XMLSchema`") | [W3C XML Schema 1.0](http://www.w3.org/TR/xmlschema-1) |
| [javax.xml.XMLConstants#RELAXNG_NS_URI](../javax.xml/XMLConstants.md)("`http://relaxng.org/ns/structure/1.0`") | [RELAX NG 1.0](http://www.relaxng.org/) |

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SchemaFactory](SchemaFactory.md))`()` Constructor for derived classes. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ErrorHandler](../org.xml.sax/ErrorHandler.md)! | [getErrorHandler](SchemaFactory.md))`()` Gets the current [ErrorHandler](../org.xml.sax/ErrorHandler.md) set to this [SchemaFactory](SchemaFactory.md). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](SchemaFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a feature flag. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getProperty](SchemaFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a property. |
| --- | --- |
| abstract [LSResourceResolver](../org.w3c.dom.ls/LSResourceResolver.md)! | [getResourceResolver](SchemaFactory.md))`()` Gets the current [LSResourceResolver](../org.w3c.dom.ls/LSResourceResolver.md) set to this [SchemaFactory](SchemaFactory.md). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSchemaLanguageSupported](SchemaFactory.md))`(`schemaLanguage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Is specified schema supported by this`SchemaFactory`? |
| openstatic [SchemaFactory](SchemaFactory.md)! | [newInstance](SchemaFactory.md))`(`schemaLanguage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Lookup an implementation of the`SchemaFactory`that supports the specified schema language and return it. |
| --- | --- |
| openstatic [SchemaFactory](SchemaFactory.md)! | [newInstance](SchemaFactory.md))`(`schemaLanguage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `factoryClassName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `classLoader:` ` [ClassLoader](../java.lang/ClassLoader.md)!`)` Returns an instance of the named implementation of`SchemaFactory`. |
| abstract [Schema](Schema.md)! | [newSchema](SchemaFactory.md))`()` Creates a special [Schema](Schema.md) object. |
| open [Schema](Schema.md)! | [newSchema](SchemaFactory.md))`(`schema:` ` [File](../java.io/File.md)!`)` Parses the specified`File`as a schema and returns it as a`Schema`. |
| --- | --- |
| open [Schema](Schema.md)! | [newSchema](SchemaFactory.md))`(`schema:` ` [URL](../java.net/URL.md)!`)` Parses the specified`URL`as a schema and returns it as a`Schema`. |
| open [Schema](Schema.md)! | [newSchema](SchemaFactory.md))`(`schema:` ` [Source](../javax.xml.transform/Source.md)!`)` Parses the specified source as a schema and returns it as a schema. |
| abstract [Schema](Schema.md)! | [newSchema](SchemaFactory.md))`(`schemas:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Source](../javax.xml.transform/Source.md)!>!`)` Parses the specified source(s) as a schema and returns it as a schema. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](SchemaFactory.md))`(`errorHandler:` ` [ErrorHandler](../org.xml.sax/ErrorHandler.md)!`)` Sets the [ErrorHandler](../org.xml.sax/ErrorHandler.md) to receive errors encountered during the`newSchema`method invocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](SchemaFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the value of a feature flag. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](SchemaFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Set the value of a property. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceResolver](SchemaFactory.md))`(`resourceResolver:` ` [LSResourceResolver](../org.w3c.dom.ls/LSResourceResolver.md)!`)` Sets the [LSResourceResolver](../org.w3c.dom.ls/LSResourceResolver.md) to customize resource resolution when parsing schemas. |

## Protected constructors

### SchemaFactory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SchemaFactory()
```

Constructor for derived classes.

The constructor does nothing.

Derived classes must create [SchemaFactory](SchemaFactory.md) objects that have`null` [ErrorHandler](../org.xml.sax/ErrorHandler.md) and`null` [LSResourceResolver](../org.w3c.dom.ls/LSResourceResolver.md).

## Public methods

### getErrorHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getErrorHandler(): ErrorHandler!
```

Gets the current [ErrorHandler](../org.xml.sax/ErrorHandler.md) set to this [SchemaFactory](SchemaFactory.md).

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ErrorHandler](../org.xml.sax/ErrorHandler.md)! | This method returns the object that was last set through the [setErrorHandler(org.xml.sax.ErrorHandler)](SchemaFactory.md))method, or null if that method has never been called since this [SchemaFactory](SchemaFactory.md) has created. |

**See Also**

- [#setErrorHandler(ErrorHandler)](SchemaFactory.md)) 

### getFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFeature(name: String!): Boolean
```

Look up the value of a feature flag.

The feature name is any fully-qualified URI. It is possible for a [SchemaFactory](SchemaFactory.md) to recognize a feature name but temporarily be unable to return its value.

Implementers are free (and encouraged) to invent their own features, using names built on their own URIs.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The feature name, which is a non-null fully-qualified URI. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The current value of the feature (true or false). |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the feature value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the [SchemaFactory](SchemaFactory.md) recognizes the feature name but cannot determine its value at this time. |
| `java.lang.NullPointerException` | if the name parameter is null. |
| --- | --- |

**See Also**

- [#setFeature(String, boolean)](SchemaFactory.md)) 

### getProperty

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProperty(name: String!): Any!
```

Look up the value of a property.

The property name is any fully-qualified URI. It is possible for a [SchemaFactory](SchemaFactory.md) to recognize a property name but temporarily be unable to return its value.

[SchemaFactory](SchemaFactory.md) s are not required to recognize any specific property names.

Implementers are free (and encouraged) to invent their own properties, using names built on their own URIs.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property name, which is a non-null fully-qualified URI. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The current value of the property. |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the property value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the XMLReader recognizes the property name but cannot determine its value at this time. |
| `java.lang.NullPointerException` | if the name parameter is null. |
| --- | --- |

**See Also**

- [#setProperty(String, Object)](SchemaFactory.md)) 

### getResourceResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getResourceResolver(): LSResourceResolver!
```

Gets the current [LSResourceResolver](../org.w3c.dom.ls/LSResourceResolver.md) set to this [SchemaFactory](SchemaFactory.md).

| Return ||
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LSResourceResolver](../org.w3c.dom.ls/LSResourceResolver.md)! | This method returns the object that was last set through the [setResourceResolver(org.w3c.dom.ls.LSResourceResolver)](SchemaFactory.md))method, or null if that method has never been called since this [SchemaFactory](SchemaFactory.md) has created. |

**See Also**

- [#setErrorHandler(ErrorHandler)](SchemaFactory.md)) 

### isSchemaLanguageSupported

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSchemaLanguageSupported(schemaLanguage: String!): Boolean
```

Is specified schema supported by this`SchemaFactory`?

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `schemaLanguage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Specifies the schema language which the returned`SchemaFactory`will understand.`schemaLanguage`must specify a [valid](SchemaFactory.md) schema language. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`SchemaFactory`supports`schemaLanguage`, else`false`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If`schemaLanguage`is`null`. |
| `java.lang.IllegalArgumentException` | If`schemaLanguage.length() == 0`or`schemaLanguage`does not specify a [valid](SchemaFactory.md) schema language. |

### newInstance

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(schemaLanguage: String!): SchemaFactory!
```

Lookup an implementation of the`SchemaFactory`that supports the specified schema language and return it.

To find a`SchemaFactory`object for a given schema language, this method looks the following places in the following order where "the class loader" refers to the context class loader:

1. If the system property`"javax.xml.validation.SchemaFactory:`*schemaLanguage*`"`is present (where*schemaLanguage*is the parameter to this method), then its value is read as a class name. The method will try to create a new instance of this class by using the class loader, and returns it if it is successfully created.
2. `$java.home/lib/jaxp.properties`is read and the value associated with the key being the system property above is looked for. If present, the value is processed just like above.
3. The class loader is asked for service provider provider-configuration files matching`javax.xml.validation.SchemaFactory`in the resource directory META-INF/services. See the JAR File Specification for file format and parsing rules. Each potential service provider is required to implement the method:

   ```kotlin
   <code><a docref="javax.xml.validation.SchemaFactory$isSchemaLanguageSupported(kotlin.String)">#isSchemaLanguageSupported(java.lang.String)</a></code>
   ```
 The first service provider found in class loader order that supports the specified schema language is returned.
4. Platform default`SchemaFactory`is located in a implementation specific way. There must be a platform default`SchemaFactory`for W3C XML Schema.

If everything fails, [IllegalArgumentException](../java.lang/IllegalArgumentException.md) will be thrown.

**Tip for Trouble-shooting:**

See [java.util.Properties#load(java.io.InputStream)](../java.util/Properties.md))for exactly how a property file is parsed. In particular, colons ':' need to be escaped in a property file, so make sure schema language URIs are properly escaped in it. For example: 

```kotlin
http\://www.w3.org/2001/XMLSchema=org.acme.foo.XSSchemaFactory
  
```

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `schemaLanguage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Specifies the schema language which the returned SchemaFactory will understand. See [the list of available schema languages](SchemaFactory.md) for the possible values. |

| Return ||
|------------------------------------------------------------------------------------------------------|----------------------------------|
| [SchemaFactory](SchemaFactory.md)! | New instance of a`SchemaFactory` |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If no implementation of the schema language is available. |
| `java.lang.NullPointerException` | If the schemaLanguage parameter is null. |

### newInstance

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(
    schemaLanguage: String!, 
    factoryClassName: String!, 
    classLoader: ClassLoader!
): SchemaFactory!
```

Returns an instance of the named implementation of`SchemaFactory`.

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`factoryClassName`is not available, cannot be instantiated, or doesn't support`schemaLanguage`. |

### newSchema

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newSchema(): Schema!
```

Creates a special [Schema](Schema.md) object.

The exact semantics of the returned [Schema](Schema.md) object depends on the schema language that this [SchemaFactory](SchemaFactory.md) is created for.

Also, implementations are allowed to use implementation-specific property/feature to alter the semantics of this method.

## W3C XML Schema 1.0

For XML Schema, this method creates a [Schema](Schema.md) object that performs validation by using location hints specified in documents.

The returned [Schema](Schema.md) object assumes that if documents refer to the same URL in the schema location hints, they will always resolve to the same schema document. This assumption allows implementations to reuse parsed results of schema documents so that multiple validations against the same schema will run faster.

Note that the use of schema location hints introduces a vulnerability to denial-of-service attacks.

## RELAX NG

RELAX NG does not support this operation.

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Schema](Schema.md)! | Always return non-null valid [Schema](Schema.md) object. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If this operation is not supported by the callee. |
| `org.xml.sax.SAXException` | If this operation is supported but failed for some reason. |

### newSchema

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newSchema(schema: File!): Schema!
```

Parses the specified`File`as a schema and returns it as a`Schema`.

This is a convenience method for [newSchema(javax.xml.transform.Source)](SchemaFactory.md)).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------|
| `schema` | [File](../java.io/File.md)!:File that represents a schema. |

| Return ||
|---------------------------------------------------------------------------------------|----------------------------------|
| [Schema](Schema.md)! | New`Schema`from parsing`schema`. |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `org.xml.sax.SAXException` | If a SAX error occurs during parsing. |
| `java.lang.NullPointerException` | if schema is null. |

### newSchema

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newSchema(schema: URL!): Schema!
```

Parses the specified`URL`as a schema and returns it as a`Schema`.

This is a convenience method for [newSchema(javax.xml.transform.Source)](SchemaFactory.md)).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `schema` | [URL](../java.net/URL.md)!:`URL`that represents a schema. |

| Return ||
|---------------------------------------------------------------------------------------|----------------------------------|
| [Schema](Schema.md)! | New`Schema`from parsing`schema`. |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `org.xml.sax.SAXException` | If a SAX error occurs during parsing. |
| `java.lang.NullPointerException` | if schema is null. |

### newSchema

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newSchema(schema: Source!): Schema!
```

Parses the specified source as a schema and returns it as a schema.

This is a convenience method for[newSchema(javax.xml.transform.Source[])](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#newSchema(kotlin.Array)).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------|
| `schema` | [Source](../javax.xml.transform/Source.md)!:Source that represents a schema. |

| Return ||
|---------------------------------------------------------------------------------------|----------------------------------|
| [Schema](Schema.md)! | New`Schema`from parsing`schema`. |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `org.xml.sax.SAXException` | If a SAX error occurs during parsing. |
| `java.lang.NullPointerException` | if schema is null. |

### newSchema

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newSchema(schemas: Array<Source!>!): Schema!
```

Parses the specified source(s) as a schema and returns it as a schema.

The callee will read all the [Source](../javax.xml.transform/Source.md) s and combine them into a single schema. The exact semantics of the combination depends on the schema language that this [SchemaFactory](SchemaFactory.md) object is created for.

When an [ErrorHandler](../org.xml.sax/ErrorHandler.md) is set, the callee will report all the errors found in sources to the handler. If the handler throws an exception, it will abort the schema compilation and the same exception will be thrown from this method. Also, after an error is reported to a handler, the callee is allowed to abort the further processing by throwing it. If an error handler is not set, the callee will throw the first error it finds in the sources.

## W3C XML Schema 1.0

The resulting schema contains components from the specified sources. The same result would be achieved if all these sources were imported, using appropriate values for schemaLocation and namespace, into a single schema document with a different targetNamespace and no components of its own, if the import elements were given in the same order as the sources. Section 4.2.3 of the XML Schema recommendation describes the options processors have in this regard. While a processor should be consistent in its treatment of JAXP schema sources and XML Schema imports, the behavior between JAXP-compliant parsers may vary; in particular, parsers may choose to ignore all but the first \<import\> for a given namespace, regardless of information provided in schemaLocation.

If the parsed set of schemas includes error(s) as specified in the section 5.1 of the XML Schema spec, then the error must be reported to the [ErrorHandler](../org.xml.sax/ErrorHandler.md).

## RELAX NG

For RELAX NG, this method must throw [UnsupportedOperationException](../java.lang/UnsupportedOperationException.md) if schemas.length!=1.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `schemas` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Source](../javax.xml.transform/Source.md)!\>!:inputs to be parsed. [SchemaFactory](SchemaFactory.md) is required to recognize [StreamSource](../javax.xml.transform.stream/StreamSource.md), [javax.xml.transform.sax.SAXSource](../javax.xml.transform.sax/SAXSource.md), and [javax.xml.transform.dom.DOMSource](../javax.xml.transform.dom/DOMSource.md). |

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Schema](Schema.md)! | Always return a non-null valid [Schema](Schema.md) object. Note that when an error has been reported, there is no guarantee that the returned [Schema](Schema.md) object is meaningful. |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | If an error is found during processing the specified inputs. When an [ErrorHandler](../org.xml.sax/ErrorHandler.md) is set, errors are reported to there first. See [setErrorHandler(org.xml.sax.ErrorHandler)](SchemaFactory.md)). |
| `java.lang.NullPointerException` | If the`schemas`parameter itself is null or any item in the array is null. |
| `java.lang.IllegalArgumentException` | If any item in the array is not recognized by this method. |
| --- | --- |
| `java.lang.UnsupportedOperationException` | If the schema language doesn't support this operation. |

### setErrorHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setErrorHandler(errorHandler: ErrorHandler!): Unit
```

Sets the [ErrorHandler](../org.xml.sax/ErrorHandler.md) to receive errors encountered during the`newSchema`method invocation.

Error handler can be used to customize the error handling process during schema parsing. When an [ErrorHandler](../org.xml.sax/ErrorHandler.md) is set, errors found during the parsing of schemas will be first sent to the [ErrorHandler](../org.xml.sax/ErrorHandler.md).

The error handler can abort the parsing of a schema immediately by throwing [SAXException](../org.xml.sax/SAXException.md) from the handler. Or for example it can print an error to the screen and try to continue the processing by returning normally from the [ErrorHandler](../org.xml.sax/ErrorHandler.md)

If any [Throwable](../java.lang/Throwable.md)(or instances of its derived classes) is thrown from an [ErrorHandler](../org.xml.sax/ErrorHandler.md), the caller of the`newSchema`method will be thrown the same [Throwable](../java.lang/Throwable.md) object.

[SchemaFactory](SchemaFactory.md) is not allowed to throw [SAXException](../org.xml.sax/SAXException.md) without first reporting it to [ErrorHandler](../org.xml.sax/ErrorHandler.md).

Applications can call this method even during a [Schema](Schema.md) is being parsed.

When the [ErrorHandler](../org.xml.sax/ErrorHandler.md) is null, the implementation will behave as if the following [ErrorHandler](../org.xml.sax/ErrorHandler.md) is set: 

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

When a new [SchemaFactory](SchemaFactory.md) object is created, initially this field is set to null. This field will*NOT* be inherited to [Schema](Schema.md) s, [Validator](Validator.md) s, or [ValidatorHandler](ValidatorHandler.md) s that are created from this [SchemaFactory](SchemaFactory.md).

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorHandler` | [ErrorHandler](../org.xml.sax/ErrorHandler.md)!:A new error handler to be set. This parameter can be null. |

### setFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFeature(
    name: String!, 
    value: Boolean
): Unit
```

Set the value of a feature flag.

Feature can be used to control the way a [SchemaFactory](SchemaFactory.md) parses schemas, although [SchemaFactory](SchemaFactory.md) s are not required to recognize any specific feature names.

The feature name is any fully-qualified URI. It is possible for a [SchemaFactory](SchemaFactory.md) to expose a feature value but to be unable to change the current value.

All implementations are required to support the [javax.xml.XMLConstants#FEATURE_SECURE_PROCESSING](../javax.xml/XMLConstants.md) feature. When the feature is:

- `true`: the implementation will limit XML processing to conform to implementation limits. Examples include entity expansion limits and XML Schema constructs that would consume large amounts of resources. If XML processing is limited for security reasons, it will be reported via a call to the registered [ErrorHandler.fatalError(org.xml.sax.SAXParseException)](../org.xml.sax/ErrorHandler.md)). See [setErrorHandler(org.xml.sax.ErrorHandler)](SchemaFactory.md)).
- `false`: the implementation will processing XML according to the XML specifications without regard to possible implementation limits.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The feature name, which is a non-null fully-qualified URI. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The requested value of the feature (true or false). |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the feature value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the [SchemaFactory](SchemaFactory.md) recognizes the feature name but cannot set the requested value. |
| `java.lang.NullPointerException` | if the name parameter is null. |
| --- | --- |

**See Also**

- [#getFeature(String)](SchemaFactory.md)) 

### setProperty

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProperty(
    name: String!, 
    object: Any!
): Unit
```

Set the value of a property.

The property name is any fully-qualified URI. It is possible for a [SchemaFactory](SchemaFactory.md) to recognize a property name but to be unable to change the current value.

[SchemaFactory](SchemaFactory.md) s are not required to recognize setting any specific property names.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property name, which is a non-null fully-qualified URI. |
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The requested value for the property. |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the property value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the [SchemaFactory](SchemaFactory.md) recognizes the property name but cannot set the requested value. |
| `java.lang.NullPointerException` | if the name parameter is null. |
| --- | --- |

### setResourceResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setResourceResolver(resourceResolver: LSResourceResolver!): Unit
```

Sets the [LSResourceResolver](../org.w3c.dom.ls/LSResourceResolver.md) to customize resource resolution when parsing schemas.

[SchemaFactory](SchemaFactory.md) uses a [LSResourceResolver](../org.w3c.dom.ls/LSResourceResolver.md) when it needs to locate external resources while parsing schemas, although exactly what constitutes "locating external resources" is up to each schema language. For example, for W3C XML Schema, this includes files \<include\>d or \<import\>ed, and DTD referenced from schema files, etc.

Applications can call this method even during a [Schema](Schema.md) is being parsed.

When the [LSResourceResolver](../org.w3c.dom.ls/LSResourceResolver.md) is null, the implementation will behave as if the following [LSResourceResolver](../org.w3c.dom.ls/LSResourceResolver.md) is set: 

```kotlin
class DumbDOMResourceResolver implements <code><a docref="org.w3c.dom.ls.LSResourceResolver">LSResourceResolver</a></code>{
      public <code><a docref="org.w3c.dom.ls.LSInput">org.w3c.dom.ls.LSInput</a></code>resolveResource(
          String publicId, String systemId, String baseURI) {
 
          return null; // always return null
      }
  }
  
```

If a [LSResourceResolver](../org.w3c.dom.ls/LSResourceResolver.md) throws a [RuntimeException](../java.lang/RuntimeException.md)(or instances of its derived classes), then the [SchemaFactory](SchemaFactory.md) will abort the parsing and the caller of the`newSchema`method will receive the same [RuntimeException](../java.lang/RuntimeException.md).

When a new [SchemaFactory](SchemaFactory.md) object is created, initially this field is set to null. This field will*NOT* be inherited to [Schema](Schema.md) s, [Validator](Validator.md) s, or [ValidatorHandler](ValidatorHandler.md) s that are created from this [SchemaFactory](SchemaFactory.md).

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resourceResolver` | [LSResourceResolver](../org.w3c.dom.ls/LSResourceResolver.md)!:A new resource resolver to be set. This parameter can be null. |
