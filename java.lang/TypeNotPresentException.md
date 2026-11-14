# TypeNotPresentException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TypeNotPresentException

```
open class TypeNotPresentException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.TypeNotPresentException](https://developer.android.com/reference/kotlin/java/lang/TypeNotPresentException#) |

Thrown when an application tries to access a type using a string representing the type's name, but no definition for the type with the specified name can be found. This exception differs from [ClassNotFoundException](https://developer.android.com/reference/kotlin/java/lang/ClassNotFoundException) in that`ClassNotFoundException`is a checked exception, whereas this exception is unchecked.

Note that this exception may be used when undefined type variables are accessed as well as when types (e.g., classes, interfaces or annotation types) are loaded. In particular, this exception can be thrown by the .

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TypeNotPresentException](https://developer.android.com/reference/kotlin/java/lang/TypeNotPresentException#TypeNotPresentException(kotlin.String,%20kotlin.Throwable))`(`typeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`TypeNotPresentException`for the named type with the specified cause. |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [typeName](https://developer.android.com/reference/kotlin/java/lang/TypeNotPresentException#typeName())`()` Returns the fully qualified name of the unavailable type. |

## Public constructors

### TypeNotPresentException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TypeNotPresentException(
    typeName: String!, 
    cause: Throwable!)
```

Constructs a`TypeNotPresentException`for the named type with the specified cause.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `typeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the fully qualified name of the unavailable type |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the exception that was thrown when the system attempted to load the named type, or`null`if unavailable or inapplicable |

## Public methods

### typeName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun typeName(): String!
```

Returns the fully qualified name of the unavailable type.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the fully qualified name of the unavailable type |
