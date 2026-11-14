# Locator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Locator

```
interface Locator
```

| [org.xml.sax.Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator#) |

| Known Direct Subclasses [Driver](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver.html#), [Locator2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2), [LocatorImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/LocatorImpl) |-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------| | [Driver](https://developer.android.com/reference/kotlin/org/xmlpull/v1/sax2/Driver.html#) | SAX2 Driver that pulls events from XmlPullParser and converts them into SAX2 callbacks. | | [Locator2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2) | SAX2 extension to augment the entity information provided though a [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator#). | | [LocatorImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/LocatorImpl) | Provide an optional convenience implementation of Locator. | |

| Known Indirect Subclasses [Locator2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl) [Locator2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl) |---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Locator2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl) | SAX2 extension helper for holding additional Entity information, implementing the [Locator2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2) interface. | | [Locator2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl) | SAX2 extension helper for holding additional Entity information, implementing the [Locator2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2) interface. | |

Interface for associating a SAX event with a document location.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

If a SAX parser provides location information to the SAX application, it does so by implementing this interface and then passing an instance to the application using the content handler's [setDocumentLocator](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler#setDocumentLocator(org.xml.sax.Locator))method. The application can use the object to obtain the location of any other SAX event in the XML source document.

Note that the results returned by the object will be valid only during the scope of each callback method: the application will receive unpredictable results if it attempts to use the locator at any other time, or after parsing completes.

SAX parsers are not required to supply a locator, but they are very strongly encouraged to do so. If the parser supplies a locator, it must do so before reporting any other document events. If no locator has been set by the time the application receives the [startDocument](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler#startDocument())event, the application should assume that a locator is not available.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnNumber](https://developer.android.com/reference/kotlin/org/xml/sax/Locator#getColumnNumber())`()` Return the column number where the current document event ends. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineNumber](https://developer.android.com/reference/kotlin/org/xml/sax/Locator#getLineNumber())`()` Return the line number where the current document event ends. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPublicId](https://developer.android.com/reference/kotlin/org/xml/sax/Locator#getPublicId())`()` Return the public identifier for the current document event. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](https://developer.android.com/reference/kotlin/org/xml/sax/Locator#getSystemId())`()` Return the system identifier for the current document event. |

## Public methods

### getColumnNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnNumber(): Int
```

Return the column number where the current document event ends. This is one-based number of Java`char`values since the last line end.

**Warning:**The return value from the method is intended only as an approximation for the sake of diagnostics; it is not intended to provide sufficient information to edit the character content of the original XML document. For example, when lines contain combining character sequences, wide characters, surrogate pairs, or bi-directional text, the value may not correspond to the column in a text editor's display.

The return value is an approximation of the column number in the document entity or external parsed entity where the markup triggering the event appears.

If possible, the SAX driver should provide the line position of the first character after the text associated with the document event. The first column in each line is column 1.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The column number, or -1 if none is available. |

**See Also**

- [#getLineNumber](https://developer.android.com/reference/kotlin/org/xml/sax/Locator#getLineNumber()) 

### getLineNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLineNumber(): Int
```

Return the line number where the current document event ends. Lines are delimited by line ends, which are defined in the XML specification.

**Warning:**The return value from the method is intended only as an approximation for the sake of diagnostics; it is not intended to provide sufficient information to edit the character content of the original XML document. In some cases, these "line" numbers match what would be displayed as columns, and in others they may not match the source text due to internal entity expansion.

The return value is an approximation of the line number in the document entity or external parsed entity where the markup triggering the event appears.

If possible, the SAX driver should provide the line position of the first character after the text associated with the document event. The first line is line 1.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The line number, or -1 if none is available. |

**See Also**

- [#getColumnNumber](https://developer.android.com/reference/kotlin/org/xml/sax/Locator#getColumnNumber()) 

### getPublicId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPublicId(): String!
```

Return the public identifier for the current document event.

The return value is the public identifier of the document entity or of the external parsed entity in which the markup triggering the event appears.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string containing the public identifier, or null if none is available. |

**See Also**

- [#getSystemId](https://developer.android.com/reference/kotlin/org/xml/sax/Locator#getSystemId()) 

### getSystemId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSystemId(): String!
```

Return the system identifier for the current document event.

The return value is the system identifier of the document entity or of the external parsed entity in which the markup triggering the event appears.

If the system identifier is a URL, the parser must resolve it fully before passing it to the application. For example, a file name must always be provided as a*file:...*URL, and other kinds of relative URI are also resolved against their bases.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string containing the system identifier, or null if none is available. |

**See Also**

- [#getPublicId](https://developer.android.com/reference/kotlin/org/xml/sax/Locator#getPublicId())
