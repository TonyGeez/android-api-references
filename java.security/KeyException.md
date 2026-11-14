# KeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyException

```
open class KeyException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.security.GeneralSecurityException](../java/security/GeneralSecurityException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.KeyException](../java/security/KeyException.md) |

| Known Direct Subclasses [InvalidKeyException](../java/security/InvalidKeyException.md), [KeyManagementException](../java/security/KeyManagementException.md) |---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------| | [InvalidKeyException](../java/security/InvalidKeyException.md) | This is the exception for invalid Keys (invalid encoding, wrong length, uninitialized, etc). | | [KeyManagementException](../java/security/KeyManagementException.md) | This is the general key management exception for all operations dealing with key management. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [KeyExpiredException](../android/security/keystore/KeyExpiredException.md), [KeyNotYetValidException](../android/security/keystore/KeyNotYetValidException.md), [KeyPermanentlyInvalidatedException](../android/security/keystore/KeyPermanentlyInvalidatedException.md), [UserNotAuthenticatedException](../android/security/keystore/UserNotAuthenticatedException.md), [UserPresenceUnavailableException](../android/security/keystore/UserPresenceUnavailableException.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------| | [KeyExpiredException](../android/security/keystore/KeyExpiredException.md) | Indicates that a cryptographic operation failed because the employed key's validity end date is in the past. | | [KeyNotYetValidException](../android/security/keystore/KeyNotYetValidException.md) | Indicates that a cryptographic operation failed because the employed key's validity start date is in the future. | | [KeyPermanentlyInvalidatedException](../android/security/keystore/KeyPermanentlyInvalidatedException.md) | Indicates that the key can no longer be used because it has been permanently invalidated. | | [UserNotAuthenticatedException](../android/security/keystore/UserNotAuthenticatedException.md) | Indicates that a cryptographic operation could not be performed because the user has not been authenticated recently enough. | | [UserPresenceUnavailableException](../android/security/keystore/UserPresenceUnavailableException.md) | Indicates the condition that a proof of user-presence was requested but this proof was not presented. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This is the basic key exception.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyException](../java/security/KeyException.md))`()` Constructs a KeyException with no detail message. |
| [KeyException](../java/security/KeyException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a KeyException with the specified detail message. |
| [KeyException](../java/security/KeyException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`KeyException`with the specified detail message and cause. |
| [KeyException](../java/security/KeyException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`KeyException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### KeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyException()
```

Constructs a KeyException with no detail message. A detail message is a String that describes this particular exception. 

### KeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyException(msg: String!)
```

Constructs a KeyException with the specified detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### KeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyException(
    message: String!, 
    cause: Throwable!)
```

Creates a`KeyException`with the specified detail message and cause.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](../java/lang/Throwable.md))method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### KeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyException(cause: Throwable!)
```

Creates a`KeyException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
