Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SAXParserFactory

```
abstract class SAXParserFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.parsers.SAXParserFactory](../javax/xml/parsers/SAXParserFactory.md) |

Defines a factory API that enables applications to configure and obtain a SAX based parser to parse XML documents.

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#SAXParserFactory()()` Protected constructor to force use of `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#newInstance()`. |

| Public methods ||
|---|---|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#getFeature(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the particular property requested for in the underlying implementation of org. |
| open [Schema](../javax/xml/validation/Schema.md)! | `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#getSchema()()` Gets the `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` object specified through the `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#setSchema(javax.xml.validation.Schema)` method. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#isNamespaceAware()()` Indicates whether or not the factory is configured to produce parsers which are namespace aware. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#isValidating()()` Indicates whether or not the factory is configured to produce parsers which validate the XML content during parse. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#isXIncludeAware()()` Get state of XInclude processing. |
| open static [SAXParserFactory](../javax/xml/parsers/SAXParserFactory.md)! | `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#newInstance()()` Returns Android's implementation of `SAXParserFactory`. |
| --- | --- |
| open static [SAXParserFactory](../javax/xml/parsers/SAXParserFactory.md)! | `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#newInstance(kotlin.String,%20java.lang.ClassLoader)(factoryClassName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, classLoader: https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!)` Returns an instance of the named implementation of `SAXParserFactory`. |
| abstract [SAXParser](../javax/xml/parsers/SAXParser.md)! | `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#newSAXParser()()` Creates a new instance of a SAXParser using the currently configured factory parameters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#setFeature(kotlin.String,%20kotlin.Boolean)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the particular feature in the underlying implementation of org. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#setNamespaceAware(kotlin.Boolean)(awareness: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Specifies that the parser produced by this code will provide support for XML namespaces. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#setSchema(javax.xml.validation.Schema)(schema: https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#!)` Set the `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` to be used by parsers created from this factory. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#setValidating(kotlin.Boolean)(validating: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Specifies that the parser produced by this code will validate documents as they are parsed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#setXIncludeAware(kotlin.Boolean)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set state of XInclude processing. |

## Protected constructors

### SAXParserFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected SAXParserFactory()
```

Protected constructor to force use of `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#newInstance()`.

## Public methods

### getFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getFeature(name: String!): Boolean
```

Returns the particular property requested for in the underlying implementation of org.xml.sax.XMLReader.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the property to be retrieved. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Value of the requested property. |

| Exceptions ||
|---|---|
| `javax.xml.parsers.ParserConfigurationException` | if a parser cannot be created which satisfies the requested configuration. |
| `org.xml.sax.SAXNotRecognizedException` | When the underlying XMLReader does not recognize the property name. |
| `org.xml.sax.SAXNotSupportedException` | When the underlying XMLReader recognizes the property name but doesn't support the property. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#getProperty(kotlin.String)`

### getSchema

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSchema(): Schema!
```

Gets the `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` object specified through the `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#setSchema(javax.xml.validation.Schema)` method.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#!` | the `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` object that was last set through the `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#setSchema(javax.xml.validation.Schema)` method, or null if the method was not invoked since a `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#` is created. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | For backward compatibility, when implementations for earlier versions of JAXP is used, this exception will be thrown. |

### isNamespaceAware

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isNamespaceAware(): Boolean
```

Indicates whether or not the factory is configured to produce parsers which are namespace aware.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the factory is configured to produce parsers which are namespace aware; false otherwise. |

### isValidating

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isValidating(): Boolean
```

Indicates whether or not the factory is configured to produce parsers which validate the XML content during parse.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the factory is configured to produce parsers which validate the XML content during parse; false otherwise. |

### isXIncludeAware

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isXIncludeAware(): Boolean
```

Get state of XInclude processing.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | current state of XInclude processing |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | For backward compatibility, when implementations for earlier versions of JAXP is used, this exception will be thrown. |

### newInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newInstance(): SAXParserFactory!
```

Returns Android's implementation of `SAXParserFactory`. Unlike other Java implementations, this method does not consult system properties, property files, or the services API.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#!` | a new SAXParserFactory. |

| Exceptions ||
|---|---|
| `javax.xml.parsers.FactoryConfigurationError` | never. Included for API compatibility with other Java implementations. |

### newInstance

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newInstance(
    factoryClassName: String!, 
    classLoader: ClassLoader!
): SAXParserFactory!
```

Returns an instance of the named implementation of `SAXParserFactory`.

| Exceptions ||
|---|---|
| `javax.xml.parsers.FactoryConfigurationError` | if `factoryClassName` is not available or cannot be instantiated. |

### newSAXParser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun newSAXParser(): SAXParser!
```

