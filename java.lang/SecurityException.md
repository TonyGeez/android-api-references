# SecurityException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecurityException

```
open class SecurityException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) ||
| | | | ↳ | [java.lang.SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException#) |

| Known Direct Subclasses [AccessControlException](https://developer.android.com/reference/kotlin/java/security/AccessControlException.html#), [AuthenticationRequiredException](https://developer.android.com/reference/kotlin/android/app/AuthenticationRequiredException.html#), [RecoverableSecurityException](https://developer.android.com/reference/kotlin/android/app/RecoverableSecurityException.html#) |-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AccessControlException](https://developer.android.com/reference/kotlin/java/security/AccessControlException.html#) | This exception is thrown by the AccessController to indicate that a requested access (to a critical system resource such as the file system or the network) is denied. | | [AuthenticationRequiredException](https://developer.android.com/reference/kotlin/android/app/AuthenticationRequiredException.html#) | Specialization of [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException#) that is thrown when authentication is needed from the end user before viewing the content. | | [RecoverableSecurityException](https://developer.android.com/reference/kotlin/android/app/RecoverableSecurityException.html#) | Specialization of [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException#) that contains additional information about how to involve the end user to recover from the exception. | |

Thrown by the security manager to indicate a security violation.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException#SecurityException())`()` Constructs a`SecurityException`with no detail message. |
| [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException#SecurityException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SecurityException`with the specified detail message. |
| [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException#SecurityException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`SecurityException`with the specified detail message and cause. |
| [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException#SecurityException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`SecurityException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### SecurityException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SecurityException()
```

Constructs a`SecurityException`with no detail message. 

### SecurityException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SecurityException(s: String!)
```

Constructs a`SecurityException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### SecurityException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SecurityException(
    message: String!, 
    cause: Throwable!)
```

Creates a`SecurityException`with the specified detail message and cause.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage())method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### SecurityException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SecurityException(cause: Throwable!)
```

Creates a`SecurityException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
