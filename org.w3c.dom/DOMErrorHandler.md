# DOMErrorHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DOMErrorHandler

```
interface DOMErrorHandler
```

| [org.w3c.dom.DOMErrorHandler](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMErrorHandler#) |

`DOMErrorHandler`is a callback interface that the DOM implementation can call when reporting errors that happens while processing XML data, or when doing some other processing (e.g. validating a document). A`DOMErrorHandler`object can be attached to a`Document`using the "error-handler" on the`DOMConfiguration`interface. If more than one error needs to be reported during an operation, the sequence and numbers of the errors passed to the error handler are implementation dependent.

The application that is using the DOM implementation is expected to implement this interface.

See also the [Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [handleError](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMErrorHandler#handleError(org.w3c.dom.DOMError))`(`error:` ` [DOMError](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-error/index.html)!`)` This method is called on the error handler when an error occurs. |

## Public methods

### handleError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun handleError(error: DOMError!): Boolean
```

This method is called on the error handler when an error occurs. 
If an exception is thrown from this method, it is considered to be equivalent of returning`true`.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [DOMError](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-error/index.html)!:The error object that describes the error. This object may be reused by the DOM implementation across multiple calls to the`handleError`method. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If the`handleError`method returns`false`, the DOM implementation should stop the current processing when possible. If the method returns`true`, the processing may continue depending on`DOMError.severity`. |
