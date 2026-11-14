# IncompleteAnnotationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IncompleteAnnotationException

```
open class IncompleteAnnotationException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.annotation.IncompleteAnnotationException](https://developer.android.com/reference/kotlin/java/lang/annotation/IncompleteAnnotationException#) |

Thrown to indicate that a program has attempted to access an element of an annotation interface that was added to the annotation interface definition after the annotation was compiled (or serialized). This exception will not be thrown if the new element has a default value. This exception can be thrown by the .

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IncompleteAnnotationException](https://developer.android.com/reference/kotlin/java/lang/annotation/IncompleteAnnotationException#IncompleteAnnotationException(java.lang.Class,%20kotlin.String))`(`annotationType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<out` ` [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!>!`, `elementName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an IncompleteAnnotationException to indicate that the named element was missing from the specified annotation interface. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<out [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\>! | [annotationType](https://developer.android.com/reference/kotlin/java/lang/annotation/IncompleteAnnotationException#annotationType())`()` Returns the Class object for the annotation interface with the missing element. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [elementName](https://developer.android.com/reference/kotlin/java/lang/annotation/IncompleteAnnotationException#elementName())`()` Returns the name of the missing element. |

## Public constructors

### IncompleteAnnotationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IncompleteAnnotationException(
    annotationType: Class<out Annotation!>!, 
    elementName: String!)
```

Constructs an IncompleteAnnotationException to indicate that the named element was missing from the specified annotation interface.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `annotationType` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<out [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\>!:the Class object for the annotation interface |
| `elementName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the missing element |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.NullPointerException` | if either parameter is`null` |

## Public methods

### annotationType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun annotationType(): Class<out Annotation!>!
```

Returns the Class object for the annotation interface with the missing element.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<out` ` [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!>! | the Class object for the annotation interface with the missing element |

### elementName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun elementName(): String!
```

Returns the name of the missing element.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the missing element |
