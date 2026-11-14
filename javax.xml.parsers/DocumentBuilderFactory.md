Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DocumentBuilderFactory

```
abstract class DocumentBuilderFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.parsers.DocumentBuilderFactory](../javax/xml/parsers/DocumentBuilderFactory.md) |

Defines a factory API that enables applications to obtain a parser that produces DOM object trees from XML documents.

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#DocumentBuilderFactory()()` <br /> |

| Public methods ||
|---|---|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#getAttribute(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Allows the user to retrieve specific attributes on the underlying implementation. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#getFeature(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Get the state of the named feature. |
| open [Schema](../javax/xml/validation/Schema.md)! | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#getSchema()()` Gets the `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` object specified through the `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setSchema(javax.xml.validation.Schema)` method. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#isCoalescing()()` Indicates whether or not the factory is configured to produce parsers which converts CDATA nodes to Text nodes and appends it to the adjacent (if any) Text node. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#isExpandEntityReferences()()` Indicates whether or not the factory is configured to produce parsers which expand entity reference nodes. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#isIgnoringComments()()` Indicates whether or not the factory is configured to produce parsers which ignores comments. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#isIgnoringElementContentWhitespace()()` Indicates whether or not the factory is configured to produce parsers which ignore ignorable whitespace in element content. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#isNamespaceAware()()` Indicates whether or not the factory is configured to produce parsers which are namespace aware. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#isValidating()()` Indicates whether or not the factory is configured to produce parsers which validate the XML content during parse. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#isXIncludeAware()()` Get state of XInclude processing. |
| open static [DocumentBuilderFactory](../javax/xml/parsers/DocumentBuilderFactory.md)! | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#newDefaultInstance()()` Creates a new instance of the `DocumentBuilderFactory` builtin system-default implementation. |
| open static [DocumentBuilderFactory](../javax/xml/parsers/DocumentBuilderFactory.md)! | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#newDefaultNSInstance()()` Creates a new NamespaceAware instance of the `DocumentBuilderFactory` builtin system-default implementation. |
| --- | --- |
| abstract [DocumentBuilder](../javax/xml/parsers/DocumentBuilder.md)! | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#newDocumentBuilder()()` Creates a new instance of a `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder` using the currently configured parameters. |
| open static [DocumentBuilderFactory](../javax/xml/parsers/DocumentBuilderFactory.md)! | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#newInstance()()` Returns Android's implementation of `DocumentBuilderFactory`. |
| open static [DocumentBuilderFactory](../javax/xml/parsers/DocumentBuilderFactory.md)! | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#newInstance(kotlin.String,%20java.lang.ClassLoader)(factoryClassName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, classLoader: https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!)` Returns an instance of the named implementation of `DocumentBuilderFactory`. |
| --- | --- |
| open static [DocumentBuilderFactory](../javax/xml/parsers/DocumentBuilderFactory.md)! | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#newNSInstance()()` Creates a new NamespaceAware, Android-specific instance of a `DocumentBuilderFactory`. |
| open static [DocumentBuilderFactory](../javax/xml/parsers/DocumentBuilderFactory.md)! | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#newNSInstance(kotlin.String,%20java.lang.ClassLoader)(factoryClassName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, classLoader: https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!)` Creates a new NamespaceAware instance of a `DocumentBuilderFactory` from the class name. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setAttribute(kotlin.String,%20kotlin.Any)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Allows the user to set specific attributes on the underlying implementation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setCoalescing(kotlin.Boolean)(coalescing: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Specifies that the parser produced by this code will convert CDATA nodes to Text nodes and append it to the adjacent (if any) text node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setExpandEntityReferences(kotlin.Boolean)(expandEntityRef: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Specifies that the parser produced by this code will expand entity reference nodes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setFeature(kotlin.String,%20kotlin.Boolean)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set a feature for this `DocumentBuilderFactory` and `DocumentBuilder`s created by this factory. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setIgnoringComments(kotlin.Boolean)(ignoreComments: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Specifies that the parser produced by this code will ignore comments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setIgnoringElementContentWhitespace(kotlin.Boolean)(whitespace: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Specifies that the parsers created by this factory must eliminate whitespace in element content (sometimes known loosely as 'ignorable whitespace') when parsing XML documents (see XML Rec 2.10). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setNamespaceAware(kotlin.Boolean)(awareness: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Specifies that the parser produced by this code will provide support for XML namespaces. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setSchema(javax.xml.validation.Schema)(schema: https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#!)` Set the `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` to be used by parsers created from this factory. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setValidating(kotlin.Boolean)(validating: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Specifies that the parser produced by this code will validate documents as they are parsed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setXIncludeAware(kotlin.Boolean)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set state of XInclude processing. |
| --- | --- |

