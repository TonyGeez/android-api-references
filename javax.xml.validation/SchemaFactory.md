# SchemaFactory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SchemaFactory

```
abstract class SchemaFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.xml.validation.SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) |

Factory that creates [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema) objects. Entry-point to the validation API.

[SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) is a schema compiler. It reads external representations of schemas and prepares them for validation.

The [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) class is not thread-safe. In other words, it is the application's responsibility to ensure that at most one thread is using a [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) object at any given moment. Implementations are encouraged to mark methods as synchronized to protect themselves from broken clients.

[SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) is not re-entrant. While one of the`newSchema`methods is being invoked, applications may not attempt to recursively invoke the`newSchema`method, even from the same thread.

## Schema Language

This spec uses a namespace URI to designate a schema language. The following table shows the values defined by this specification.

To be compliant with the spec, the implementation is only required to support W3C XML Schema 1.0. However, if it chooses to support other schema languages listed here, it must conform to the relevant behaviors described in this spec.

Schema languages not listed here are expected to introduce their own URIs to represent themselves. The [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) class is capable of locating other implementations for other schema languages at run-time.

Note that because the XML DTD is strongly tied to the parsing process and has a significant effect on the parsing process, it is impossible to define the DTD validation as a process independent from parsing. For this reason, this specification does not define the semantics for the XML DTD. This doesn't prohibit implementers from implementing it in a way they see fit, but*users are warned that any DTD validation implemented on this interface necessarily deviate from the XML DTD semantics as defined in the XML 1.0*.

| value | language |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [javax.xml.XMLConstants#W3C_XML_SCHEMA_NS_URI](https://developer.android.com/reference/kotlin/javax/xml/XMLConstants.html#W3C_XML_SCHEMA_NS_URI:kotlin.String)("`http://www.w3.org/2001/XMLSchema`") | [W3C XML Schema 1.0](http://www.w3.org/TR/xmlschema-1) |
| [javax.xml.XMLConstants#RELAXNG_NS_URI](https://developer.android.com/reference/kotlin/javax/xml/XMLConstants.html#RELAXNG_NS_URI:kotlin.String)("`http://relaxng.org/ns/structure/1.0`") | [RELAX NG 1.0](http://www.relaxng.org/) |

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#SchemaFactory())`()` Constructor for derived classes. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)! | [getErrorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#getErrorHandler())`()` Gets the current [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) set to this [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#getFeature(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a feature flag. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getProperty](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#getProperty(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a property. |
| abstract [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#)! | [getResourceResolver](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#getResourceResolver())`()` Gets the current [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) set to this [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSchemaLanguageSupported](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#isSchemaLanguageSupported(kotlin.String))`(`schemaLanguage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Is specified schema supported by this`SchemaFactory`? |
| openstatic [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#)! | [newInstance](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#newInstance(kotlin.String))`(`schemaLanguage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Lookup an implementation of the`SchemaFactory`that supports the specified schema language and return it. |
| openstatic [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#)! | [newInstance](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#newInstance(kotlin.String,%20kotlin.String,%20java.lang.ClassLoader))`(`schemaLanguage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `factoryClassName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `classLoader:` ` [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!`)` Returns an instance of the named implementation of`SchemaFactory`. |
| abstract [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema)! | [newSchema](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#newSchema())`()` Creates a special [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema) object. |
| open [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema)! | [newSchema](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#newSchema(java.io.File))`(`schema:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Parses the specified`File`as a schema and returns it as a`Schema`. |
| open [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema)! | [newSchema](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#newSchema(java.net.URL))`(`schema:` ` [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)!`)` Parses the specified`URL`as a schema and returns it as a`Schema`. |
| open [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema)! | [newSchema](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#newSchema(javax.xml.transform.Source))`(`schema:` ` [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!`)` Parses the specified source as a schema and returns it as a schema. |
| abstract [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema)! | [newSchema](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#newSchema(kotlin.Array))`(`schemas:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!>!`)` Parses the specified source(s) as a schema and returns it as a schema. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#setErrorHandler(org.xml.sax.ErrorHandler))`(`errorHandler:` ` [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)!`)` Sets the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) to receive errors encountered during the`newSchema`method invocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#setFeature(kotlin.String,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the value of a feature flag. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#setProperty(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Set the value of a property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceResolver](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#setResourceResolver(org.w3c.dom.ls.LSResourceResolver))`(`resourceResolver:` ` [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#)!`)` Sets the [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) to customize resource resolution when parsing schemas. |

## Protected constructors

### SchemaFactory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SchemaFactory()
```

Constructor for derived classes.

The constructor does nothing.

Derived classes must create [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) objects that have`null` [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) and`null` [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#).

## Public methods

### getErrorHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getErrorHandler(): ErrorHandler!
```

Gets the current [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) set to this [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#).

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)! | This method returns the object that was last set through the [setErrorHandler(org.xml.sax.ErrorHandler)](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#setErrorHandler(org.xml.sax.ErrorHandler))method, or null if that method has never been called since this [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) has created. |

**See Also**

- [#setErrorHandler(ErrorHandler)](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#setErrorHandler(org.xml.sax.ErrorHandler)) 

### getFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFeature(name: String!): Boolean
```

Look up the value of a feature flag.

The feature name is any fully-qualified URI. It is possible for a [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) to recognize a feature name but temporarily be unable to return its value.

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
| `org.xml.sax.SAXNotSupportedException` | When the [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) recognizes the feature name but cannot determine its value at this time. |
| `java.lang.NullPointerException` | if the name parameter is null. |

**See Also**

- [#setFeature(String, boolean)](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#setFeature(kotlin.String,%20kotlin.Boolean)) 

### getProperty

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProperty(name: String!): Any!
```

Look up the value of a property.

The property name is any fully-qualified URI. It is possible for a [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) to recognize a property name but temporarily be unable to return its value.

[SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) s are not required to recognize any specific property names.

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

**See Also**

- [#setProperty(String, Object)](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#setProperty(kotlin.String,%20kotlin.Any)) 

### getResourceResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getResourceResolver(): LSResourceResolver!
```

Gets the current [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) set to this [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#).

| Return ||
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#)! | This method returns the object that was last set through the [setResourceResolver(org.w3c.dom.ls.LSResourceResolver)](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#setResourceResolver(org.w3c.dom.ls.LSResourceResolver))method, or null if that method has never been called since this [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) has created. |

**See Also**

- [#setErrorHandler(ErrorHandler)](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#setErrorHandler(org.xml.sax.ErrorHandler)) 

### isSchemaLanguageSupported

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSchemaLanguageSupported(schemaLanguage: String!): Boolean
```

Is specified schema supported by this`SchemaFactory`?

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `schemaLanguage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Specifies the schema language which the returned`SchemaFactory`will understand.`schemaLanguage`must specify a [valid](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#schemaLanguage) schema language. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`SchemaFactory`supports`schemaLanguage`, else`false`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If`schemaLanguage`is`null`. |
| `java.lang.IllegalArgumentException` | If`schemaLanguage.length() == 0`or`schemaLanguage`does not specify a [valid](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#schemaLanguage) schema language. |

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

If everything fails, [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) will be thrown.

**Tip for Trouble-shooting:**

See [java.util.Properties#load(java.io.InputStream)](https://developer.android.com/reference/kotlin/java/util/Properties.html#load(java.io.InputStream))for exactly how a property file is parsed. In particular, colons ':' need to be escaped in a property file, so make sure schema language URIs are properly escaped in it. For example: 

```kotlin
http\://www.w3.org/2001/XMLSchema=org.acme.foo.XSSchemaFactory
  
```

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `schemaLanguage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Specifies the schema language which the returned SchemaFactory will understand. See [the list of available schema languages](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#schemaLanguage) for the possible values. |

| Return ||
|------------------------------------------------------------------------------------------------------|----------------------------------|
| [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#)! | New instance of a`SchemaFactory` |

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

Creates a special [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema) object.

The exact semantics of the returned [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema) object depends on the schema language that this [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) is created for.

Also, implementations are allowed to use implementation-specific property/feature to alter the semantics of this method.

## W3C XML Schema 1.0

For XML Schema, this method creates a [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema) object that performs validation by using location hints specified in documents.

The returned [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema) object assumes that if documents refer to the same URL in the schema location hints, they will always resolve to the same schema document. This assumption allows implementations to reuse parsed results of schema documents so that multiple validations against the same schema will run faster.

Note that the use of schema location hints introduces a vulnerability to denial-of-service attacks.

## RELAX NG

RELAX NG does not support this operation.

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema)! | Always return non-null valid [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema) object. |

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

This is a convenience method for [newSchema(javax.xml.transform.Source)](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#newSchema(javax.xml.transform.Source)).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------|
| `schema` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:File that represents a schema. |

| Return ||
|---------------------------------------------------------------------------------------|----------------------------------|
| [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema)! | New`Schema`from parsing`schema`. |

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

This is a convenience method for [newSchema(javax.xml.transform.Source)](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#newSchema(javax.xml.transform.Source)).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `schema` | [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)!:`URL`that represents a schema. |

| Return ||
|---------------------------------------------------------------------------------------|----------------------------------|
| [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema)! | New`Schema`from parsing`schema`. |

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
| `schema` | [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!:Source that represents a schema. |

| Return ||
|---------------------------------------------------------------------------------------|----------------------------------|
| [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema)! | New`Schema`from parsing`schema`. |

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

The callee will read all the [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#) s and combine them into a single schema. The exact semantics of the combination depends on the schema language that this [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) object is created for.

When an [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) is set, the callee will report all the errors found in sources to the handler. If the handler throws an exception, it will abort the schema compilation and the same exception will be thrown from this method. Also, after an error is reported to a handler, the callee is allowed to abort the further processing by throwing it. If an error handler is not set, the callee will throw the first error it finds in the sources.

## W3C XML Schema 1.0

The resulting schema contains components from the specified sources. The same result would be achieved if all these sources were imported, using appropriate values for schemaLocation and namespace, into a single schema document with a different targetNamespace and no components of its own, if the import elements were given in the same order as the sources. Section 4.2.3 of the XML Schema recommendation describes the options processors have in this regard. While a processor should be consistent in its treatment of JAXP schema sources and XML Schema imports, the behavior between JAXP-compliant parsers may vary; in particular, parsers may choose to ignore all but the first \<import\> for a given namespace, regardless of information provided in schemaLocation.

If the parsed set of schemas includes error(s) as specified in the section 5.1 of the XML Schema spec, then the error must be reported to the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#).

## RELAX NG

For RELAX NG, this method must throw [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#) if schemas.length!=1.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `schemas` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!\>!:inputs to be parsed. [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) is required to recognize [StreamSource](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource.html#), [javax.xml.transform.sax.SAXSource](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource.html#), and [javax.xml.transform.dom.DOMSource](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMSource.html#). |

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema)! | Always return a non-null valid [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema) object. Note that when an error has been reported, there is no guarantee that the returned [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema) object is meaningful. |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | If an error is found during processing the specified inputs. When an [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) is set, errors are reported to there first. See [setErrorHandler(org.xml.sax.ErrorHandler)](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#setErrorHandler(org.xml.sax.ErrorHandler)). |
| `java.lang.NullPointerException` | If the`schemas`parameter itself is null or any item in the array is null. |
| `java.lang.IllegalArgumentException` | If any item in the array is not recognized by this method. |
| `java.lang.UnsupportedOperationException` | If the schema language doesn't support this operation. |

### setErrorHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setErrorHandler(errorHandler: ErrorHandler!): Unit
```

Sets the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) to receive errors encountered during the`newSchema`method invocation.

Error handler can be used to customize the error handling process during schema parsing. When an [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#) is set, errors found during the parsing of schemas will be first sent to the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#).

The error handler can abort the parsing of a schema immediately by throwing [SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException.html#) from the handler. Or for example it can print an error to the screen and try to continue the processing by returning normally from the [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)

If any [Throwable](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#)(or instances of its derived classes) is thrown from an [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#), the caller of the`newSchema`method will be thrown the same [Throwable](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#) object.

[SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) is not allowed to throw [SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException.html#) without first reporting it to [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#).

Applications can call this method even during a [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema) is being parsed.

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

When a new [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) object is created, initially this field is set to null. This field will*NOT* be inherited to [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema) s, [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator) s, or [ValidatorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler) s that are created from this [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#).

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

Feature can be used to control the way a [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) parses schemas, although [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) s are not required to recognize any specific feature names.

The feature name is any fully-qualified URI. It is possible for a [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) to expose a feature value but to be unable to change the current value.

All implementations are required to support the [javax.xml.XMLConstants#FEATURE_SECURE_PROCESSING](https://developer.android.com/reference/kotlin/javax/xml/XMLConstants.html#FEATURE_SECURE_PROCESSING:kotlin.String) feature. When the feature is:

- `true`: the implementation will limit XML processing to conform to implementation limits. Examples include entity expansion limits and XML Schema constructs that would consume large amounts of resources. If XML processing is limited for security reasons, it will be reported via a call to the registered [ErrorHandler.fatalError(org.xml.sax.SAXParseException)](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#fatalError(org.xml.sax.SAXParseException)). See [setErrorHandler(org.xml.sax.ErrorHandler)](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#setErrorHandler(org.xml.sax.ErrorHandler)).
- `false`: the implementation will processing XML according to the XML specifications without regard to possible implementation limits.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The feature name, which is a non-null fully-qualified URI. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The requested value of the feature (true or false). |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the feature value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) recognizes the feature name but cannot set the requested value. |
| `java.lang.NullPointerException` | if the name parameter is null. |

**See Also**

- [#getFeature(String)](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#getFeature(kotlin.String)) 

### setProperty

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProperty(
    name: String!, 
    object: Any!
): Unit
```

Set the value of a property.

The property name is any fully-qualified URI. It is possible for a [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) to recognize a property name but to be unable to change the current value.

[SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) s are not required to recognize setting any specific property names.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property name, which is a non-null fully-qualified URI. |
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The requested value for the property. |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXNotRecognizedException` | If the property value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) recognizes the property name but cannot set the requested value. |
| `java.lang.NullPointerException` | if the name parameter is null. |

### setResourceResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setResourceResolver(resourceResolver: LSResourceResolver!): Unit
```

Sets the [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) to customize resource resolution when parsing schemas.

[SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) uses a [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) when it needs to locate external resources while parsing schemas, although exactly what constitutes "locating external resources" is up to each schema language. For example, for W3C XML Schema, this includes files \<include\>d or \<import\>ed, and DTD referenced from schema files, etc.

Applications can call this method even during a [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema) is being parsed.

When the [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) is null, the implementation will behave as if the following [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) is set: 

```kotlin
class DumbDOMResourceResolver implements <code><a docref="org.w3c.dom.ls.LSResourceResolver">LSResourceResolver</a></code>{
      public <code><a docref="org.w3c.dom.ls.LSInput">org.w3c.dom.ls.LSInput</a></code>resolveResource(
          String publicId, String systemId, String baseURI) {
 
          return null; // always return null
      }
  }
  
```

If a [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#) throws a [RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#)(or instances of its derived classes), then the [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) will abort the parsing and the caller of the`newSchema`method will receive the same [RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#).

When a new [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#) object is created, initially this field is set to null. This field will*NOT* be inherited to [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema) s, [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator) s, or [ValidatorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler) s that are created from this [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory#).

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resourceResolver` | [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#)!:A new resource resolver to be set. This parameter can be null. |
