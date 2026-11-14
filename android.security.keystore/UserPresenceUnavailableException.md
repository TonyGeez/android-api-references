# UserPresenceUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserPresenceUnavailableException

Kotlin| [Java](https://developer.android.com/reference/android/security/keystore/UserPresenceUnavailableException "View this page in Java") 

```
open class UserPresenceUnavailableException : InvalidKeyException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) ||||
| | | | ↳ | [java.security.KeyException](https://developer.android.com/reference/kotlin/java/security/KeyException.html#) |||
| | | | | ↳ | [java.security.InvalidKeyException](https://developer.android.com/reference/kotlin/java/security/InvalidKeyException.html#) ||
| | | | | | ↳ | [android.security.keystore.UserPresenceUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/UserPresenceUnavailableException#) |

Indicates the condition that a proof of user-presence was requested but this proof was not presented.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UserPresenceUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/UserPresenceUnavailableException#UserPresenceUnavailableException())`()` Constructs a`UserPresenceUnavailableException`without a detail message or cause. |
| [UserPresenceUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/UserPresenceUnavailableException#UserPresenceUnavailableException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`UserPresenceUnavailableException`using the provided detail message but no cause. |
| [UserPresenceUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/UserPresenceUnavailableException#UserPresenceUnavailableException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`UserPresenceUnavailableException`using the provided detail message and cause. |

## Public constructors

### UserPresenceUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UserPresenceUnavailableException()
```

Constructs a`UserPresenceUnavailableException`without a detail message or cause. 

### UserPresenceUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UserPresenceUnavailableException(message: String!)
```

Constructs a`UserPresenceUnavailableException`using the provided detail message but no cause. 

### UserPresenceUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UserPresenceUnavailableException(
    message: String!, 
    cause: Throwable!)
```

Constructs a`UserPresenceUnavailableException`using the provided detail message and cause.