## Protected constructors

### DocumentBuilderFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected DocumentBuilderFactory()
```

## Public methods

### getAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getAttribute(name: String!): Any!
```

Allows the user to retrieve specific attributes on the underlying implementation.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the attribute. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | value The value of the attribute. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | thrown if the underlying implementation doesn't recognize the attribute. |

### getFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getFeature(name: String!): Boolean
```

Get the state of the named feature.

Feature names are fully qualified `https://developer.android.com/reference/kotlin/java/net/URI.html#`s. Implementations may define their own features. An `https://developer.android.com/reference/kotlin/javax/xml/parsers/ParserConfigurationException` is thrown if this `DocumentBuilderFactory` or the `DocumentBuilder`s it creates cannot support the feature. It is possible for an `DocumentBuilderFactory` to expose a feature value but be unable to change its state.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Feature name. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | State of the named feature. |

| Exceptions ||
|---|---|
| `javax.xml.parsers.ParserConfigurationException` | if this `DocumentBuilderFactory` or the `DocumentBuilder`s it creates cannot support this feature. |

### getSchema

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSchema(): Schema!
```

Gets the `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` object specified through the `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setSchema(javax.xml.validation.Schema)` method.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#!` | the `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` object that was last set through the `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setSchema(javax.xml.validation.Schema)` method, or null if the method was not invoked since a `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#` is created. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | For backward compatibility, when implementations for earlier versions of JAXP is used, this exception will be thrown. |

### isCoalescing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCoalescing(): Boolean
```

Indicates whether or not the factory is configured to produce parsers which converts CDATA nodes to Text nodes and appends it to the adjacent (if any) Text node.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the factory is configured to produce parsers which converts CDATA nodes to Text nodes and appends it to the adjacent (if any) Text node; false otherwise. |

### isExpandEntityReferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isExpandEntityReferences(): Boolean
```

Indicates whether or not the factory is configured to produce parsers which expand entity reference nodes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the factory is configured to produce parsers which expand entity reference nodes; false otherwise. |

### isIgnoringComments

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isIgnoringComments(): Boolean
```

Indicates whether or not the factory is configured to produce parsers which ignores comments.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the factory is configured to produce parsers which ignores comments; false otherwise. |

### isIgnoringElementContentWhitespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isIgnoringElementContentWhitespace(): Boolean
```

Indicates whether or not the factory is configured to produce parsers which ignore ignorable whitespace in element content.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the factory is configured to produce parsers which ignore ignorable whitespace in element content; false otherwise. |

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

### newDefaultInstance

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newDefaultInstance(): DocumentBuilderFactory!
```

Creates a new instance of the `DocumentBuilderFactory` builtin system-default implementation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#!` | A new instance of the `DocumentBuilderFactory` builtin system-default implementation. |

### newDefaultNSInstance

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newDefaultNSInstance(): DocumentBuilderFactory!
```

Creates a new NamespaceAware instance of the `DocumentBuilderFactory` builtin system-default implementation. Parsers produced by the factory instance provides support for XML namespaces by default.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#!` | a new instance of the `DocumentBuilderFactory` builtin system-default implementation. |

### newDocumentBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun newDocumentBuilder(): DocumentBuilder!
```

Creates a new instance of a `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder` using the currently configured parameters.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder!` | A new instance of a DocumentBuilder. |

| Exceptions ||
|---|---|
| `javax.xml.parsers.ParserConfigurationException` | if a DocumentBuilder cannot be created which satisfies the configuration requested. |

### newInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newInstance(): DocumentBuilderFactory!
```

Returns Android's implementation of `DocumentBuilderFactory`. Unlike other Java implementations, this method does not consult system properties, property files, or the services API. On Android this is the same as `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#newDefaultInstance()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#!` | a new DocumentBuilderFactory. |

### newInstance

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newInstance(
    factoryClassName: String!, 
    classLoader: ClassLoader!
): DocumentBuilderFactory!
```

Returns an instance of the named implementation of `DocumentBuilderFactory`.

| Exceptions ||
|---|---|
| `javax.xml.parsers.FactoryConfigurationError` | if `factoryClassName` is not available or cannot be instantiated. |

### newNSInstance

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newNSInstance(): DocumentBuilderFactory!
```

Creates a new NamespaceAware, Android-specific instance of a `DocumentBuilderFactory`. Unlike other Java implementations, this method does not consult system properties, property files, or the services API. On Android this is the same as `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#newDefaultNSInstance()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#!` | a new instance of a `DocumentBuilderFactory` |

### newNSInstance

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newNSInstance(
    factoryClassName: String!, 
    classLoader: ClassLoader!
): DocumentBuilderFactory!
```

Creates a new NamespaceAware instance of a `DocumentBuilderFactory` from the class name. Parsers produced by the factory instance provides support for XML namespaces by default.

| Parameters ||
|---|---|
| `factoryClassName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a fully qualified factory class name that provides implementation of `javax.xml.parsers.DocumentBuilderFactory`. |
| `classLoader` | [ClassLoader](../java/lang/ClassLoader.md)!: the `ClassLoader` used to load the factory class. If it is `null`, the current `Thread`'s context classLoader is used to load the factory class. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#!` | a new instance of a `DocumentBuilderFactory` |

| Exceptions ||
|---|---|
| `javax.xml.parsers.FactoryConfigurationError` | if `factoryClassName` is `null`, or the factory class cannot be loaded, instantiated. |

### setAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setAttribute(
    name: String!, 
    value: Any!
): Unit
```

Allows the user to set specific attributes on the underlying implementation.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the attribute. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The value of the attribute. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | thrown if the underlying implementation doesn't recognize the attribute. |

### setCoalescing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCoalescing(coalescing: Boolean): Unit
```

Specifies that the parser produced by this code will convert CDATA nodes to Text nodes and append it to the adjacent (if any) text node. By default the value of this is set to `false`

| Parameters ||
|---|---|
| `coalescing` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the parser produced will convert CDATA nodes to Text nodes and append it to the adjacent (if any) text node; false otherwise. |

### setExpandEntityReferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExpandEntityReferences(expandEntityRef: Boolean): Unit
```

Specifies that the parser produced by this code will expand entity reference nodes. By default the value of this is set to `true`

| Parameters ||
|---|---|
| `expandEntityRef` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the parser produced will expand entity reference nodes; false otherwise. |

### setFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setFeature(
    name: String!, 
    value: Boolean
): Unit
```

Set a feature for this `DocumentBuilderFactory` and `DocumentBuilder`s created by this factory.

Feature names are fully qualified `https://developer.android.com/reference/kotlin/java/net/URI.html#`s. Implementations may define their own features. An `https://developer.android.com/reference/kotlin/javax/xml/parsers/ParserConfigurationException` is thrown if this `DocumentBuilderFactory` or the `DocumentBuilder`s it creates cannot support the feature. It is possible for an `DocumentBuilderFactory` to expose a feature value but be unable to change its state.

