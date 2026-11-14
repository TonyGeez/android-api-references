# UserNotAuthenticatedException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserNotAuthenticatedException

Kotlin| [Java](../android/security/keystore/UserNotAuthenticatedException.md) 
| --- | --- |

```
open class UserNotAuthenticatedException : InvalidKeyException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||||
| | | ↳ | [java.security.GeneralSecurityException](../java/security/GeneralSecurityException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.KeyException](../java/security/KeyException.md) |||
| | | | | ↳ | [java.security.InvalidKeyException](../java/security/InvalidKeyException.md) ||
| | | | | | ↳ | [android.security.keystore.UserNotAuthenticatedException](../android/security/keystore/UserNotAuthenticatedException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Indicates that a cryptographic operation could not be performed because the user has not been authenticated recently enough. Authenticating the user will resolve this issue.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UserNotAuthenticatedException](../android/security/keystore/UserNotAuthenticatedException.md))`()` Constructs a new`UserNotAuthenticatedException`without detail message and cause. |
| [UserNotAuthenticatedException](../android/security/keystore/UserNotAuthenticatedException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`UserNotAuthenticatedException`with the provided detail message and no cause. |
| [UserNotAuthenticatedException](../android/security/keystore/UserNotAuthenticatedException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new`UserNotAuthenticatedException`with the provided detail message and cause. |

## Public constructors

### UserNotAuthenticatedException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UserNotAuthenticatedException()
```

Constructs a new`UserNotAuthenticatedException`without detail message and cause. 

### UserNotAuthenticatedException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UserNotAuthenticatedException(message: String!)
```

Constructs a new`UserNotAuthenticatedException`with the provided detail message and no cause. 

### UserNotAuthenticatedException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UserNotAuthenticatedException(
    message: String!, 
    cause: Throwable!)
```

Constructs a new`UserNotAuthenticatedException`with the provided detail message and cause.
