Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ValidatorHandler

```
abstract class ValidatorHandler : ContentHandler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.validation.ValidatorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#) |

Streaming validator that works on SAX stream.

A `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` object is a thread-unsafe, non-reentrant object. In other words, it is the application's responsibility to make sure that one `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` object is not used from more than one thread at any given time.

`https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` checks if the SAX events follow the set of constraints described in the associated `https://developer.android.com/reference/kotlin/javax/xml/validation/Schema`, and additionally it may modify the SAX events (for example by adding default values, etc.)

`https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` extends from `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#`, but it refines the underlying `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` in the following way:

1. startElement/endElement events must receive non-null String for `uri`, `localName`, and `qname`, even though SAX allows some of them to be null. Similarly, the user-specified `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` will receive non-null Strings for all three parameters.
2. Applications must ensure that `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#`'s `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startPrefixMapping(kotlin.String,%20kotlin.String)` and `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endPrefixMapping(kotlin.String)` are invoked properly. Similarly, the user-specified `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` will receive startPrefixMapping/endPrefixMapping events. If the `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` introduces additional namespace bindings, the user-specified `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` will receive additional startPrefixMapping/endPrefixMapping events.
3. `https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#` for the `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startElement(kotlin.String,%20kotlin.String,%20kotlin.String,%20org.xml.sax.Attributes)` method may or may not include xmlns\* attributes.

A `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` is automatically reset every time the startDocument method is invoked.

## Recognized Properties and Features

This spec defines the following feature that must be recognized by all `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` implementations.

### `http://xml.org/sax/features/namespace-prefixes`

This feature controls how a `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` introduces namespace bindings that were not present in the original SAX event stream. When this feature is set to true, it must make sure that the user's `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` will see the corresponding `xmlns*` attribute in the `https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#` object of the `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startElement(kotlin.String,%20kotlin.String,%20kotlin.String,%20org.xml.sax.Attributes)` callback. Otherwise, `xmlns*` attributes must not be added to `https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#` that's passed to the user-specified `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#`.

(Note that regardless of this switch, namespace bindings are always notified to applications through `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startPrefixMapping(kotlin.String,%20kotlin.String)` and `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endPrefixMapping(kotlin.String)` methods of the `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` specified by the user.)

Note that this feature does *NOT* affect the way a `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` receives SAX events. It merely changes the way it augments SAX events.

This feature is set to `false` by default.

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#ValidatorHandler()()` Constructor for derived classes. |