Creates a new instance of a SAXParser using the currently configured factory parameters.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser!` | A new instance of a SAXParser. |

| Exceptions ||
|---|---|
| `javax.xml.parsers.ParserConfigurationException` | if a parser cannot be created which satisfies the requested configuration. |
| `org.xml.sax.SAXException` | for SAX errors. |

### setFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setFeature(
    name: String!, 
    value: Boolean
): Unit
```

Sets the particular feature in the underlying implementation of org.xml.sax.XMLReader. A list of the core features and properties can be found at <http://www.saxproject.org/>

All implementations are required to support the `https://developer.android.com/reference/kotlin/javax/xml/XMLConstants.html#FEATURE_SECURE_PROCESSING:kotlin.String` feature. When the feature is

- `true`: the implementation will limit XML processing to conform to implementation limits. Examples include entity expansion limits and XML Schema constructs that would consume large amounts of resources. If XML processing is limited for security reasons, it will be reported via a call to the registered `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#fatalError(org.xml.sax.SAXParseException)`. See `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser` `parse` methods for handler specification.
- When the feature is `false`, the implementation will processing XML according to the XML specifications without regard to possible implementation limits.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the feature to be set. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The value of the feature to be set. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If the `name` parameter is null. |
| `javax.xml.parsers.ParserConfigurationException` | if a parser cannot be created which satisfies the requested configuration. |
| `org.xml.sax.SAXNotRecognizedException` | When the underlying XMLReader does not recognize the property name. |
| --- | --- |
| `org.xml.sax.SAXNotSupportedException` | When the underlying XMLReader recognizes the property name but doesn't support the property. |

**See Also**

- `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#setFeature(kotlin.String,%20kotlin.Boolean)`

### setNamespaceAware

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNamespaceAware(awareness: Boolean): Unit
```

Specifies that the parser produced by this code will provide support for XML namespaces. By default the value of this is set to `false`.

| Parameters ||
|---|---|
| `awareness` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the parser produced by this code will provide support for XML namespaces; false otherwise. |

### setSchema

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSchema(schema: Schema!): Unit
```

Set the `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` to be used by parsers created from this factory.

When a `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` is non-null, a parser will use a validator created from it to validate documents before it passes information down to the application.

When warnings/errors/fatal errors are found by the validator, the parser must handle them as if those errors were found by the parser itself. In other words, if the user-specified `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#` is set, it must receive those errors, and if not, they must be treated according to the implementation specific default error handling rules.

A validator may modify the SAX event stream (for example by adding default values that were missing in documents), and a parser is responsible to make sure that the application will receive those modified event stream.

Initially, `null` is set as the `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#`.

This processing will take effect even if the `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#isValidating()` method returns `false`.

It is an error to use the `http://java.sun.com/xml/jaxp/properties/schemaSource` property and/or the `http://java.sun.com/xml/jaxp/properties/schemaLanguage` property in conjunction with a non-null `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` object. Such configuration will cause a `https://developer.android.com/reference/kotlin/org/xml/sax/SAXException.html#` exception when those properties are set on a `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParser`.

#### Note for implementors

A parser must be able to work with any `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` implementation. However, parsers and schemas are allowed to use implementation-specific custom mechanisms as long as they yield the result described in the specification.

| Parameters ||
|---|---|
| `schema` | [Schema](../javax/xml/validation/Schema.md)!: `Schema` to use, `null` to remove a schema. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | For backward compatibility, when implementations for earlier versions of JAXP is used, this exception will be thrown. |

### setValidating

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setValidating(validating: Boolean): Unit
```

Specifies that the parser produced by this code will validate documents as they are parsed. By default the value of this is set to `false`.

Note that "the validation" here means [a validating parser](http://www.w3.org/TR/REC-xml#proc-types) as defined in the XML recommendation. In other words, it essentially just controls the DTD validation. (except the legacy two properties defined in JAXP 1.2. See [here](../javax/xml/parsers/SAXParserFactory.md) for more details.)

To use modern schema languages such as W3C XML Schema or RELAX NG instead of DTD, you can configure your parser to be a non-validating parser by leaving the `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#setValidating(kotlin.Boolean)` method false, then use the `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory#setSchema(javax.xml.validation.Schema)` method to associate a schema to a parser.

| Parameters ||
|---|---|
| `validating` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the parser produced by this code will validate documents as they are parsed; false otherwise. |

### setXIncludeAware

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setXIncludeAware(state: Boolean): Unit
```

Set state of XInclude processing.

If XInclude markup is found in the document instance, should it be processed as specified in [XML Inclusions (XInclude) Version 1.0](http://www.w3.org/TR/xinclude/).

XInclude processing defaults to `false`.

| Parameters ||
|---|---|
| `state` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set XInclude processing to `true` or `false` |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | For backward compatibility, when implementations for earlier versions of JAXP is used, this exception will be thrown. |
