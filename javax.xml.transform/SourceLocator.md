# SourceLocator

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SourceLocator

```
interface SourceLocator
```

| [javax.xml.transform.SourceLocator](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator#) |

| Known Direct Subclasses [DOMLocator](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMLocator) |-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------| | [DOMLocator](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMLocator) | Indicates the position of a node in a source DOM, intended primarily for error reporting. | |
| --- | --- | --- | --- | --- | --- | --- |

This interface is primarily for the purposes of reporting where an error occurred in the XML source or transformation instructions.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnNumber](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator#getColumnNumber())`()` Return the character position where the current document event ends. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineNumber](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator#getLineNumber())`()` Return the line number where the current document event ends. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPublicId](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator#getPublicId())`()` Return the public identifier for the current document event. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator#getSystemId())`()` Return the system identifier for the current document event. |

## Public methods

### getColumnNumber

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnNumber(): Int
```

Return the character position where the current document event ends.

**Warning:**The return value from the method is intended only as an approximation for the sake of error reporting; it is not intended to provide sufficient information to edit the character content of the original XML document.

The return value is an approximation of the column number in the document entity or external parsed entity where the markup that triggered the event appears.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The column number, or -1 if none is available. |

**See Also**

- [#getLineNumber](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator#getLineNumber()) 

### getLineNumber

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLineNumber(): Int
```

Return the line number where the current document event ends.

**Warning:**The return value from the method is intended only as an approximation for the sake of error reporting; it is not intended to provide sufficient information to edit the character content of the original XML document.

The return value is an approximation of the line number in the document entity or external parsed entity where the markup that triggered the event appears.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The line number, or -1 if none is available. |

**See Also**

- [#getColumnNumber](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator#getColumnNumber()) 

### getPublicId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPublicId(): String!
```

Return the public identifier for the current document event.

The return value is the public identifier of the document entity or of the external parsed entity in which the markup that triggered the event appears.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string containing the public identifier, or null if none is available. |

**See Also**

- [#getSystemId](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator#getSystemId()) 

### getSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSystemId(): String!
```

Return the system identifier for the current document event.

The return value is the system identifier of the document entity or of the external parsed entity in which the markup that triggered the event appears.

If the system identifier is a URL, the parser must resolve it fully before passing it to the application.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string containing the system identifier, or null if none is available. |

**See Also**

- [#getPublicId](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator#getPublicId())