| Public methods ||
|---|---|
| abstract [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)! | `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#getContentHandler()()` Gets the `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` which receives the augmented validation result. |
| abstract [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)! | `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#getErrorHandler()()` Gets the current `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#` set to this `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#getFeature(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Look up the value of a feature flag. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#getProperty(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Look up the value of a property. |
| abstract [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#)! | `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#getResourceResolver()()` Gets the current `https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#` set to this `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#`. |
| abstract [TypeInfoProvider](https://developer.android.com/reference/kotlin/javax/xml/validation/TypeInfoProvider)! | `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#getTypeInfoProvider()()` Obtains the `https://developer.android.com/reference/kotlin/javax/xml/validation/TypeInfoProvider` implementation of this `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#setContentHandler(org.xml.sax.ContentHandler)(receiver: https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#!)` Sets the `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` which receives the augmented validation result. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#setErrorHandler(org.xml.sax.ErrorHandler)(errorHandler: https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#!)` Sets the `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#` to receive errors encountered during the validation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#setFeature(kotlin.String,%20kotlin.Boolean)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set the value of a feature flag. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#setProperty(kotlin.String,%20kotlin.Any)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, object: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Set the value of a property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#setResourceResolver(org.w3c.dom.ls.LSResourceResolver)(resourceResolver: https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#!)` Sets the `https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#` to customize resource resolution while in a validation episode. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#characters(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Receive notification of character data. The Parser will call this method to report each chunk of character data. SAX parsers may return all contiguous character data in a single chunk, or they may split it into several chunks; however, all of the characters in any single event must come from the same external entity so that the Locator provides useful information. The application must not attempt to read from the array outside of the specified range. Individual characters may consist of more than one Java `char` value. There are two important cases where this happens, because characters can't be represented in just sixteen bits. In one case, characters are represented in a *Surrogate Pair*, using two special Unicode values. Such characters are in the so-called "Astral Planes", with a code point above U+FFFF. A second case involves composite characters, such as a base character combining with one or more accent characters. Your code should not assume that algorithms using `char`-at-a-time idioms will be working in character units; in some cases they will split characters. This is relevant wherever XML permits arbitrary characters, such as attribute values, processing instruction data, and comments as well as in data reported from this method. It's also generally relevant whenever Java code manipulates internationalized text; the issue isn't unique to XML. Note that some parsers will report whitespace in element content using the `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#ignorableWhitespace(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)` method rather than this one (validating parsers *must* do so). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endDocument()()` Receive notification of the end of a document. **There is an apparent contradiction between the documentation for this method and the documentation for `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#fatalError(org.xml.sax.SAXParseException)`. Until this ambiguity is resolved in a future major release, clients should make no assumptions about whether endDocument() will or will not be invoked when the parser has reported a fatalError() or thrown an exception.** The SAX parser will invoke this method only once, and it will be the last method invoked during the parse. The parser shall not invoke this method until it has either abandoned parsing (because of an unrecoverable error) or reached the end of input. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endElement(kotlin.String,%20kotlin.String,%20kotlin.String)(uri: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, localName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, qName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Receive notification of the end of an element. The SAX parser will invoke this method at the end of every element in the XML document; there will be a corresponding `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startElement(kotlin.String,%20kotlin.String,%20kotlin.String,%20org.xml.sax.Attributes)` event for every endElement event (even when the element is empty). For information on the names, see startElement. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endPrefixMapping(kotlin.String)(prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` End the scope of a prefix-URI mapping. See `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startPrefixMapping(kotlin.String,%20kotlin.String)` for details. These events will always occur immediately after the corresponding `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endElement(kotlin.String,%20kotlin.String,%20kotlin.String)` event, but the order of `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endPrefixMapping(kotlin.String)` events is not otherwise guaranteed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#ignorableWhitespace(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Receive notification of ignorable whitespace in element content. Validating Parsers must use this method to report each chunk of whitespace in element content (see the W3C XML 1.0 recommendation, section 2.10): non-validating parsers may also use this method if they are capable of parsing and using content models. SAX parsers may return all contiguous whitespace in a single chunk, or they may split it into several chunks; however, all of the characters in any single event must come from the same external entity, so that the Locator provides useful information. The application must not attempt to read from the array outside of the specified range. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#processingInstruction(kotlin.String,%20kotlin.String)(target: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Receive notification of a processing instruction. The Parser will invoke this method once for each processing instruction found: note that processing instructions may occur before or after the main document element. A SAX parser must never report an XML declaration (XML 1.0, section 2.8) or a text declaration (XML 1.0, section 4.3.1) using this method. Like `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#characters(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)`, processing instruction data may have characters that need more than one `char` value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#setDocumentLocator(org.xml.sax.Locator)(locator: https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#!)` Receive an object for locating the origin of SAX document events. SAX parsers are strongly encouraged (though not absolutely required) to supply a locator: if it does so, it must supply the locator to the application by invoking this method before invoking any of the other methods in the ContentHandler interface. The locator allows the application to determine the end position of any document-related event, even if the parser is not reporting an error. Typically, the application will use this information for reporting its own errors (such as character content that does not match an application's business rules). The information returned by the locator is probably not sufficient for use with a search engine. Note that the locator will return correct information only during the invocation SAX event callbacks after `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startDocument()` returns and before `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endDocument()` is called. The application should not attempt to use it at any other time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#skippedEntity(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Receive notification of a skipped entity. This is not called for entity references within markup constructs such as element start tags or markup declarations. (The XML recommendation requires reporting skipped external entities. SAX also reports internal entity expansion/non-expansion, except within markup constructs.) The Parser will invoke this method each time the entity is skipped. Non-validating processors may skip entities if they have not seen the declarations (because, for example, the entity was declared in an external DTD subset). All processors may skip external entities, depending on the values of the `http://xml.org/sax/features/external-general-entities` and the `http://xml.org/sax/features/external-parameter-entities` properties. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startDocument()()` Receive notification of the beginning of a document. The SAX parser will invoke this method only once, before any other event callbacks (except for `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#setDocumentLocator(org.xml.sax.Locator)`). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startElement(kotlin.String,%20kotlin.String,%20kotlin.String,%20org.xml.sax.Attributes)(uri: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, localName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, qName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, atts: https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#!)` Receive notification of the beginning of an element. The Parser will invoke this method at the beginning of every element in the XML document; there will be a corresponding `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endElement(kotlin.String,%20kotlin.String,%20kotlin.String)` event for every startElement event (even when the element is empty). All of the element's content will be reported, in order, before the corresponding endElement event. This event allows up to three name components for each element: 1. the Namespace URI; 2. the local name; and 3. the qualified (prefixed) name. Any or all of these may be provided, depending on the values of the http://xml.org/sax/features/namespaces and the http://xml.org/sax/features/namespace-prefixes properties: - the Namespace URI and local name are required when the namespaces property is true (the default), and are optional when the namespaces property is false (if one is specified, both must be); - the qualified name is required when the namespace-prefixes property is true, and is optional when the namespace-prefixes property is false (the default). Note that the attribute list provided will contain only attributes with explicit values (specified or defaulted): #IMPLIED attributes will be omitted. The attribute list will contain attributes used for Namespace declarations (xmlns\* attributes) only if the `http://xml.org/sax/features/namespace-prefixes` property is true (it is false by default, and support for a true value is optional). Like `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#characters(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)`, attribute values may have characters that need more than one `char` value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startPrefixMapping(kotlin.String,%20kotlin.String)(prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, uri: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Begin the scope of a prefix-URI Namespace mapping. The information from this event is not necessary for normal Namespace processing: the SAX XML reader will automatically replace prefixes for element and attribute names when the `http://xml.org/sax/features/namespaces` feature is true (the default). There are cases, however, when applications need to use prefixes in character data or in attribute values, where they cannot safely be expanded automatically; the start/endPrefixMapping event supplies the information to the application to expand prefixes in those contexts itself, if necessary. Note that start/endPrefixMapping events are not guaranteed to be properly nested relative to each other: all startPrefixMapping events will occur immediately before the corresponding `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startElement(kotlin.String,%20kotlin.String,%20kotlin.String,%20org.xml.sax.Attributes)` event, and all `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endPrefixMapping(kotlin.String)` events will occur immediately after the corresponding `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endElement(kotlin.String,%20kotlin.String,%20kotlin.String)` event, but their order is not otherwise guaranteed. There should never be start/endPrefixMapping events for the "xml" prefix, since it is predeclared and immutable. <br /> | ||

## Protected constructors

### ValidatorHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected ValidatorHandler()
```

Constructor for derived classes.

The constructor does nothing.

Derived classes must create `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` objects that have null `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#` and null `https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#`.

## Public methods

### getContentHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getContentHandler(): ContentHandler!
```

Gets the `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` which receives the augmented validation result.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#!` | This method returns the object that was last set through the `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#getContentHandler()` method, or null if that method has never been called since this `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` has created. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#setContentHandler(org.xml.sax.ContentHandler)`

### getErrorHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getErrorHandler(): ErrorHandler!
```

Gets the current `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#` set to this `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#!` | This method returns the object that was last set through the `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#setErrorHandler(org.xml.sax.ErrorHandler)` method, or null if that method has never been called since this `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` has created. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#setErrorHandler(org.xml.sax.ErrorHandler)`

### getFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFeature(name: String!): Boolean
```

Look up the value of a feature flag.

The feature name is any fully-qualified URI. It is possible for a `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` to recognize a feature name but temporarily be unable to return its value. Some feature values may be available only in specific contexts, such as before, during, or after a validation.

Implementors are free (and encouraged) to invent their own features, using names built on their own URIs.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The feature name, which is a non-null fully-qualified URI. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The current value of the feature (true or false). |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | When the name parameter is null. |
| `org.xml.sax.SAXNotRecognizedException` | If the feature value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` recognizes the feature name but cannot determine its value at this time. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#setFeature(kotlin.String,%20kotlin.Boolean)`

### getProperty

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProperty(name: String!): Any!
```

Look up the value of a property.

The property name is any fully-qualified URI. It is possible for a `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` to recognize a property name but temporarily be unable to return its value. Some property values may be available only in specific contexts, such as before, during, or after a validation.

`https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#`s are not required to recognize any specific property names.

Implementors are free (and encouraged) to invent their own properties, using names built on their own URIs.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The property name, which is a non-null fully-qualified URI. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | The current value of the property. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | When the name parameter is null. |
| `org.xml.sax.SAXNotRecognizedException` | If the property value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the XMLReader recognizes the property name but cannot determine its value at this time. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#setProperty(kotlin.String,%20kotlin.Any)`

### getResourceResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getResourceResolver(): LSResourceResolver!
```

Gets the current `https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#` set to this `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#!` | This method returns the object that was last set through the `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#setResourceResolver(org.w3c.dom.ls.LSResourceResolver)` method, or null if that method has never been called since this `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` has created. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#setErrorHandler(org.xml.sax.ErrorHandler)`

### getTypeInfoProvider

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getTypeInfoProvider(): TypeInfoProvider!
```

Obtains the `https://developer.android.com/reference/kotlin/javax/xml/validation/TypeInfoProvider` implementation of this `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#`.

The obtained `https://developer.android.com/reference/kotlin/javax/xml/validation/TypeInfoProvider` can be queried during a parse to access the type information determined by the validator.

Some schema languages do not define the notion of type, for those languages, this method may not be supported. However, to be compliant with this specification, implementations for W3C XML Schema 1.0 must support this operation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/validation/TypeInfoProvider!` | null if the validator / schema language does not support the notion of `https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-type-info/index.html`. Otherwise a non-null valid `https://developer.android.com/reference/kotlin/javax/xml/validation/TypeInfoProvider`. |

### setContentHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setContentHandler(receiver: ContentHandler!): Unit
```

Sets the `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` which receives the augmented validation result.

When a `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` is specified, a `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` will work as a filter and basically copy the incoming events to the specified `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#`.

In doing so, a `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` may modify the events, for example by adding defaulted attributes.

A `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` may buffer events to certain extent, but to allow `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` to be used by a parser, the following requirement has to be met.

1. When `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startElement(kotlin.String,%20kotlin.String,%20kotlin.String,%20org.xml.sax.Attributes)`, `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endElement(kotlin.String,%20kotlin.String,%20kotlin.String)`, `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#startDocument()`, or `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#endDocument()` are invoked on a `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#`, the same method on the user-specified `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` must be invoked for the same event before the callback returns.
2. `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` may not introduce new elements that were not present in the input.
3. `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` may not remove attributes that were present in the input.

When a callback method on the specified `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` throws an exception, the same exception object must be thrown from the `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#`. The `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#` should not be notified of such an exception.

This method can be called even during a middle of a validation.

| Parameters ||
|---|---|
| `receiver` | [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)!: A `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#` or a null value. |

### setErrorHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setErrorHandler(errorHandler: ErrorHandler!): Unit
```

Sets the `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#` to receive errors encountered during the validation.

Error handler can be used to customize the error handling process during a validation. When an `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#` is set, errors found during the validation will be first sent to the `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#`.

The error handler can abort further validation immediately by throwing `https://developer.android.com/reference/kotlin/org/xml/sax/SAXException.html#` from the handler. Or for example it can print an error to the screen and try to continue the validation by returning normally from the `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#`

If any `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#` is thrown from an `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#`, the same `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#` object will be thrown toward the root of the call stack.

`https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` is not allowed to throw `https://developer.android.com/reference/kotlin/org/xml/sax/SAXException.html#` without first reporting it to `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#`.

When the `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#` is null, the implementation will behave as if the following `https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#` is set:

```kotlin
class DraconianErrorHandler implements <code><a docref="org.xml.sax.ErrorHandler">ErrorHandler</a></code>{
      public void fatalError( <code><a docref="org.xml.sax.SAXParseException">org.xml.sax.SAXParseException</a></code>e ) throws <code><a docref="org.xml.sax.SAXException">org.xml.sax.SAXException</a></code>{
          throw e;
      }
      public void error( <code><a docref="org.xml.sax.SAXParseException">org.xml.sax.SAXParseException</a></code>e ) throws <code><a docref="org.xml.sax.SAXException">org.xml.sax.SAXException</a></code>{
          throw e;
      }
      public void warning( <code><a docref="org.xml.sax.SAXParseException">org.xml.sax.SAXParseException</a></code>e ) throws <code><a docref="org.xml.sax.SAXException">org.xml.sax.SAXException</a></code>{
          // noop
      }
  }
  
```

When a new `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` object is created, initially this field is set to null.

| Parameters ||
|---|---|
| `errorHandler` | [ErrorHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ErrorHandler.html#)!: A new error handler to be set. This parameter can be null. |

### setFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFeature(
    name: String!, 
    value: Boolean
): Unit
```

Set the value of a feature flag.

Feature can be used to control the way a `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` parses schemas, although `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#`s are not required to recognize any specific property names.

The feature name is any fully-qualified URI. It is possible for a `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` to expose a feature value but to be unable to change the current value. Some feature values may be immutable or mutable only in specific contexts, such as before, during, or after a validation.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The feature name, which is a non-null fully-qualified URI. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The requested value of the feature (true or false). |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | When the name parameter is null. |
| `org.xml.sax.SAXNotRecognizedException` | If the feature value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` recognizes the feature name but cannot set the requested value. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#getFeature(kotlin.String)`

### setProperty

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setProperty(
    name: String!, 
    object: Any!
): Unit
```

Set the value of a property.

The property name is any fully-qualified URI. It is possible for a `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` to recognize a property name but to be unable to change the current value. Some property values may be immutable or mutable only in specific contexts, such as before, during, or after a validation.

`https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#`s are not required to recognize setting any specific property names.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The property name, which is a non-null fully-qualified URI. |
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The requested value for the property. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | When the name parameter is null. |
| `org.xml.sax.SAXNotRecognizedException` | If the property value can't be assigned or retrieved. |
| `org.xml.sax.SAXNotSupportedException` | When the `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` recognizes the property name but cannot set the requested value. |
| --- | --- |

### setResourceResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setResourceResolver(resourceResolver: LSResourceResolver!): Unit
```

Sets the `https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#` to customize resource resolution while in a validation episode.

`https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` uses a `https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#` when it needs to locate external resources while a validation, although exactly what constitutes "locating external resources" is up to each schema language.

When the `https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#` is null, the implementation will behave as if the following `https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#` is set:

```kotlin
class DumbLSResourceResolver implements <code><a docref="org.w3c.dom.ls.LSResourceResolver">LSResourceResolver</a></code>{
      public <code><a docref="org.w3c.dom.ls.LSInput">org.w3c.dom.ls.LSInput</a></code>resolveResource(
          String publicId, String systemId, String baseURI) {
 
          return null; // always return null
      }
  }
  
```

If a `https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#` throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` (or instances of its derived classes), then the `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` will abort the parsing and the caller of the `validate` method will receive the same `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`.

When a new `https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#` object is created, initially this field is set to null.

| Parameters ||
|---|---|
| `resourceResolver` | [LSResourceResolver](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSResourceResolver.html#)!: A new resource resolver to be set. This parameter can be null. |
