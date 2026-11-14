# Locator2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Locator2

```
interface Locator2 : Locator
```

| [org.xml.sax.ext.Locator2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2#) |

| Known Direct Subclasses [Locator2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl) |---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Locator2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl) | SAX2 extension helper for holding additional Entity information, implementing the [Locator2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2#) interface. | |
| --- | --- | --- | --- | --- | --- | --- |

SAX2 extension to augment the entity information provided though a [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#). If an implementation supports this extension, the Locator provided in [ContentHandler.setDocumentLocator()](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#setDocumentLocator(org.xml.sax.Locator))will implement this interface, and the*http://xml.org/sax/features/use-locator2* feature flag will have the value*true* .*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.*

XMLReader implementations are not required to support this information, and it is not part of core-only SAX2 distributions.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2#getEncoding())`()` Returns the name of the character encoding for the entity. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getXMLVersion](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2#getXMLVersion())`()` Returns the version of XML used for the entity. |

| Inherited functions ||
|---|---|
| From class [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#) |-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnNumber](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#getColumnNumber())`()` <br /> Return the column number where the current document event ends. This is one-based number of Java`char`values since the last line end. **Warning:**The return value from the method is intended only as an approximation for the sake of diagnostics; it is not intended to provide sufficient information to edit the character content of the original XML document. For example, when lines contain combining character sequences, wide characters, surrogate pairs, or bi-directional text, the value may not correspond to the column in a text editor's display. The return value is an approximation of the column number in the document entity or external parsed entity where the markup triggering the event appears. If possible, the SAX driver should provide the line position of the first character after the text associated with the document event. The first column in each line is column 1. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineNumber](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#getLineNumber())`()` <br /> Return the line number where the current document event ends. Lines are delimited by line ends, which are defined in the XML specification. **Warning:**The return value from the method is intended only as an approximation for the sake of diagnostics; it is not intended to provide sufficient information to edit the character content of the original XML document. In some cases, these "line" numbers match what would be displayed as columns, and in others they may not match the source text due to internal entity expansion. The return value is an approximation of the line number in the document entity or external parsed entity where the markup triggering the event appears. If possible, the SAX driver should provide the line position of the first character after the text associated with the document event. The first line is line 1. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPublicId](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#getPublicId())`()` <br /> Return the public identifier for the current document event. The return value is the public identifier of the document entity or of the external parsed entity in which the markup triggering the event appears. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#getSystemId())`()` <br /> Return the system identifier for the current document event. The return value is the system identifier of the document entity or of the external parsed entity in which the markup triggering the event appears. If the system identifier is a URL, the parser must resolve it fully before passing it to the application. For example, a file name must always be provided as a*file:...*URL, and other kinds of relative URI are also resolved against their bases. <br /> | ||

## Public methods

### getEncoding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncoding(): String!
```

Returns the name of the character encoding for the entity. If the encoding was declared externally (for example, in a MIME Content-Type header), that will be the name returned. Else if there was an*\<?xml ...encoding='...'?\>*declaration at the start of the document, that encoding name will be returned. Otherwise the encoding will been inferred (normally to be UTF-8, or some UTF-16 variant), and that inferred name will be returned.

When an [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#) is used to provide an entity's character stream, this method returns the encoding provided in that input stream.

Note that some recent W3C specifications require that text in some encodings be normalized, using Unicode Normalization Form C, before processing. Such normalization must be performed by applications, and would normally be triggered based on the value returned by this method.

Encoding names may be those used by the underlying JVM, and comparisons should be case-insensitive.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Name of the character encoding being used to interpret \* the entity's text, or null if this was not provided for a \* character stream passed through an InputSource or is otherwise not yet available in the current parsing state. |

### getXMLVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getXMLVersion(): String!
```

Returns the version of XML used for the entity. This will normally be the identifier from the current entity's*\<?xml version='...' ...?\>*declaration, or be defaulted by the parser.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Identifier for the XML version being used to interpret the entity's text, or null if that information is not yet available in the current parsing state. |
