# AnnotationTypeMismatchException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnnotationTypeMismatchException

```
open class AnnotationTypeMismatchException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.annotation.AnnotationTypeMismatchException](AnnotationTypeMismatchException.md) |

Thrown to indicate that a program has attempted to access an element of an annotation whose type has changed after the annotation was compiled (or serialized). This exception can be thrown by the .

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AnnotationTypeMismatchException](AnnotationTypeMismatchException.md))`(`element:` ` [Method](../java.lang.reflect/Method.md)!`, `foundType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an AnnotationTypeMismatchException for the specified annotation type element and found data type. |

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Method](../java.lang.reflect/Method.md)! | [element](AnnotationTypeMismatchException.md))`()` Returns the`Method`object for the incorrectly typed element. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [foundType](AnnotationTypeMismatchException.md))`()` Returns the type of data found in the incorrectly typed element. |

## Public constructors

### AnnotationTypeMismatchException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AnnotationTypeMismatchException(
    element: Method!, 
    foundType: String!)
```

Constructs an AnnotationTypeMismatchException for the specified annotation type element and found data type.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `element` | [Method](../java.lang.reflect/Method.md)!:the`Method`object for the annotation element, may be`null` |
| `foundType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the (erroneous) type of data found in the annotation. This string may, but is not required to, contain the value as well. The exact format of the string is unspecified, may be`null`. |

## Public methods

### element

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun element(): Method!
```

Returns the`Method`object for the incorrectly typed element. The value may be unavailable if this exception has been serialized and then read back in.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Method](../java.lang.reflect/Method.md)! | the`Method`object for the incorrectly typed element, or`null`if unavailable |

### foundType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun foundType(): String!
```

Returns the type of data found in the incorrectly typed element. The returned string may, but is not required to, contain the value as well. The exact format of the string is unspecified and the string may be`null`.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the type of data found in the incorrectly typed element |
