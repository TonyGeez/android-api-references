# AnnotationTypeMismatchException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnnotationTypeMismatchException

```
open class AnnotationTypeMismatchException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.annotation.AnnotationTypeMismatchException](https://developer.android.com/reference/kotlin/java/lang/annotation/AnnotationTypeMismatchException#) |

Thrown to indicate that a program has attempted to access an element of an annotation whose type has changed after the annotation was compiled (or serialized). This exception can be thrown by the .

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AnnotationTypeMismatchException](https://developer.android.com/reference/kotlin/java/lang/annotation/AnnotationTypeMismatchException#AnnotationTypeMismatchException(java.lang.reflect.Method,%20kotlin.String))`(`element:` ` [Method](https://developer.android.com/reference/kotlin/java/lang/reflect/Method.html#)!`, `foundType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an AnnotationTypeMismatchException for the specified annotation type element and found data type. |

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Method](https://developer.android.com/reference/kotlin/java/lang/reflect/Method.html#)! | [element](https://developer.android.com/reference/kotlin/java/lang/annotation/AnnotationTypeMismatchException#element())`()` Returns the`Method`object for the incorrectly typed element. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [foundType](https://developer.android.com/reference/kotlin/java/lang/annotation/AnnotationTypeMismatchException#foundType())`()` Returns the type of data found in the incorrectly typed element. |

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
| `element` | [Method](https://developer.android.com/reference/kotlin/java/lang/reflect/Method.html#)!:the`Method`object for the annotation element, may be`null` |
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
| [Method](https://developer.android.com/reference/kotlin/java/lang/reflect/Method.html#)! | the`Method`object for the incorrectly typed element, or`null`if unavailable |

### foundType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun foundType(): String!
```

Returns the type of data found in the incorrectly typed element. The returned string may, but is not required to, contain the value as well. The exact format of the string is unspecified and the string may be`null`.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the type of data found in the incorrectly typed element |
