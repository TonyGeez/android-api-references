# PrivilegedActionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrivilegedActionException

```
open class PrivilegedActionException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [java.security.PrivilegedActionException](https://developer.android.com/reference/kotlin/java/security/PrivilegedActionException#) |
| --- | --- | --- | --- |

Legacy security code; do not use. This exception is thrown by`doPrivileged(PrivilegedExceptionAction)`and`doPrivileged(PrivilegedExceptionAction, AccessControlContext context)`to indicate that the action being performed threw a checked exception. The exception thrown by the action can be obtained by calling the`getException`method. In effect, an`PrivilegedActionException`is a "wrapper" for an exception thrown by a privileged action.

As of release 1.4, this exception has been retrofitted to conform to the general purpose exception-chaining mechanism. The "exception thrown by the privileged computation" that is provided at construction time and accessed via the [getException()](https://developer.android.com/reference/kotlin/java/security/PrivilegedActionException#getException())method is now known as the*cause* , and may be accessed via the [Throwable.getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method, as well as the aforementioned "legacy method."

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PrivilegedActionException](https://developer.android.com/reference/kotlin/java/security/PrivilegedActionException#PrivilegedActionException(java.lang.Exception))`(`exception:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!`)` Constructs a new PrivilegedActionException "wrapping" the specific Exception. |

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)! | [getException](https://developer.android.com/reference/kotlin/java/security/PrivilegedActionException#getException())`()` Returns the exception thrown by the privileged computation that resulted in this`PrivilegedActionException`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/PrivilegedActionException#toString())`()` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](https://developer.android.com/reference/kotlin/java/security/PrivilegedActionException#cause:kotlin.Throwable) Returns the cause of this exception (the exception thrown by the privileged computation that resulted in this`PrivilegedActionException`). |

## Public constructors

### PrivilegedActionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrivilegedActionException(exception: Exception!)
```

Constructs a new PrivilegedActionException "wrapping" the specific Exception.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------|
| `exception` | [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!:The exception thrown |

## Public methods

### getException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getException(): Exception!
```

Returns the exception thrown by the privileged computation that resulted in this`PrivilegedActionException`.

This method predates the general-purpose exception chaining facility. The [Throwable.getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method is now the preferred means of obtaining this information.

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)! | the exception thrown by the privileged computation that resulted in this`PrivilegedActionException`. |

**See Also**

- [java.security.PrivilegedExceptionAction](https://developer.android.com/reference/kotlin/java/security/PrivilegedExceptionAction)
- [java.security.AccessController#doPrivileged(PrivilegedExceptionAction)](https://developer.android.com/reference/kotlin/java/security/AccessController#doPrivileged(java.security.PrivilegedExceptionAction))
- [java.security.AccessController#doPrivileged(PrivilegedExceptionAction,
* AccessControlContext)](https://developer.android.com/reference/kotlin/java/security/AccessController#doPrivileged(java.security.PrivilegedExceptionAction,%20java.security.AccessControlContext)) 

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
