# InvalidKeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvalidKeyException

```
open class InvalidKeyException : KeyException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.KeyException](https://developer.android.com/reference/kotlin/java/security/KeyException) ||
| | | | | ↳ | [java.security.InvalidKeyException](https://developer.android.com/reference/kotlin/java/security/InvalidKeyException#) |

| Known Direct Subclasses [KeyExpiredException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyExpiredException.html#), [KeyNotYetValidException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyNotYetValidException.html#), [KeyPermanentlyInvalidatedException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyPermanentlyInvalidatedException.html#), [UserNotAuthenticatedException](https://developer.android.com/reference/kotlin/android/security/keystore/UserNotAuthenticatedException.html#), [UserPresenceUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/UserPresenceUnavailableException.html#) |---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------| | [KeyExpiredException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyExpiredException.html#) | Indicates that a cryptographic operation failed because the employed key's validity end date is in the past. | | [KeyNotYetValidException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyNotYetValidException.html#) | Indicates that a cryptographic operation failed because the employed key's validity start date is in the future. | | [KeyPermanentlyInvalidatedException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyPermanentlyInvalidatedException.html#) | Indicates that the key can no longer be used because it has been permanently invalidated. | | [UserNotAuthenticatedException](https://developer.android.com/reference/kotlin/android/security/keystore/UserNotAuthenticatedException.html#) | Indicates that a cryptographic operation could not be performed because the user has not been authenticated recently enough. | | [UserPresenceUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/UserPresenceUnavailableException.html#) | Indicates the condition that a proof of user-presence was requested but this proof was not presented. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This is the exception for invalid Keys (invalid encoding, wrong length, uninitialized, etc).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InvalidKeyException](https://developer.android.com/reference/kotlin/java/security/InvalidKeyException#InvalidKeyException())`()` Constructs an InvalidKeyException with no detail message. |
| [InvalidKeyException](https://developer.android.com/reference/kotlin/java/security/InvalidKeyException#InvalidKeyException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an InvalidKeyException with the specified detail message. |
| [InvalidKeyException](https://developer.android.com/reference/kotlin/java/security/InvalidKeyException#InvalidKeyException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates an`InvalidKeyException`with the specified detail message and cause. |
| [InvalidKeyException](https://developer.android.com/reference/kotlin/java/security/InvalidKeyException#InvalidKeyException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates an`InvalidKeyException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### InvalidKeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidKeyException()
```

Constructs an InvalidKeyException with no detail message. A detail message is a String that describes this particular exception. 

### InvalidKeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidKeyException(msg: String!)
```

Constructs an InvalidKeyException with the specified detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### InvalidKeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidKeyException(
    message: String!, 
    cause: Throwable!)
```

Creates an`InvalidKeyException`with the specified detail message and cause.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### InvalidKeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidKeyException(cause: Throwable!)
```

Creates an`InvalidKeyException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
