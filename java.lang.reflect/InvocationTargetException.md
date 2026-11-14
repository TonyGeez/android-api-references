# InvocationTargetException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvocationTargetException

```
open class InvocationTargetException : ReflectiveOperationException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.ReflectiveOperationException](https://developer.android.com/reference/kotlin/java/lang/ReflectiveOperationException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.reflect.InvocationTargetException](https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationTargetException#) |

InvocationTargetException is a checked exception that wraps an exception thrown by an invoked method or constructor.

As of release 1.4, this exception has been retrofitted to conform to the general purpose exception-chaining mechanism. The "target exception" that is provided at construction time and accessed via the [getTargetException()](https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationTargetException#getTargetException())method is now known as the*cause* , and may be accessed via the [Throwable.getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method, as well as the aforementioned "legacy method."

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InvocationTargetException](https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationTargetException#InvocationTargetException(kotlin.Throwable))`(`target:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a InvocationTargetException with a target exception. |
| [InvocationTargetException](https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationTargetException#InvocationTargetException(kotlin.Throwable,%20kotlin.String))`(`target:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`, `s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a InvocationTargetException with a target exception and a detail message. |

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InvocationTargetException](https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationTargetException#InvocationTargetException())`()` Constructs an`InvocationTargetException`with`null`as the target exception. |

| Public methods ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [getTargetException](https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationTargetException#getTargetException())`()` Get the thrown target exception. |

| Properties ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationTargetException#cause:kotlin.Throwable) Returns the cause of this exception (the thrown target exception, which may be`null`). |

## Public constructors

### InvocationTargetException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvocationTargetException(target: Throwable!)
```

Constructs a InvocationTargetException with a target exception.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `target` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the target exception |

### InvocationTargetException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvocationTargetException(
    target: Throwable!, 
    s: String!)
```

Constructs a InvocationTargetException with a target exception and a detail message.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `target` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the target exception |
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |

## Protected constructors

### InvocationTargetException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected InvocationTargetException()
```

Constructs an`InvocationTargetException`with`null`as the target exception.

## Public methods

### getTargetException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTargetException(): Throwable!
```

Get the thrown target exception.

This method predates the general-purpose exception chaining facility. The [Throwable.getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method is now the preferred means of obtaining this information.

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | the thrown target exception (cause of this exception). |

## Properties

### cause

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val cause: Throwable?
```

Returns the cause of this exception (the thrown target exception, which may be`null`).

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | the cause of this exception. |
