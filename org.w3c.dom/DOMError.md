# DOMError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DOMError

```
interface DOMError
```

| [org.w3c.dom.DOMError](../org/w3c/dom/DOMError.md) |

`DOMError`is an interface that describes an error.

See also the [Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407).

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [SEVERITY_ERROR](../org/w3c/dom/DOMError.md) The severity of the error described by the`DOMError`is error. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [SEVERITY_FATAL_ERROR](../org/w3c/dom/DOMError.md) The severity of the error described by the`DOMError`is fatal error. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [SEVERITY_WARNING](../org/w3c/dom/DOMError.md) The severity of the error described by the`DOMError`is warning. |
| --- | --- |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DOMLocator](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-locator/index.html)! | [getLocation](../org/w3c/dom/DOMError.md))`()` The location of the error. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMessage](../org/w3c/dom/DOMError.md))`()` An implementation specific string describing the error that occurred. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getRelatedData](../org/w3c/dom/DOMError.md))`()` The related`DOMError.type`dependent data if any. |
| --- | --- |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getRelatedException](../org/w3c/dom/DOMError.md))`()` The related platform dependent exception if any. |
| abstract [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getSeverity](../org/w3c/dom/DOMError.md))`()` The severity of the error, either`SEVERITY_WARNING`,`SEVERITY_ERROR`, or`SEVERITY_FATAL_ERROR`. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](../org/w3c/dom/DOMError.md))`()` A`DOMString`indicating which related data is expected in`relatedData`. |
| --- | --- |

## Constants

### SEVERITY_ERROR

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEVERITY_ERROR: Short
```

The severity of the error described by the`DOMError`is error. A`SEVERITY_ERROR`may not cause the processing to stop if the error can be recovered, unless`DOMErrorHandler.handleError()`returns`false`. 

 Value: 2

### SEVERITY_FATAL_ERROR

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEVERITY_FATAL_ERROR: Short
```

The severity of the error described by the`DOMError`is fatal error. A`SEVERITY_FATAL_ERROR`will cause the normal processing to stop. The return value of`DOMErrorHandler.handleError()`is ignored unless the implementation chooses to continue, in which case the behavior becomes undefined. 

 Value: 3

### SEVERITY_WARNING

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEVERITY_WARNING: Short
```

The severity of the error described by the`DOMError`is warning. A`SEVERITY_WARNING`will not cause the processing to stop, unless`DOMErrorHandler.handleError()`returns`false`. 

 Value: 1

## Public methods

### getLocation

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLocation(): DOMLocator!
```

The location of the error. 

### getMessage

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMessage(): String!
```

An implementation specific string describing the error that occurred. 

### getRelatedData

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRelatedData(): Any!
```

The related`DOMError.type`dependent data if any. 

### getRelatedException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRelatedException(): Any!
```

The related platform dependent exception if any. 

### getSeverity

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSeverity(): Short
```

The severity of the error, either`SEVERITY_WARNING`,`SEVERITY_ERROR`, or`SEVERITY_FATAL_ERROR`. 

### getType

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getType(): String!
```

A`DOMString`indicating which related data is expected in`relatedData`. Users should refer to the specification of the error in order to find its`DOMString`type and`relatedData`definitions if any.

**Note:** As an example,`Document.normalizeDocument()`does generate warnings when the "split-cdata-sections" parameter is in use. Therefore, the method generates a`SEVERITY_WARNING`with`type``"cdata-sections-splitted"`and the first`CDATASection`node in document order resulting from the split is returned by the`relatedData`attribute.
