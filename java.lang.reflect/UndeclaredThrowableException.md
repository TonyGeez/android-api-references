# UndeclaredThrowableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UndeclaredThrowableException

```
open class UndeclaredThrowableException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.reflect.UndeclaredThrowableException](../java/lang/reflect/UndeclaredThrowableException.md) |

Thrown by a method invocation on a proxy instance if its invocation handler's [invoke](../java/lang/reflect/InvocationHandler.md))method throws a checked exception (a`Throwable`that is not assignable to`RuntimeException`or`Error`) that is not assignable to any of the exception types declared in the`throws`clause of the method that was invoked on the proxy instance and dispatched to the invocation handler.

An`UndeclaredThrowableException`instance contains the undeclared checked exception that was thrown by the invocation handler, and it can be retrieved with the`getUndeclaredThrowable()`method.`UndeclaredThrowableException`extends`RuntimeException`, so it is an unchecked exception that wraps a checked exception.

As of release 1.4, this exception has been retrofitted to conform to the general purpose exception-chaining mechanism. The "undeclared checked exception that was thrown by the invocation handler" that may be provided at construction time and accessed via the [getUndeclaredThrowable()](../java/lang/reflect/UndeclaredThrowableException.md))method is now known as the*cause* , and may be accessed via the [java.lang.Throwable#getCause()](../java/lang/Throwable.md))method, as well as the aforementioned "legacy method."

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UndeclaredThrowableException](../java/lang/reflect/UndeclaredThrowableException.md))`(`undeclaredThrowable:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an`UndeclaredThrowableException`with the specified`Throwable`. |
| [UndeclaredThrowableException](../java/lang/reflect/UndeclaredThrowableException.md))`(`undeclaredThrowable:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`, `s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`UndeclaredThrowableException`with the specified`Throwable`and a detail message. |

| Public methods ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [getUndeclaredThrowable](../java/lang/reflect/UndeclaredThrowableException.md))`()` Returns the`Throwable`instance wrapped in this`UndeclaredThrowableException`, which may be`null`. |

| Properties ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](../java/lang/reflect/UndeclaredThrowableException.md) Returns the cause of this exception (the`Throwable`instance wrapped in this`UndeclaredThrowableException`, which may be`null`). |

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

This method predates the general-purpose exception chaining facility. The [Throwable.getCause()](../java/lang/Throwable.md))method is now the preferred means of obtaining this information.

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
