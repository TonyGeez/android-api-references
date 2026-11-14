# PrivilegedActionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrivilegedActionException

```
open class PrivilegedActionException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [java.security.PrivilegedActionException](PrivilegedActionException.md) |
| --- | --- | --- | --- |

Legacy security code; do not use. This exception is thrown by`doPrivileged(PrivilegedExceptionAction)`and`doPrivileged(PrivilegedExceptionAction, AccessControlContext context)`to indicate that the action being performed threw a checked exception. The exception thrown by the action can be obtained by calling the`getException`method. In effect, an`PrivilegedActionException`is a "wrapper" for an exception thrown by a privileged action.

As of release 1.4, this exception has been retrofitted to conform to the general purpose exception-chaining mechanism. The "exception thrown by the privileged computation" that is provided at construction time and accessed via the [getException()](PrivilegedActionException.md))method is now known as the*cause* , and may be accessed via the [Throwable.getCause()](../java.lang/Throwable.md))method, as well as the aforementioned "legacy method."

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PrivilegedActionException](PrivilegedActionException.md))`(`exception:` ` [Exception](../java.lang/Exception.md)!`)` Constructs a new PrivilegedActionException "wrapping" the specific Exception. |

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Exception](../java.lang/Exception.md)! | [getException](PrivilegedActionException.md))`()` Returns the exception thrown by the privileged computation that resulted in this`PrivilegedActionException`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](PrivilegedActionException.md))`()` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](PrivilegedActionException.md) Returns the cause of this exception (the exception thrown by the privileged computation that resulted in this`PrivilegedActionException`). |

## Public constructors

### PrivilegedActionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrivilegedActionException(exception: Exception!)
```

Constructs a new PrivilegedActionException "wrapping" the specific Exception.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------|
| `exception` | [Exception](../java.lang/Exception.md)!:The exception thrown |

## Public methods

### getException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getException(): Exception!
```

Returns the exception thrown by the privileged computation that resulted in this`PrivilegedActionException`.

This method predates the general-purpose exception chaining facility. The [Throwable.getCause()](../java.lang/Throwable.md))method is now the preferred means of obtaining this information.

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Exception](../java.lang/Exception.md)! | the exception thrown by the privileged computation that resulted in this`PrivilegedActionException`. |

**See Also**

- [java.security.PrivilegedExceptionAction](PrivilegedExceptionAction.md)
- [java.security.AccessController#doPrivileged(PrivilegedExceptionAction)](AccessController.md))
- [java.security.AccessController#doPrivileged(PrivilegedExceptionAction,
* AccessControlContext)](AccessController.md)) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this throwable. |

## Properties

### cause

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val cause: Throwable?
```

Returns the cause of this exception (the exception thrown by the privileged computation that resulted in this`PrivilegedActionException`).

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | the cause of this exception. |
