# LSException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LSException

```
open class LSException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [org.w3c.dom.ls.LSException](../org/w3c/dom/ls/LSException.md) |

Parser or write operations may throw an `LSException` if the processing is stopped. The processing can be stopped due to a `DOMError` with a severity of `DOMError.SEVERITY_FATAL_ERROR` or a non recovered `DOMError.SEVERITY_ERROR`, or if `DOMErrorHandler.handleError()` returned `false`.

**Note:** As suggested in the definition of the constants in the `DOMError` interface, a DOM implementation may choose to continue after a fatal error, but the resulting DOM tree is then implementation dependent.

See also the [Document Object Model (DOM) Level 3 Load and Save Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-LS-20040407).

## Summary

| Constants ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [PARSE_ERR](../org/w3c/dom/ls/LSException.md) If an attempt was made to load a document, or an XML Fragment, using `LSParser` and the processing has been stopped. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [SERIALIZE_ERR](../org/w3c/dom/ls/LSException.md) If an attempt was made to serialize a `Node` using `LSSerializer` and the processing has been stopped. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LSException](../org/w3c/dom/ls/LSException.md))`(`code:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Properties ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [code](../org/w3c/dom/ls/LSException.md) <br /> |

## Constants

### PARSE_ERR

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARSE_ERR: Short
```

If an attempt was made to load a document, or an XML Fragment, using `LSParser` and the processing has been stopped. 

 Value: 81

### SERIALIZE_ERR

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERIALIZE_ERR: Short
```

If an attempt was made to serialize a `Node` using `LSSerializer` and the processing has been stopped. 

 Value: 82

## Public constructors

### LSException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LSException(
    code: Short, 
    message: String!)
```

## Properties

### code

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var code: Short
```
