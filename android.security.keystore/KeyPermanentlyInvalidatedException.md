# KeyPermanentlyInvalidatedException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyPermanentlyInvalidatedException

Kotlin| [Java](https://developer.android.com/reference/android/security/keystore/KeyPermanentlyInvalidatedException "View this page in Java") 

```
open class KeyPermanentlyInvalidatedException : InvalidKeyException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) ||||
| | | | ↳ | [java.security.KeyException](https://developer.android.com/reference/kotlin/java/security/KeyException.html#) |||
| | | | | ↳ | [java.security.InvalidKeyException](https://developer.android.com/reference/kotlin/java/security/InvalidKeyException.html#) ||
| | | | | | ↳ | [android.security.keystore.KeyPermanentlyInvalidatedException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyPermanentlyInvalidatedException#) |

Indicates that the key can no longer be used because it has been permanently invalidated.

This only occurs for keys which are authorized to be used only if the user has been authenticated. Such keys are permanently and irreversibly invalidated once the secure lock screen is disabled (i.e., reconfigured to None, Swipe or other mode which does not authenticate the user) or when the secure lock screen is forcibly reset (e.g., by Device Admin). Additionally, keys configured to require user authentication to take place for every of the keys, are also permanently invalidated once a new fingerprint is enrolled or once no more fingerprints are enrolled.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyPermanentlyInvalidatedException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyPermanentlyInvalidatedException#KeyPermanentlyInvalidatedException())`()` Constructs a new`KeyPermanentlyInvalidatedException`without detail message and cause. |
| [KeyPermanentlyInvalidatedException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyPermanentlyInvalidatedException#KeyPermanentlyInvalidatedException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`KeyPermanentlyInvalidatedException`with the provided detail message and no cause. |
| [KeyPermanentlyInvalidatedException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyPermanentlyInvalidatedException#KeyPermanentlyInvalidatedException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new`KeyPermanentlyInvalidatedException`with the provided detail message and cause. |

## Public constructors

### KeyPermanentlyInvalidatedException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyPermanentlyInvalidatedException()
```

Constructs a new`KeyPermanentlyInvalidatedException`without detail message and cause. 

### KeyPermanentlyInvalidatedException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyPermanentlyInvalidatedException(message: String!)
```

Constructs a new`KeyPermanentlyInvalidatedException`with the provided detail message and no cause. 

### KeyPermanentlyInvalidatedException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyPermanentlyInvalidatedException(
    message: String!, 
    cause: Throwable!)
```

Constructs a new`KeyPermanentlyInvalidatedException`with the provided detail message and cause.
