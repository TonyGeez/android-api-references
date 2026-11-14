# UserNotAuthenticatedException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserNotAuthenticatedException

Kotlin| [Java](https://developer.android.com/reference/android/security/keystore/UserNotAuthenticatedException "View this page in Java") 
| --- | --- |

```
open class UserNotAuthenticatedException : InvalidKeyException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.KeyException](https://developer.android.com/reference/kotlin/java/security/KeyException.html#) |||
| | | | | ↳ | [java.security.InvalidKeyException](https://developer.android.com/reference/kotlin/java/security/InvalidKeyException.html#) ||
| | | | | | ↳ | [android.security.keystore.UserNotAuthenticatedException](https://developer.android.com/reference/kotlin/android/security/keystore/UserNotAuthenticatedException#) |
| --- | --- | --- | --- | --- | --- | --- |

Indicates that a cryptographic operation could not be performed because the user has not been authenticated recently enough. Authenticating the user will resolve this issue.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UserNotAuthenticatedException](https://developer.android.com/reference/kotlin/android/security/keystore/UserNotAuthenticatedException#UserNotAuthenticatedException())`()` Constructs a new`UserNotAuthenticatedException`without detail message and cause. |
| [UserNotAuthenticatedException](https://developer.android.com/reference/kotlin/android/security/keystore/UserNotAuthenticatedException#UserNotAuthenticatedException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`UserNotAuthenticatedException`with the provided detail message and no cause. |
| [UserNotAuthenticatedException](https://developer.android.com/reference/kotlin/android/security/keystore/UserNotAuthenticatedException#UserNotAuthenticatedException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new`UserNotAuthenticatedException`with the provided detail message and cause. |

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
