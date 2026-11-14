# IncompleteAnnotationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IncompleteAnnotationException

```
open class IncompleteAnnotationException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.annotation.IncompleteAnnotationException](../java/lang/annotation/IncompleteAnnotationException.md) |

Thrown to indicate that a program has attempted to access an element of an annotation interface that was added to the annotation interface definition after the annotation was compiled (or serialized). This exception will not be thrown if the new element has a default value. This exception can be thrown by the .

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IncompleteAnnotationException](../java/lang/annotation/IncompleteAnnotationException.md))`(`annotationType:` ` [Class](../java/lang/Class.md)<out` ` [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!>!`, `elementName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an IncompleteAnnotationException to indicate that the named element was missing from the specified annotation interface. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Class](../java/lang/Class.md)\<out [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\>! | [annotationType](../java/lang/annotation/IncompleteAnnotationException.md))`()` Returns the Class object for the annotation interface with the missing element. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [elementName](../java/lang/annotation/IncompleteAnnotationException.md))`()` Returns the name of the missing element. |

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
| `annotationType` | [Class](../java/lang/Class.md)\<out [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\>!:the Class object for the annotation interface |
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
| [Class](../java/lang/Class.md)<out` ` [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!>! | the Class object for the annotation interface with the missing element |

### elementName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun elementName(): String!
```

Returns the name of the missing element.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the missing element |
