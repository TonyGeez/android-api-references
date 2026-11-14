# KeyNotYetValidException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyNotYetValidException

Kotlin| [Java](https://developer.android.com/reference/android/security/keystore/KeyNotYetValidException "View this page in Java") 

```
open class KeyNotYetValidException : InvalidKeyException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) ||||
| | | | ↳ | [java.security.KeyException](https://developer.android.com/reference/kotlin/java/security/KeyException.html#) |||
| | | | | ↳ | [java.security.InvalidKeyException](https://developer.android.com/reference/kotlin/java/security/InvalidKeyException.html#) ||
| | | | | | ↳ | [android.security.keystore.KeyNotYetValidException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyNotYetValidException#) |

Indicates that a cryptographic operation failed because the employed key's validity start date is in the future.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyNotYetValidException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyNotYetValidException#KeyNotYetValidException())`()` Constructs a new`KeyNotYetValidException`without detail message and cause. |
| [KeyNotYetValidException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyNotYetValidException#KeyNotYetValidException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`KeyNotYetValidException`with the provided detail message and no cause. |
| [KeyNotYetValidException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyNotYetValidException#KeyNotYetValidException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new`KeyNotYetValidException`with the provided detail message and cause. |

## Public constructors

### KeyNotYetValidException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyNotYetValidException()
```

Constructs a new`KeyNotYetValidException`without detail message and cause. 

### KeyNotYetValidException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyNotYetValidException(message: String!)
```

Constructs a new`KeyNotYetValidException`with the provided detail message and no cause. 

### KeyNotYetValidException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyNotYetValidException(
    message: String!, 
    cause: Throwable!)
```

Constructs a new`KeyNotYetValidException`with the provided detail message and cause.