Earlier versions of this documentation have mandated support for the `https://developer.android.com/reference/kotlin/javax/xml/XMLConstants.html#FEATURE_SECURE_PROCESSING:kotlin.String` feature, but this is not a supported feature on any version of Android.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Feature name. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Is feature state `true` or `false`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If the `name` parameter is null. |
| `javax.xml.parsers.ParserConfigurationException` | if this `DocumentBuilderFactory` or the `DocumentBuilder`s it creates cannot support this feature. |

### setIgnoringComments

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIgnoringComments(ignoreComments: Boolean): Unit
```

Specifies that the parser produced by this code will ignore comments. By default the value of this is set to `false `.

| Parameters ||
|---|---|
| `ignoreComments` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `boolean` value to ignore comments during processing |

### setIgnoringElementContentWhitespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIgnoringElementContentWhitespace(whitespace: Boolean): Unit
```

Specifies that the parsers created by this factory must eliminate whitespace in element content (sometimes known loosely as 'ignorable whitespace') when parsing XML documents (see XML Rec 2.10). Note that only whitespace which is directly contained within element content that has an element only content model (see XML Rec 3.2.1) will be eliminated. Due to reliance on the content model this setting requires the parser to be in validating mode. By default the value of this is set to `false`.

| Parameters ||
|---|---|
| `whitespace` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the parser created must eliminate whitespace in the element content when parsing XML documents; false otherwise. |

### setNamespaceAware

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNamespaceAware(awareness: Boolean): Unit
```

Specifies that the parser produced by this code will provide support for XML namespaces. By default the value of this is set to `false`

| Parameters ||
|---|---|
| `awareness` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the parser produced will provide support for XML namespaces; false otherwise. |

### setSchema

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSchema(schema: Schema!): Unit
```

Set the `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` to be used by parsers created from this factory.

When a `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` is non-null, a parser will use a validator created from it to validate documents before it passes information down to the application.

When errors are found by the validator, the parser is responsible to report them to the user-specified `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#` (or if the error handler is not set, ignore them or throw them), just like any other errors found by the parser itself. In other words, if the user-specified `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#` is set, it must receive those errors, and if not, they must be treated according to the implementation specific default error handling rules.

A validator may modify the outcome of a parse (for example by adding default values that were missing in documents), and a parser is responsible to make sure that the application will receive modified DOM trees.

Initially, null is set as the `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#`.

This processing will take effect even if the `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#isValidating()` method returns false.

It is an error to use the `http://java.sun.com/xml/jaxp/properties/schemaSource` property and/or the `http://java.sun.com/xml/jaxp/properties/schemaLanguage` property in conjunction with a `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` object. Such configuration will cause a `https://developer.android.com/reference/kotlin/javax/xml/parsers/ParserConfigurationException` exception when the `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#newDocumentBuilder()` is invoked.

#### Note for implementors

A parser must be able to work with any `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema.html#` implementation. However, parsers and schemas are allowed to use implementation-specific custom mechanisms as long as they yield the result described in the specification.

| Parameters ||
|---|---|
| `schema` | [Schema](../javax/xml/validation/Schema.md)!: `Schema` to use or `null` to remove a schema. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | For backward compatibility, when implementations for earlier versions of JAXP is used, this exception will be thrown. |

### setValidating

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setValidating(validating: Boolean): Unit
```

Specifies that the parser produced by this code will validate documents as they are parsed. By default the value of this is set to `false`.

Note that "the validation" here means [a validating parser](http://www.w3.org/TR/REC-xml#proc-types) as defined in the XML recommendation. In other words, it essentially just controls the DTD validation. (except the legacy two properties defined in JAXP 1.2. See [here](../javax/xml/parsers/DocumentBuilderFactory.md) for more details.)

To use modern schema languages such as W3C XML Schema or RELAX NG instead of DTD, you can configure your parser to be a non-validating parser by leaving the `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setValidating(kotlin.Boolean)` method false, then use the `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory#setSchema(javax.xml.validation.Schema)` method to associate a schema to a parser.

| Parameters ||
|---|---|
| `validating` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the parser produced will validate documents as they are parsed; false otherwise. |

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
