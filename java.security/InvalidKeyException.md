# InvalidKeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvalidKeyException

```
open class InvalidKeyException : KeyException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.security.GeneralSecurityException](../java/security/GeneralSecurityException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.KeyException](../java/security/KeyException.md) ||
| | | | | ↳ | [java.security.InvalidKeyException](../java/security/InvalidKeyException.md) |

| Known Direct Subclasses [KeyExpiredException](../android/security/keystore/KeyExpiredException.md), [KeyNotYetValidException](../android/security/keystore/KeyNotYetValidException.md), [KeyPermanentlyInvalidatedException](../android/security/keystore/KeyPermanentlyInvalidatedException.md), [UserNotAuthenticatedException](../android/security/keystore/UserNotAuthenticatedException.md), [UserPresenceUnavailableException](../android/security/keystore/UserPresenceUnavailableException.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------| | [KeyExpiredException](../android/security/keystore/KeyExpiredException.md) | Indicates that a cryptographic operation failed because the employed key's validity end date is in the past. | | [KeyNotYetValidException](../android/security/keystore/KeyNotYetValidException.md) | Indicates that a cryptographic operation failed because the employed key's validity start date is in the future. | | [KeyPermanentlyInvalidatedException](../android/security/keystore/KeyPermanentlyInvalidatedException.md) | Indicates that the key can no longer be used because it has been permanently invalidated. | | [UserNotAuthenticatedException](../android/security/keystore/UserNotAuthenticatedException.md) | Indicates that a cryptographic operation could not be performed because the user has not been authenticated recently enough. | | [UserPresenceUnavailableException](../android/security/keystore/UserPresenceUnavailableException.md) | Indicates the condition that a proof of user-presence was requested but this proof was not presented. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This is the exception for invalid Keys (invalid encoding, wrong length, uninitialized, etc).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InvalidKeyException](../java/security/InvalidKeyException.md))`()` Constructs an InvalidKeyException with no detail message. |
| [InvalidKeyException](../java/security/InvalidKeyException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an InvalidKeyException with the specified detail message. |
| [InvalidKeyException](../java/security/InvalidKeyException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates an`InvalidKeyException`with the specified detail message and cause. |
| [InvalidKeyException](../java/security/InvalidKeyException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates an`InvalidKeyException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

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
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](../java/lang/Throwable.md))method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### InvalidKeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidKeyException(cause: Throwable!)
```

Creates an`InvalidKeyException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
