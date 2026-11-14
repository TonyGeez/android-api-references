# KeyExpiredException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyExpiredException

Kotlin| [Java](https://developer.android.com/reference/android/security/keystore/KeyExpiredException "View this page in Java") 

```
open class KeyExpiredException : InvalidKeyException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) ||||
| | | | ↳ | [java.security.KeyException](https://developer.android.com/reference/kotlin/java/security/KeyException.html#) |||
| | | | | ↳ | [java.security.InvalidKeyException](https://developer.android.com/reference/kotlin/java/security/InvalidKeyException.html#) ||
| | | | | | ↳ | [android.security.keystore.KeyExpiredException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyExpiredException#) |

Indicates that a cryptographic operation failed because the employed key's validity end date is in the past.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyExpiredException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyExpiredException#KeyExpiredException())`()` Constructs a new`KeyExpiredException`without detail message and cause. |
| [KeyExpiredException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyExpiredException#KeyExpiredException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`KeyExpiredException`with the provided detail message and no cause. |
| [KeyExpiredException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyExpiredException#KeyExpiredException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new`KeyExpiredException`with the provided detail message and cause. |

## Public constructors

### KeyExpiredException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyExpiredException()
```

Constructs a new`KeyExpiredException`without detail message and cause. 

### KeyExpiredException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyExpiredException(message: String!)
```

Constructs a new`KeyExpiredException`with the provided detail message and no cause. 

### KeyExpiredException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyExpiredException(
    message: String!, 
    cause: Throwable!)
```

Constructs a new`KeyExpiredException`with the provided detail message and cause.
