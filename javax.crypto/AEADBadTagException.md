# AEADBadTagException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AEADBadTagException

```
open class AEADBadTagException : BadPaddingException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) |||
| | | | ↳ | [javax.crypto.BadPaddingException](https://developer.android.com/reference/kotlin/javax/crypto/BadPaddingException) ||
| | | | | ↳ | [javax.crypto.AEADBadTagException](https://developer.android.com/reference/kotlin/javax/crypto/AEADBadTagException#) |

This exception is thrown when a [Cipher](https://developer.android.com/reference/kotlin/javax/crypto/Cipher) operating in an AEAD mode (such as GCM/CCM) is unable to verify the supplied authentication tag.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AEADBadTagException](https://developer.android.com/reference/kotlin/javax/crypto/AEADBadTagException#AEADBadTagException())`()` Constructs a AEADBadTagException with no detail message. |
| [AEADBadTagException](https://developer.android.com/reference/kotlin/javax/crypto/AEADBadTagException#AEADBadTagException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a AEADBadTagException with the specified detail message. |

## Public constructors

### AEADBadTagException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AEADBadTagException()
```

Constructs a AEADBadTagException with no detail message. 

### AEADBadTagException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AEADBadTagException(msg: String!)
```

Constructs a AEADBadTagException with the specified detail message.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
