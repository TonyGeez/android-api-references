# ExceptionInInitializerError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExceptionInInitializerError

```
open class ExceptionInInitializerError : LinkageError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error) |||
| | | ↳ | [java.lang.LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.ExceptionInInitializerError](https://developer.android.com/reference/kotlin/java/lang/ExceptionInInitializerError#) |

Signals that an unexpected exception has occurred in a static initializer. An`ExceptionInInitializerError`is thrown to indicate that an exception occurred during evaluation of a static initializer or the initializer for a static variable.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ExceptionInInitializerError](https://developer.android.com/reference/kotlin/java/lang/ExceptionInInitializerError#ExceptionInInitializerError())`()` Constructs an`ExceptionInInitializerError`with`null`as its detail message string and with no saved throwable object. |
| [ExceptionInInitializerError](https://developer.android.com/reference/kotlin/java/lang/ExceptionInInitializerError#ExceptionInInitializerError(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`ExceptionInInitializerError`with the specified detail message string. |
| [ExceptionInInitializerError](https://developer.android.com/reference/kotlin/java/lang/ExceptionInInitializerError#ExceptionInInitializerError(kotlin.Throwable))`(`thrown:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new`ExceptionInInitializerError`class by saving a reference to the`Throwable`object thrown for later retrieval by the [getException()](https://developer.android.com/reference/kotlin/java/lang/ExceptionInInitializerError#getException())method. |

| Public methods ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [getException](https://developer.android.com/reference/kotlin/java/lang/ExceptionInInitializerError#getException())`()` Returns the exception that occurred during a static initialization that caused this error to be created. |

## Public constructors

### ExceptionInInitializerError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExceptionInInitializerError()
```

Constructs an`ExceptionInInitializerError`with`null`as its detail message string and with no saved throwable object. A detail message is a String that describes this particular exception. 

### ExceptionInInitializerError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExceptionInInitializerError(s: String!)
```

Constructs an`ExceptionInInitializerError`with the specified detail message string. A detail message is a String that describes this particular exception. The detail message string is saved for later retrieval by the [Throwable.getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage())method. There is no saved throwable object.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |

### ExceptionInInitializerError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExceptionInInitializerError(thrown: Throwable!)
```

Constructs a new`ExceptionInInitializerError`class by saving a reference to the`Throwable`object thrown for later retrieval by the [getException()](https://developer.android.com/reference/kotlin/java/lang/ExceptionInInitializerError#getException())method. The detail message string is set to`null`.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `thrown` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:The exception thrown |

## Public methods

### getException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getException(): Throwable!
```

Returns the exception that occurred during a static initialization that caused this error to be created.

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | the saved throwable object of this`ExceptionInInitializerError`, or`null`if this`ExceptionInInitializerError`has no saved throwable object. |
