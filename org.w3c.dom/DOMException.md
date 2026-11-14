# DOMException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DOMException

```
open class DOMException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [org.w3c.dom.DOMException](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#) |

DOM operations only raise exceptions in "exceptional" circumstances, i.e., when an operation is impossible to perform (either for logical reasons, because data is lost, or because the implementation has become unstable). In general, DOM methods return specific error values in ordinary processing situations, such as out-of-bound errors when using`NodeList`.

Implementations should raise other exceptions under other circumstances. For example, implementations should raise an implementation-dependent exception if a`null`argument is passed when`null`was not expected.

Some languages and object systems do not support the concept of exceptions. For such systems, error conditions may be indicated using native error reporting mechanisms. For some bindings, for example, methods may return error codes similar to those listed in the corresponding method descriptions.

See also the [Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407).

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOMSTRING_SIZE_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#DOMSTRING_SIZE_ERR:kotlin.Short) If the specified range of text does not fit into a`DOMString`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [HIERARCHY_REQUEST_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#HIERARCHY_REQUEST_ERR:kotlin.Short) If any`Node`is inserted somewhere it doesn't belong. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [INDEX_SIZE_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#INDEX_SIZE_ERR:kotlin.Short) If index or size is negative, or greater than the allowed value. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [INUSE_ATTRIBUTE_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#INUSE_ATTRIBUTE_ERR:kotlin.Short) If an attempt is made to add an attribute that is already in use elsewhere. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [INVALID_ACCESS_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#INVALID_ACCESS_ERR:kotlin.Short) If a parameter or an operation is not supported by the underlying object. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [INVALID_CHARACTER_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#INVALID_CHARACTER_ERR:kotlin.Short) If an invalid or illegal character is specified, such as in an XML name. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [INVALID_MODIFICATION_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#INVALID_MODIFICATION_ERR:kotlin.Short) If an attempt is made to modify the type of the underlying object. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [INVALID_STATE_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#INVALID_STATE_ERR:kotlin.Short) If an attempt is made to use an object that is not, or is no longer, usable. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [NAMESPACE_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#NAMESPACE_ERR:kotlin.Short) If an attempt is made to create or change an object in a way which is incorrect with regard to namespaces. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [NOT_FOUND_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#NOT_FOUND_ERR:kotlin.Short) If an attempt is made to reference a`Node`in a context where it does not exist. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [NOT_SUPPORTED_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#NOT_SUPPORTED_ERR:kotlin.Short) If the implementation does not support the requested type of object or operation. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [NO_DATA_ALLOWED_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#NO_DATA_ALLOWED_ERR:kotlin.Short) If data is specified for a`Node`which does not support data. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [NO_MODIFICATION_ALLOWED_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#NO_MODIFICATION_ALLOWED_ERR:kotlin.Short) If an attempt is made to modify an object where modifications are not allowed. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [SYNTAX_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#SYNTAX_ERR:kotlin.Short) If an invalid or illegal string is specified. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [TYPE_MISMATCH_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#TYPE_MISMATCH_ERR:kotlin.Short) If the type of an object is incompatible with the expected type of the parameter associated to the object. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [VALIDATION_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#VALIDATION_ERR:kotlin.Short) If a call to a method such as`insertBefore`or`removeChild`would make the`Node`invalid with respect to "partial validity", this exception would be raised and the operation would not be done. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [WRONG_DOCUMENT_ERR](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#WRONG_DOCUMENT_ERR:kotlin.Short) If a`Node`is used in a different document than the one that created it (that doesn't support it). |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DOMException](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#DOMException(kotlin.Short,%20kotlin.String))`(`code:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Properties ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [code](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException#code:kotlin.Short) <br /> |

## Constants

### DOMSTRING_SIZE_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOMSTRING_SIZE_ERR: Short
```

If the specified range of text does not fit into a`DOMString`. 

 Value: 2

### HIERARCHY_REQUEST_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HIERARCHY_REQUEST_ERR: Short
```

If any`Node`is inserted somewhere it doesn't belong. 

 Value: 3

### INDEX_SIZE_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INDEX_SIZE_ERR: Short
```

If index or size is negative, or greater than the allowed value. 

 Value: 1

### INUSE_ATTRIBUTE_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INUSE_ATTRIBUTE_ERR: Short
```

If an attempt is made to add an attribute that is already in use elsewhere. 

 Value: 10

### INVALID_ACCESS_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_ACCESS_ERR: Short
```

If a parameter or an operation is not supported by the underlying object. 

 Value: 15

### INVALID_CHARACTER_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_CHARACTER_ERR: Short
```

If an invalid or illegal character is specified, such as in an XML name. 

 Value: 5

### INVALID_MODIFICATION_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_MODIFICATION_ERR: Short
```

If an attempt is made to modify the type of the underlying object. 

 Value: 13

### INVALID_STATE_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_STATE_ERR: Short
```

If an attempt is made to use an object that is not, or is no longer, usable. 

 Value: 11

### NAMESPACE_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAMESPACE_ERR: Short
```

If an attempt is made to create or change an object in a way which is incorrect with regard to namespaces. 

 Value: 14

### NOT_FOUND_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NOT_FOUND_ERR: Short
```

If an attempt is made to reference a`Node`in a context where it does not exist. 

 Value: 8

### NOT_SUPPORTED_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NOT_SUPPORTED_ERR: Short
```

If the implementation does not support the requested type of object or operation. 

 Value: 9

### NO_DATA_ALLOWED_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_DATA_ALLOWED_ERR: Short
```

If data is specified for a`Node`which does not support data. 

 Value: 6

### NO_MODIFICATION_ALLOWED_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_MODIFICATION_ALLOWED_ERR: Short
```

If an attempt is made to modify an object where modifications are not allowed. 

 Value: 7

### SYNTAX_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNTAX_ERR: Short
```

If an invalid or illegal string is specified. 

 Value: 12

### TYPE_MISMATCH_ERR

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MISMATCH_ERR: Short
```

If the type of an object is incompatible with the expected type of the parameter associated to the object. 

 Value: 17

### VALIDATION_ERR

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VALIDATION_ERR: Short
```

If a call to a method such as`insertBefore`or`removeChild`would make the`Node`invalid with respect to "partial validity", this exception would be raised and the operation would not be done. This code is used in \ [[DOM Level 3 Validation](http://www.w3.org/TR/2004/REC-DOM-Level-3-Val-20040127/)\] . Refer to this specification for further information. 

 Value: 16

### WRONG_DOCUMENT_ERR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WRONG_DOCUMENT_ERR: Short
```

If a`Node`is used in a different document than the one that created it (that doesn't support it). 

 Value: 4

## Public constructors

### DOMException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DOMException(
    code: Short, 
    message: String!)
```

## Properties

### code

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var code: Short
```
