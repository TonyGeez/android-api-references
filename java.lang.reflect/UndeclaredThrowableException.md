# UndeclaredThrowableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UndeclaredThrowableException

```
open class UndeclaredThrowableException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.reflect.UndeclaredThrowableException](https://developer.android.com/reference/kotlin/java/lang/reflect/UndeclaredThrowableException#) |

Thrown by a method invocation on a proxy instance if its invocation handler's [invoke](https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationHandler#invoke(kotlin.Any,%20java.lang.reflect.Method,%20kotlin.Array))method throws a checked exception (a`Throwable`that is not assignable to`RuntimeException`or`Error`) that is not assignable to any of the exception types declared in the`throws`clause of the method that was invoked on the proxy instance and dispatched to the invocation handler.

An`UndeclaredThrowableException`instance contains the undeclared checked exception that was thrown by the invocation handler, and it can be retrieved with the`getUndeclaredThrowable()`method.`UndeclaredThrowableException`extends`RuntimeException`, so it is an unchecked exception that wraps a checked exception.

As of release 1.4, this exception has been retrofitted to conform to the general purpose exception-chaining mechanism. The "undeclared checked exception that was thrown by the invocation handler" that may be provided at construction time and accessed via the [getUndeclaredThrowable()](https://developer.android.com/reference/kotlin/java/lang/reflect/UndeclaredThrowableException#getUndeclaredThrowable())method is now known as the*cause* , and may be accessed via the [java.lang.Throwable#getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method, as well as the aforementioned "legacy method."

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UndeclaredThrowableException](https://developer.android.com/reference/kotlin/java/lang/reflect/UndeclaredThrowableException#UndeclaredThrowableException(kotlin.Throwable))`(`undeclaredThrowable:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an`UndeclaredThrowableException`with the specified`Throwable`. |
| [UndeclaredThrowableException](https://developer.android.com/reference/kotlin/java/lang/reflect/UndeclaredThrowableException#UndeclaredThrowableException(kotlin.Throwable,%20kotlin.String))`(`undeclaredThrowable:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`, `s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`UndeclaredThrowableException`with the specified`Throwable`and a detail message. |

| Public methods ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [getUndeclaredThrowable](https://developer.android.com/reference/kotlin/java/lang/reflect/UndeclaredThrowableException#getUndeclaredThrowable())`()` Returns the`Throwable`instance wrapped in this`UndeclaredThrowableException`, which may be`null`. |

| Properties ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](https://developer.android.com/reference/kotlin/java/lang/reflect/UndeclaredThrowableException#cause:kotlin.Throwable) Returns the cause of this exception (the`Throwable`instance wrapped in this`UndeclaredThrowableException`, which may be`null`). |

## Public constructors

### UndeclaredThrowableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UndeclaredThrowableException(undeclaredThrowable: Throwable!)
```

Constructs an`UndeclaredThrowableException`with the specified`Throwable`.

| Parameters ||
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `undeclaredThrowable` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the undeclared checked exception that was thrown |

### UndeclaredThrowableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UndeclaredThrowableException(
    undeclaredThrowable: Throwable!, 
    s: String!)
```

Constructs an`UndeclaredThrowableException`with the specified`Throwable`and a detail message.

| Parameters ||
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `undeclaredThrowable` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the undeclared checked exception that was thrown |
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |

## Public methods

### getUndeclaredThrowable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUndeclaredThrowable(): Throwable!
```

Returns the`Throwable`instance wrapped in this`UndeclaredThrowableException`, which may be`null`.

This method predates the general-purpose exception chaining facility. The [Throwable.getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method is now the preferred means of obtaining this information.

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | the undeclared checked exception that was thrown |

## Properties

### cause

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val cause: Throwable?
```

Returns the cause of this exception (the`Throwable`instance wrapped in this`UndeclaredThrowableException`, which may be`null`).

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | the cause of this exception. |
